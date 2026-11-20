+++
title = "3. La IA y los datos"
weight = 3
+++

Nota: Lectura de ampliación (esta sección se ha desplazado al final para lectura adicional).

## Conceptos clave

- Resumen técnico: elige ML clásico (árboles, SVM) para datos tabulares con poco volumen; DL (CNNs, Transformers) para imágenes/audio/texto con grandes volúmenes.  
- Validación práctica: usa validación temporal para series y cross‑validation estratificado para clasificación; siempre compara contra un baseline sencillo.  
- Producción (MLOps mínimo): versionado (DVC/git), tracking (MLflow/W&B), flujos reproducibles (Airflow/Kubeflow) y tests que bloqueen despliegues.  
- Acción inmediata: implementar un flujo de entrenamiento reproducible + pruebas de calidad de dato en ingestión.

---

La relación entre la **IA** y los **datos** es íntima: los datos son la materia prima que define lo que un sistema puede aprender y cómo se comportará en el mundo real. Esta sección desarrolla cinco subpuntos (3.1–3.5) sobre por qué los datos importan, cómo gestionarlos en flujos a escala, la calidad en contextos Big Data, y las implicaciones de privacidad, seguridad y ética.

## 3.1 Importancia del dato como materia prima

La **importancia del dato** en IA no puede subestimarse: son los ejemplos, las etiquetas y los metadatos los que permiten transformar hipótesis en modelos prácticos. Un buen diseño de datos incluye **representatividad**, balance entre clases relevantes y metadatos que describan procedencia y contexto. Si los datos son escasos o sesgados, incluso los mejores algoritmos producirán resultados poco fiables o discriminatorios. Por ello, las organizaciones maduras invierten en procesos de captura, flujos de limpieza y auditorías de calidad antes de escalar un modelo.

En práctica, los datos alimentan decisiones en todas las fases: el **entrenamiento** depende de ejemplos etiquetados y balanceados; la **validación** exige conjuntos que simulen producción; y la **monitorización** necesita métricas de calidad de entrada para detectar drift. Por ejemplo, en proyectos médicos se emplean dobles lecturas por expertos y controles de calidad para asegurar que las etiquetas reflejen diagnósticos clínicos reales.

Invertir en datos también significa medir su coste: etiquetado humano, almacenamiento y gobernanza tienen impacto presupuestario. A la hora de priorizar proyectos, conviene estimar el ROI del esfuerzo de recopilación frente al beneficio esperado, y comenzar por **pilotos** que validen hipótesis con conjuntos reducidos y de alta calidad antes de escalar.

Finalmente, los datos deben considerarse un activo gestionado: definir propietarios, políticas de retención y procesos de acceso garantiza que la materia prima esté disponible y documentada para futuros entrenamientos y auditorías.

### Ejemplos, casos, enlaces y tabla resumen — 3.1

- Ejemplo (en simple): si tu dataset incluye suficientes ejemplos de todos los grupos (representatividad), el modelo aprende mejor esos patrones y sube el **recall** en los subgrupos que antes fallaba.
- Caso real (qué es “ruido de etiquetas”): etiquetas mal puestas o inconsistentes. Herramientas como **Cleanlab** detectan y ayudan a corregir esas etiquetas; al limpiar, suele subir la **F1** sin tocar el modelo.
- Enlace (para documentar datos): [Datasheets for Datasets](https://arxiv.org/abs/1803.09010)
- Tabla comparativa rápida:

| Problema         | Efecto       | Remedio                 |
|------------------|-------------|-------------------------|
| Sesgo de muestreo| Baja general.| Muestreo estratificado  |
| Etiquetas ruidosas| Overfitting | Revisión/cleaning       |
| Metadata pobre   | Reproducib.  | Documentación/lineage   |

## 3.2 Ciclo de vida del dato y flujos (ingestión, etiquetado, versionado)

Objetivo práctico: convertir datos crudos en artefactos listos para entrenar y servir modelos, con trazabilidad y calidad.

Flujo resumido (etapas y puntos de control):

| Etapa | Qué hace | Checkpoint / artefacto | Herramientas ejemplo |
|---|---|---|---|
| Ingestión | Captura y normaliza datos desde orígenes | Raw snapshot, esquema | Kafka, Cloud Storage, Flume |
| Validación inicial | Verifica esquema y sanidad | Reglas de validación (schema) | Great Expectations |
| Limpieza & enrich | Imputación, normalización, joins | Clean dataset | Spark, Beam, pandas |
| Etiquetado | Creación/curación de etiquetas | Labeled dataset, label provenance | Label Studio, Prodigy |
| Feature engineering | Generación y versionado de features | Feature table, feature hashes | Spark, Feature Store (Feast) |
| Versionado | Registrar versión de dataset y features | Data commit, dataset hashes | DVC, Delta Lake |
| Entrenamiento | Experimentos reproducibles | Model artefact, run logs | MLflow, Kubeflow |
| Evaluación | Validación offline y pruebas de robustez | Metrics report, confusion matrix | scikit-learn, Evidently |
| Despliegue | Servir modelo con la misma lógica de features | Container/endpoint | Docker, Kubernetes, SageMaker |
| Monitorización | Detectar drift y degradación | Alertas, dashboards | Evidently, Prometheus, Grafana |

Puntos de control y buenas prácticas:

- Versiona siempre los datasets críticos (hashes + metadatos).  
- Mantén trazabilidad del etiquetado (quién, cuándo, con qué reglas).  
- Usa feature stores para evitar desalineación entre entrenamiento e inferencia.  
- Incluye tests automáticos de calidad que bloqueen despliegues.

Conceptos clave

- Feature store: catálogo de features consistentes entre entrenamiento e inferencia.  
- Data lineage: historial de transformaciones aplicado a un dataset.

### Ejemplos, casos, enlaces y tabla resumen 

- Ejemplo: Flujo con **ingestión → validación → limpieza → features → entrenamiento** y feature store para consistencia.
- Caso real: **Airflow** orquesta reentrenamiento nocturno; **Feast** sirve features alineadas entre train y prod.
- Enlace: [Feast (Feature Store)](https://feast.dev)
- Tabla comparativa rápida:

| Etapa       | Checkpoint        | Herramienta |
|-------------|-------------------|-------------|
| Validación  | Report de calidad | Great Exp.  |
| Features    | Tabla versionada  | Feast       |
| Entrenamiento| Artefacto modelo | MLflow      |

## 3.3 Big Data y calidad de los datos

**Big Data** implica volumen, velocidad y variedad—pero sin calidad, el volumen es inútil. La gestión de datos a gran escala requiere estrategias de muestreo, limpieza en streaming, deduplicación y normalización que reduzcan ruido y eviten que los modelos aprendan artefactos. Además, la integración semántica (ontologías, diccionarios) facilita combinar fuentes heterogéneas sin perder coherencia.

Herramientas distribuidas (Spark, Beam) y almacenes como BigQuery o Snowflake permiten procesar datos a escala, pero deben complementarse con frameworks de data quality (Great Expectations) y procesos de observabilidad que detecten anomalías en tiempo real. Un sistema robusto implementa alertas que disparen retraining o tareas manuales cuando cambian las distribuciones.

Ejemplo: en telemetría IoT, millones de eventos requieren filtros y agregaciones por ventana para eliminar ruido; sin esos pasos los modelos de detección de anomalías reportan demasiados falsos positivos. Telecoms y empresas industriales implementan capas de preprocesado para mejorar la señal útil antes de entrenar.

Recursos didácticos: documentación de [Apache Spark](https://spark.apache.org), [BigQuery](https://cloud.google.com/bigquery) y artículos sobre data quality en [Dataversity](https://www.dataversity.net) son buenas lecturas de referencia.

### Ejemplos, casos, enlaces y tabla resumen 
- Ejemplo: **Streaming cleanup** (filtros + ventanas) reduce ruido antes de entrenar modelos de anomalías.
- Caso real: Telemetría **IoT** con agregaciones por ventana disminuye falsos positivos y mejora precisión.
- Enlace: [Apache Spark](https://spark.apache.org)
- Tabla comparativa rápida:

| Problema  | Técnica            | Efecto              |
|-----------|--------------------|---------------------|
| Ruido     | Ventanas/filtrado  | Menos falsos positivos |
| Duplicados| Deduplicación keys | Datos consistentes  |
| Esquemas  | Validación schema  | Menos fallos en prod |

## 3.4 Privacidad y seguridad de los datos

La **privacidad** y la **seguridad** son requisitos clave en proyectos de IA. Técnicas como **anonimización**, **enmascaramiento**, **differential privacy** y **federated learning** reducen riesgos cuando se trabaja con datos sensibles. Complementariamente, controles operativos —cifrado, gestión de identidades y permisos, auditorías— son imprescindibles para cumplir normativas y proteger activos.

La elección técnica debe adecuarse al caso: **differential privacy** es útil cuando se liberan agregados protegidos; **federated learning** permite entrenar sin centralizar datos; y los enclaves de ejecución o hardware de confianza son apropiados cuando se requiere procesar datos críticos en entornos seguros. El cumplimiento con GDPR y otros marcos exige además documentación y procesos (consentimiento, DPIAs).

Ejemplo: en salud, proyectos que agrupan datos de varios hospitales usan aprendizaje federado para crear modelos comunes sin intercambiar historiales clínicos, reduciendo el riesgo de exposición. Otro caso es el uso de differential privacy por empresas que publican informes agregados de comportamiento.

Recursos: [GDPR](https://gdpr.eu/), [TensorFlow Federated](https://www.tensorflow.org/federated), y materiales sobre [differential privacy](https://privacytools.seas.harvard.edu/differential-privacy).

### Ejemplos, casos, enlaces y tabla resumen
- Ejemplo: Publicar **agregados** con differential privacy para proteger individuos.
- Caso real: **Teclados móviles** usan aprendizaje federado para mejorar sin centralizar datos.
- Enlace: [GDPR](https://gdpr.eu/)
- Tabla comparativa rápida:

| Caso        | Técnica               | Beneficio            |
|-------------|-----------------------|----------------------|
| Reportes    | Differential privacy  | Menos riesgo de fuga |
| Entrenamiento | Federated learning  | Privacidad por diseño|
| Procesamiento| Enclaves/TEE          | Entorno confiable     |

## 3.5 Ética, consentimiento y mitigación de sesgos en los datos

La **ética** en datos implica asegurar consentimiento, transparencia y evitar daños. Pedir **consentimiento informado**, registrar usos permitidos y limitar retención son prácticas básicas. La mitigación de sesgos requiere auditorías de datos, reweighting, re‑sampling y, cuando procede, la generación controlada de datos sintéticos para mejorar representatividad.

La publicación de **model cards** y **datasheets** para datasets ayuda a comunicar limitaciones y riesgos, facilitando auditorías y debate público. En decisiones críticas (crédito, salud, empleo), se recomienda incluir revisión humana y procesos de apelación que permitan corregir errores y garantizar un trato justo.

Ejemplo: sistemas de selección automatizada de personal requieren auditorías regulares; ante disparidades detectadas, las empresas combinan ajustes en el dataset, normalización de características y controles humanos en la decisión final. Herramientas como [Fairlearn](https://fairlearn.org) y las guías de [datasheets](https://arxiv.org/abs/1803.09010) son útiles para estos procesos.

Recursos: [Fairlearn](https://fairlearn.org), [Model Cards](https://modelcards.withgoogle.com/), e indicaciones sobre [DPIA](https://gdpr.eu/data-protection-impact-assessment/) proporcionan marcos y herramientas prácticas.

### Ejemplos, casos, enlaces y tabla resumen 

- Ejemplo: **Model card** resume dataset, métricas y limitaciones para auditar un modelo.
- Caso real: Selección de personal con checks de fairness por subgrupo y revisión humana en decisiones críticas.
- Enlace: [Model Cards](https://modelcards.withgoogle.com/)
- Tabla comparativa rápida:

| Riesgo           | Acción             | Resultado             |
|------------------|--------------------|-----------------------|
| Sesgo en datos   | Reweighting/limpieza| Disparidades menores  |
| Falta de trazabilidad | Documentación | Auditorías más fáciles|
| Daño potencial   | Human‑in‑the‑loop  | Control en casos críticos |

---

## Conceptos clave — Sección 3 (resumen)

- Idea central: sin datos de calidad no hay modelo fiable; prioriza trazabilidad, cobertura y etiquetado reproducible.  
- Flujo esencial: captura → validación automática → limpieza → feature store → versionado → entrenamiento → monitorización.  
- Métricas de calidad de datos a medir: %missing, drift por feature, tasa de outliers, cobertura por subgrupo.  
- Acción inmediata: habilitar tests automáticos (Great Expectations) y versionar snapshots críticos.

---

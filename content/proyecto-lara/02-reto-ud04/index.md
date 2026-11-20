+++
title = "Reto UD04"
weight = 2
+++

---

## Guía

Objetivo: aplicar la IA a la cadena "Moda Urbana LARA" para generar impacto en ventas, operaciones y experiencia de cliente, enlazando con los retos UD01 (digitalización), UD02 (THD) y UD03 (nube).

> Nota: esta UD04 se centra en seleccionar y ejecutar casos de IA con valor empresarial tangible en 3–6 meses. Los apartados marcados como "opcional" son ampliaciones no evaluables.

Qué entregar:

- Tabla de priorización (Valor vs Esfuerzo) y baseline definido para 3 casos (ventas, operaciones, experiencia).
- Mini‑fichas de los 3 casos (objetivo, datos, baseline, método, métrica ML, KPI negocio, riesgos).
- Diagrama de flujo (resumido) del proceso + pipeline/DAG (ASCII o imagen).
- Comparativa baseline vs mejor modelo (tabla con métricas clave y % mejora).
- Evidencias de versionado (MLflow, DVC y dependencias).
- Mini dashboard con 2 KPIs de negocio + 1 métrica técnica.
- Política breve de retraining y fairness.
- Lista de riesgos transversales con acciones preventivas.

Consejos:

- Escribe claro y con ejemplos; mejor simple y completo que técnico y confuso.
- Dibuja cajas y flechas; los dibujos ayudan a entender (ASCII vale).
- Pon nombres reales a herramientas: “MLflow para experimentos”, “DVC para datos”, “Airflow para orquestación”, “Vertex/SageMaker para endpoints”.
- Empieza pequeño (canary) y mide negocio antes de escalar.
- Define un baseline y compáralo siempre con el modelo.

## Objetivo (UD04)

- Identificar tipos de IA y su aplicabilidad en retail de moda (IA débil, ML/DL, RL).
- Conocer el funcionamiento básico de ML (datos → features → entrenamiento → validación → despliegue) y cuándo usar DL.
- Relacionar IA con minería de datos (CRISP‑DM) y analítica para decisiones.
- Evaluar beneficios y riesgos éticos (privacidad, sesgos, explicabilidad).
- Integrar IA con THD y arquitectura en la nube definida en UD03.

## ¿Qué hacer? (UD04)

1. Elegir 3 casos de IA con impacto: uno de ventas (p. ej., recomendador), uno de operaciones (p. ej., previsión de demanda) y uno de experiencia (p. ej., talla recomendada/FAQ bot).
2. Para cada caso, completar mini‑ficha: objetivo, datos, método, métrica ML, KPI negocio, riesgos.
3. Diseñar el flujo reproducible (CRISP‑DM) y el pipeline como DAG (Airflow) con checkpoints.
4. Definir cómo se evalúa y monitoriza (baseline, validación, drift, revisión periódica).
5. Indicar dónde se ejecuta: Edge/Mist/Fog/Nube y servicios de nube (SaaS/PaaS/IaaS/FaaS).

## Casos de uso propuestos

1) Recomendador de outfits (ventas)

- Datos: histórico de compras, navegación, catálogo, tallas.
- Método: modelos de recomendación (matrix factorization / LightFM / embeddings), reglas de negocio.
- Métrica ML: Recall@K / NDCG.
- KPI negocio: Conversión, AOV, CTR en recomendación.
- Riesgos: sesgos por estacionalidad; privacidad; frío‑inicio.

1) Previsión de demanda por tienda (operaciones)

- Datos: ventas por tienda/sku/semana, calendario, clima/eventos.
- Método: regresión con boosting (XGBoost/LightGBM) + features de calendario; baseline naive.
- Métrica ML: MAE/MAPE por tienda.
- KPI negocio: roturas de stock (−%), tasa de sobrestock (−%).
- Riesgos: cambios de catálogo; shocks; datos faltantes.

1) Recomendación de talla (experiencia)

- Datos: devoluciones por talla, medidas de producto, perfiles anónimos.
- Método: clasificación/ordinal + reglas; opcional embeddings.
- Métrica ML: F1 macro / Accuracy balanceada.
- KPI negocio: reducción de devoluciones (−%), NPS (+).
- Riesgos: privacidad y sesgos de cuerpo/género; explicabilidad.

1) Visual Search (búsqueda por imagen)

- Datos: fotos del móvil + catálogo etiquetado.
- Método: modelo de embeddings (CNN/ViT) con ANN (faiss).
- Métrica ML: Recall@K imagen‑a‑producto.
- KPI: conversión desde búsqueda visual, tiempo a encontrar.
- Riesgos: latencia en móvil; cobertura del catálogo.

1) Detección de devoluciones anómalas (fraude)

- Datos: tickets, devoluciones, cliente, tienda, horario.
- Método: anomalías (Isolation Forest) o clasificación con umbral.
- Métrica ML: ROC‑AUC, Recall en top‑N.
- KPI: tasa de fraude detectado, falsos positivos.
- Riesgos: equidad por segmento; escalada a revisión humana.

## Entregables mínimos (UD04)

Lista única de lo imprescindible. Si entregas esto con calidad y coherencia, UD04 está cubierta. Sin fases.

1. Tabla de priorización (Valor vs Esfuerzo) con la decisión de 3 casos y baseline por caso.
2. Mini‑fichas de los 3 casos: objetivo, datos (fuentes), baseline, método propuesto, métrica ML, KPI negocio, 3 riesgos + mitigación.
3. Diagrama de flujo (resumido) del proceso CRISP‑DM + pipeline/DAG (ASCII o imagen) con 2–3 checkpoints.
4. Comparativa baseline vs mejor modelo (1–2 métricas clave y % mejora).
5. Evidencia de versionado: captura MLflow, referencia DVC (.dvc o hash) y lista de dependencias.
6. Mini dashboard piloto (mock si no real): 2 KPIs negocio + 1 métrica técnica con fecha.
7. Política breve (≤1 página) de retraining y fairness.
8. Lista de riesgos transversales (privacidad, sesgos, drift, coste, seguridad) con acción preventiva.

### Notas rápidas por entregable

- Tabla de priorización
  - Qué es: matriz Valor (impacto) vs Esfuerzo (tiempo/recursos) con puntuación 1–5.
  - Criterios: incluye 3 casos seleccionados y baseline definido por caso.
- Mini‑fichas
  - Qué es: ficha por caso con campos obligatorios (objetivo, datos, baseline, método, métrica, KPI, riesgos).
  - Criterios: lenguaje claro, 1 página por ficha como máximo.
- Diagrama de flujo (resumido)
  - Qué es: 6–8 cajas desde datos → features → entrenamiento → validación → despliegue → monitorización.
  - Criterios: legible en 1 página, con 2–3 decisiones (p. ej., “¿mejora ≥10% vs baseline?”).
- Comparativa baseline vs modelo
  - Qué es: tabla con métrica(s) clave y % mejora respecto al baseline.
  - Criterios: datasets y métricas consistentes; dejar constancia del split/periodo.
- Evidencias de versionado
  - Qué es: captura de MLflow (experimentos/métricas), referencia DVC de datos y listado de dependencias.
  - Criterios: permite reproducir el mejor resultado.
- Mini dashboard
  - Qué es: visual simple con 2 KPIs de negocio (p. ej., Conversión, Roturas) + 1 métrica técnica (MAPE/Recall@K).
  - Criterios: fecha/rango visibles; objetivo a 3–6 meses indicado.
- Política de retraining y fairness
  - Qué es: cuándo re‑entrenar, cómo revisar sesgos, qué hacer ante degradación.
  - Criterios: ≤1 página, responsable y cadencia definidos.
- Riesgos transversales
  - Qué es: lista única de riesgos comunes (privacidad, sesgos, drift, coste, seguridad) con prevención, señal y plan de respuesta.
  - Criterios: umbrales claros (p. ej., PSI>0.2, MAPE +5 pt), responsable/cadencia.

## Arquitectura y MLOps (Edge → Mist → Fog → Nube)

- Edge (tienda): kioscos/APP móvil → inferencia ligera (talla/visual search); modo offline básico.
- Mist (gateway): agregación de eventos, colas (MQTT/Kafka ligero), caché.
- Fog (regional): APIs de recomendación, feature store ligero, ANN index.
- Nube: entrenamiento, tracking (MLflow), versionado (DVC), orquestación (Airflow), gobierno/monitorización.

## Riesgos y mitigación (ética y seguridad)

- Privacidad: minimización, anonimización, cifrado en tránsito/reposo, consentimiento.
- Sesgos y fairness: evaluación por segmento; ajustes o umbrales; revisión HITL.
- Drift y calidad: monitorización de datos y desempeño; alertas.
- Coste/lock‑in: empezar con servicios gestionados de bajo coste; portabilidad con ONNX.
- Seguridad: MFA, RBAC por roles, logs/auditoría; pruebas de restore.

## Ejemplos de entregables (UD04)

- Ejemplo de tabla de priorización (Valor vs Esfuerzo) con 3 casos y baseline por caso.
- Mini‑fichas rellenas (3): objetivo, datos, baseline, método, métrica, KPI, riesgos.
- Diagrama de flujo (resumido) en ASCII o imagen del proceso + pipeline.
- Comparativa: baseline vs mejor modelo (tabla con % mejora).
- Evidencias: captura de MLflow y referencia DVC + dependencias.
- Mini dashboard (mock o real): 2 KPIs negocio + 1 métrica técnica con fecha.
- Política breve de retraining y fairness.
- Lista de riesgos transversales con prevención, señal y respuesta.

## Ejemplo de Plantilla de entrega (UD04). No es un modelo, es un ejemplo

Título: IA aplicada a Moda Urbana LARA (UD04)

| Caso | Objetivo | Datos | Método | Métrica ML | KPI negocio | Riesgos |
|---|---|---|---|---|---|---|
| Recomendador outfits | ↑ Conversión y AOV | compras, navegación, tallas | MF/embeddings + reglas | Recall@K/NDCG | Conversión, AOV | privacidad, estacionalidad |
| Demanda por tienda | ↓ Roturas y sobrestock | ventas, calendario, clima | XGBoost/LightGBM | MAE/MAPE | Roturas, sobrestock | cambios catálogo |
| Talla recomendada | ↓ Devoluciones | devoluciones, medidas | clasificador ordinal | F1 macro | % devoluciones, NPS | sesgos, explicabilidad |

## Coherencia con UD01→UD02→UD03

- UD01 → UD04: los datos de inventario/TPV/CRM sustentan los casos de IA (compras, stock, clientes). Las mejoras de UD01 proveen las fuentes de datos.
- UD02 → UD04: los THD seleccionados (IoT, IA, 5G) se concretan ahora en modelos y pipelines de IA con KPIs claros.
- UD03 → UD04: la arquitectura en la nube y seguridad (Edge/Mist/Fog/Nube, MFA, cifrado, backups) habilitan entrenamiento, despliegue y gobierno de IA.

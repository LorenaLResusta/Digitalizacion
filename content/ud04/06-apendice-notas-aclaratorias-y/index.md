+++
title = "Apéndice — Notas aclaratorias y explicaciones simples"
weight = 6
+++

## Notas aclaratorias: Gobernanza en IA

Qué es la gobernanza en IA (breve): conjunto de reglas, responsabilidades y procesos para garantizar que los sistemas de IA sean seguros, justos y auditables. Incluye documentación (model cards), controles de acceso, pruebas previas al despliegue y mecanismos de rollback.

## Técnicas de mitigación

- Mitigación de sesgos: acciones para reducir resultados injustos en modelos. Ejemplos sencillos:
  - Reweighting: dar más peso a ejemplos de grupos infrarrepresentados durante el entrenamiento.
  - Re‑sampling: aumentar o reducir muestras de ciertos grupos para equilibrar clases.
  - Feature cleaning: eliminar o transformar variables sensibles que introduzcan sesgo.
  - Revisión humana: incorporar validación por expertos cuando la decisión es crítica.

Estas técnicas no garantizan eliminación total del sesgo pero reducen su impacto y facilitan auditorías.

## Flujos reproducibles

- ¿Qué es un flujo reproducible? Es un conjunto automatizado de pasos (ingestión, limpieza, entrenamiento, evaluación y despliegue) que se puede ejecutar de forma idéntica en el tiempo para regenerar resultados. Elementos clave:
  - Versionado de datos y código (p. ej. DVC, git)
  - Registro de configuraciones y parámetros (tracking de experimentos: MLflow, W&B)
  - Checkpoints y artefactos almacenados (modelos, transformaciones)
  - Pruebas automáticas y validaciones que bloquean despliegues si algo falla

Un flujo reproducible facilita auditoría, debugging y reentrenamientos controlados.

## Glosario rápido (términos MLOps y despliegue)

- Artefacto entrenado (modelo): archivo(s) con los pesos y la arquitectura del modelo listos para usarse en inferencia.
- Flujo reproducible (antes “pipeline”): una secuencia automatizada de pasos (ingestión → limpieza → entrenamiento → evaluación → despliegue) que puedes repetir y auditar.
- Endpoint de inferencia: servicio web/API que recibe entradas y devuelve predicciones en tiempo real o por lotes (batch).
- Monitorización (del modelo): seguimiento continuo de métricas técnicas (latencia, errores) y de negocio (CTR, conversión) y de salud del modelo (drift de datos/rendimiento).
- Drift (cambio de datos): cuando cambian los datos o su relación con la salida y el modelo empeora; dispara reentrenos o ajustes.
- MLOps: prácticas para llevar modelos a producción de forma fiable (versionado, orquestación, despliegue, monitorización, gobernanza).
- Feature store: catálogo central de variables (features) coherentes entre entrenamiento e inferencia.
- Despliegue canary: liberar la nueva versión del modelo a un 5–10% del tráfico; si mejora, ampliar; si empeora, revertir.
- Blue‑green vs canary: blue‑green cambia 100% entre dos versiones con un “switch”; canary va por porcentajes graduales.
- A/B test vs canary: A/B compara variantes estables para causalidad; canary busca seguridad al introducir una versión nueva.
- CTR (Click‑Through Rate): porcentaje de usuarios que hacen clic entre los que vieron una recomendación o elemento.
- Precision vs recall: precision evita falsos positivos; recall evita falsos negativos (elige según coste de error).
- ROC/AUC: curvas/área para evaluar calidad de un clasificador al variar el umbral.
- Overfitting/underfitting: sobreajuste = aprende el ruido; infraajuste = modelo demasiado simple.
- Congelar capas / entrenar la cabeza: en transfer learning, fijar capas base y entrenar sólo las finales para la nueva tarea.
- Embeddings: vectores que representan elementos (palabras, productos, usuarios) para medir similitud.
- Cuantización/pruning: técnicas para hacer modelos más ligeros y rápidos con mínima pérdida de precisión.
- Alineación (alignment): que los objetivos del sistema de IA coincidan con valores humanos.
- Seguridad en IA: prevenir abusos o fallos peligrosos (ataques adversariales, filtrado de datos sensibles, control de permisos y auditorías).

## Checklist rápido de gobernanza (para equipos)

1. Documentar datasets y modelos (model cards, datasheets).
2. Versionar datos y código.
3. Ejecutar pruebas de fairness y performance antes del despliegue.
4. Implementar monitorización en producción y alertas de drift.
5. Definir responsables y procesos de rollback/appeal para decisiones automatizadas.

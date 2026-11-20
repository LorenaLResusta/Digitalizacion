+++
title = "2. Cómo aprende una IA"
weight = 2
+++

El aprendizaje de una IA se basa en algoritmos que extraen patrones de datos para hacer predicciones o tomar decisiones. Las dos familias principales son el aprendizaje automático (ML) y el aprendizaje profundo (DL).

cómo aprende un modelo

- Datos y objetivo: partimos de ejemplos (X) y, si los hay, etiquetas (y) que representan el resultado deseado.
- Modelo: definimos una función con parámetros ajustables que intenta mapear X → y.
- Pérdida: medimos el error entre la predicción y la realidad con una función de pérdida (loss).
- Optimización: ajustamos los parámetros para minimizar esa pérdida (p. ej., con gradiente/Adam).
- Evaluación: comprobamos el rendimiento con un conjunto de validación y métricas adecuadas al problema.
- Despliegue y operación: servimos el modelo para inferencia y monitorizamos su comportamiento (drift, latencia, coste).

## Ejemplos, casos, enlaces y tabla resumen

Ejemplo  (clasificar spam)

- Objetivo: clasificar correos como spam/no spam.
- Features: palabras (TF‑IDF), presencia de enlaces, frecuencia de remitente.
- Pérdida/métrica: log loss para entrenar; F1/ROC‑AUC para evaluar en datos desbalanceados.
- Trucos prácticos: estratificar la validación, revisar leakage (p. ej., incluir el asunto “SPAM” sin querer), calibrar probabilidades y monitorizar drift del vocabulario.
- Caso real: **YouTube/Google** documentan en su curso de ML prácticas de evaluación y overfitting/underfitting aplicables a múltiples dominios.
- Enlace: [Google ML Crash Course](https://developers.google.com/machine-learning/crash-course) y [Tutorial básico de clasificación (scikit‑learn)](https://scikit-learn.org/stable/tutorial/basic/tutorial.html)
- Tabla comparativa rápida:

| Elemento    | Función                         | Beneficio                 |
|-------------|----------------------------------|---------------------------|
| Datos (X, y) | Materia prima + objetivo         | Señal representativa      |
| Modelo       | Mapea X→y                        | Generaliza patrones       |
| Pérdida      | Mide error                       | Guía la optimización      |
| Evaluación   | Valida rendimiento               | Evita sobreajuste         |

**Resumen:** El aprendizaje en **IA** combina datos representativos, un modelo y un proceso de optimización medido con métricas adecuadas; partir de un baseline y evaluar con validaciones correctas evita falsas mejoras y asegura impacto en el objetivo de negocio.

## 2.1 Aprendizaje automático (machine learning) — fundamentos y ejemplos

El **aprendizaje automático (ML)** se centra en construir modelos estadísticos a partir de datos para tareas como **clasificación**, **regresión** y **clustering**. Los paradigmas principales son **supervisado** (datos etiquetados), **no supervisado** (sin etiquetas), **semi‑supervisado** y **aprendizaje por refuerzo**. Un proyecto ML típico incluye **recolección & limpieza de datos**, ingeniería de features (características), selección de modelos, evaluación, despliegue y monitorización.

Recursos didácticos: la documentación de [Scikit‑learn](https://scikit-learn.org/stable/tutorial/index.html) y el curso de Andrew Ng en Coursera ([Machine Learning](https://www.coursera.org/learn/machine-learning)) son referencias útiles.

Finalmente, la elección del modelo depende de datos y restricciones: con pocos datos tabulares, modelos como Random Forest o XGBoost suelen superar redes profundas, mientras que en imágenes y texto el **transfer learning** y redes profundas dominan. [Hugging Face](https://huggingface.co) y [Fast.ai](https://www.fast.ai) proporcionan recursos prácticos para aplicar estos enfoques.

### Ejemplos, casos, enlaces y tabla resumen — 2.1

- Ejemplo: **Churn** con XGBoost usando features de uso.
- - Caso real: **Credit scoring** con árboles + calibración; explicaciones locales para cumplir regulación.
- Enlace: [Guía de clasificación (scikit‑learn)](https://scikit-learn.org/stable/supervised_learning.html)
- Tabla comparativa rápida:

| Tarea           | Modelo base     | Métrica a vigilar |
|-----------------|-----------------|-------------------|
| Clasificación   | Árboles/XGBoost | F1 / AUC          |
| Regresión       | RandomForest    | MAE / RMSE        |
| Clustering      | K‑means         | Silhouette        |

### Tabla comparativa: algoritmos ML comunes

| Algoritmo | Ventaja principal | Uso típico |
|---|---|---|
| Regresión lineal | Interpretabilidad, rápido | Predicción continua simple |
| Árboles (RF/XGBoost) | Robustez, manejo de no linealidad | Tabular, clasificación |
| SVM | Buen rendimiento con pocos datos | Clasificación en espacios complejos |
| K‑means | Simple y rápido | Clustering/segmentación |
| Naive Bayes | Muy rápido, bueno en texto | Clasificación de texto |

## 2.2 Aprendizaje profundo (deep learning) — redes neuronales y ejemplos prácticos

El **aprendizaje profundo (DL)** emplea redes neuronales con muchas capas para aprender representaciones jerárquicas directamente desde datos crudos, como imágenes, audio o texto. Arquitecturas comunes incluyen **CNNs** para visión, **RNN/LSTM** para secuencias, y **Transformers** para procesamiento de lenguaje natural. El diseño arquitectónico, la elección del optimizador (SGD, Adam) y técnicas de regularización (dropout, weight decay) son determinantes para la convergencia y la generalización.

DL suele requerir grandes cantidades de datos y **capacidad de cómputo** (GPUs/TPUs). Cuando los datos son limitados, es efectivo usar **transfer learning**: partir de un modelo preentrenado (p. ej. ResNet, BERT) y afinarlo en el dominio específico.

Retos técnicos: a veces los gradientes se apagan o se disparan (vanishing/exploding gradients) y el entrenamiento se vuelve inestable. Para estabilizar, se usan trucos de arquitectura como BatchNorm y conexiones residuales, y se ajusta la tasa de aprendizaje (learning rate). Métricas específicas ayudan a elegir y evaluar modelos: IoU (superposición) en segmentación de imágenes y BLEU/ROUGE en traducción y resumen.

En producción, los modelos DL requieren optimizaciones para reducir latencia y coste: **pruning**, **quantization** y compiladores de modelos (TensorRT, ONNX). Ejemplos prácticos incluyen asistentes de voz en teléfonos móviles que emplean modelos optimizados en el edge y soluciones híbridas cloud/edge para equilibrar latencia y precisión.

### Ejemplos, casos, enlaces y tabla resumen — 2.2

- Ejemplo: **Transfer learning** con ResNet en imágenes médicas: se “congelan” las capas base preentrenadas y se entrena solo la “cabeza” (capas finales) para la nueva tarea.
- Caso real: **Reconocimiento de voz** en móvil con modelos comprimidos; se equilibra precisión vs. consumo.
- Enlace: [Tutoriales de PyTorch](https://pytorch.org/tutorials/) y [CS231n](http://cs231n.stanford.edu/)
- Tabla comparativa rápida:

| Caso            | Arquitectura | Truco de entrenamiento |
|-----------------|--------------|------------------------|
| Visión médica   | ResNet/U‑Net | Transfer learning      |
| Texto (PLN)     | Transformers | Fine‑tuning por capas  |
| Audio/voz       | CNN/Transform| Data augmentation      |

Ejemplo real: hospitales ajustan modelos de visión médica con sus propios datos locales. Así mejoran los diagnósticos sin reunir millones de imágenes. Recursos: [CS231n](http://cs231n.stanford.edu/) y [tutoriales de PyTorch](https://pytorch.org/tutorials/).

### Tabla comparativa: ML vs Deep Learning

| Aspecto | ML tradicional | Deep Learning |
|---|---|---|
| Requisitos de datos | Moderados | Altos |
| Necesidad de feature eng. | Alta | Baja |
| Interpretabilidad | Mejor | Menor |
| Infraestructura | Ligera | GPUs/TPUs |
| Rendimiento en visión/PLN | Bueno | Superior |

## 2.3 Ética, fairness y explicabilidad (XAI)

- SHAP: indica cuánto aporta cada característica a una predicción concreta, en positivo o en negativo. Salida típica: barras por característica; valores altos empujan la decisión, bajos la frenan. Útil en datos tabulares y con árboles/boosting.
- LIME: explica "alrededor" de un caso creando pequeñas variaciones y ajustando un modelo sencillo (por ejemplo, lineal) que aproxima al original. Salida típica: lista corta de características con su peso y sentido. Útil cuando SHAP no tiene soporte directo o para una vista rápida.

La explicabilidad (XAI) aporta herramientas para entender y justificar predicciones: **SHAP** y **LIME** permiten explicaciones locales; los modelos interpretable‑by‑design (regresión, árboles pequeños) son preferidos en contextos regulados. En medicina, técnicas como saliency maps se combinan con la revisión clínica para validar hallazgos; en finanzas, los modelos deben producir explicaciones que cumplan requisitos de auditoría. Recursos: [SHAP](https://github.com/slundberg/shap) y [LIME](https://github.com/marcotcr/lime).

En cuanto a privacidad, técnicas como **differential privacy** y **federated learning** reducen la exposición de datos sensibles; Google y Apple han usado variantes de aprendizaje federado en teclados predictivos y mejoras de modelos móviles. Para normativa, revisa [GDPR](https://gdpr.eu/) y guías de privacidad sectoriales.

Finalmente, es recomendable establecer marcos de gobernanza: políticas de consentimiento, evaluaciones de impacto (DPIA), y procesos de revisión humana para decisiones críticas. La combinación de métricas técnicas y auditorías sociales ayuda a mitigar riesgos.

### Ejemplos, casos, enlaces y tabla resumen — 2.3

- Ejemplo: Evaluar **fairness** por subgrupos (género/edad) y aplicar reweighting si hay disparidades.
- Caso real: En **salud**, monitorizar drift de desempeño por hospital/zona para evitar degradación desigual.
- Enlace: [Fairlearn](https://fairlearn.org)
- Tabla comparativa rápida:

| Riesgo        | Métrica         | Mitigación            |
|---------------|-----------------|-----------------------|
| Sesgo         | Demographic Par.| Reweighting/constraints|
| Explicabilidad| SHAP/LIME       | Modelos interpretable |
| Privacidad    | k‑anonymity     | DP, federated learning|

## 2.4 Casos para digitalizar empresas y servicios

Objetivo: ofrecer casos “listos para empezar” en 2–6 semanas para digitalizar procesos con IA de forma práctica y asequible.

Plantilla (contrato mínimo por caso)

- Problema/objetivo: qué impacto de negocio se busca (ahorro, ingresos, calidad).
- Datos mínimos: qué datos hay hoy (CSV/CRM/tickets) y volumen aproximado.
- Modelo/solución: heurística/ML clásico/DL preentrenado/no‑code.
- Métrica de éxito: 1–2 métricas claras (p. ej., F1, MAPE, tiempo medio de respuesta).
- Esfuerzo & herramientas: estimación S/M/L y herramientas concretas.

Casos propuestos (PYME/servicios)

- Caso: Atención al cliente 24/7 (FAQ + búsqueda)
  - Datos mínimos: FAQs, web corporativa, 50–200 preguntas típicas.
  - Solución: chatbot con recuperación (RAG ligero) + intents básicos; sin entrenamiento pesado.
  - Métrica: tasa de autoservicio, CSAT/NPS, desvío de llamadas.
  - Esfuerzo/herramientas: S; Power Virtual Agents/Bot Framework + Azure AI Search/SharePoint + Power Automate.

- Caso: Clasificación y enrutado de tickets/email
  - Datos mínimos: histórico de tickets con 5–10 categorías.
  - Solución: ML clásico (Reg. logística/SVM/Naive Bayes) con TF‑IDF; reglas fallback.
  - Métrica: F1 macro y reducción del tiempo de primera respuesta (FRT).
  - Esfuerzo/herramientas: S; scikit‑learn + Power Automate/Zapier.

- Caso: Priorización de leads (scoring simple)
  - Datos mínimos: CRM con estado de lead, canal, últimas interacciones.
  - Solución: árboles/XGBoost; recalibrar mensualmente.
  - Métrica: lift@k y conversión en top‑segment.
  - Esfuerzo/herramientas: M; scikit‑learn/XGBoost + BI (Power BI/Tableau).

- Caso: Recomendaciones básicas en e‑commerce
  - Datos mínimos: ventas históricas (pedido‑producto), top ventas por categoría.
  - Solución: reglas de asociación/co‑ocurrencia o top‑N por categoría; empezar sin modelo pesado.
  - Métrica: CTR en carruseles y € por sesión.
  - Esfuerzo/herramientas: M; Excel/SQL + plugins de plataforma (Shopify/WooCommerce).

- Caso: Predicción de demanda (versión ligera)
  - Datos mínimos: ventas semanales/diarias por referencia (6–24 meses).
  - Solución: Prophet/ARIMA + suavizado exponencial; actualizar mensual.
  - Métrica: MAPE/MAE y rupturas de stock.
  - Esfuerzo/herramientas: M; Prophet, statsmodels, Power BI.

- Caso: Detección temprana de churn o impagos
  - Datos mínimos: alta/baja, uso, incidencias, pagos.
  - Solución: árboles/GBM con variables de actividad y recencia.
  - Métrica: recall en el decil superior y ROI de retención.
  - Esfuerzo/herramientas: M; scikit‑learn/XGBoost + campañas en CRM.

- Caso: OCR de facturas y extracción de campos
  - Datos mínimos: 100–300 PDFs/escaneos con campos clave.
  - Solución: OCR + modelos NER preentrenados (sin entrenar desde cero).
  - Métrica: F1 de extracción por campo y tasa de revisión humana.
  - Esfuerzo/herramientas: S–M; Azure Document Intelligence/Form Recognizer o Power Automate AI Builder.

- Caso: Monitorizar opiniones (sentimiento y temas)
  - Datos mínimos: reseñas, encuestas, redes (si procede).
  - Solución: análisis de sentimiento/tema preentrenado; dashboard de tendencias.
  - Métrica: F1/accuracy y tiempo de resolución de quejas.
  - Esfuerzo/herramientas: S; Azure Text Analytics/Language Studio + Power BI.

- Caso: Alertas de inventario (stock‑out)
  - Datos mínimos: stock actual, ventas, reposiciones.
  - Solución: regla + umbrales dinámicos con forecast simple.
  - Métrica: % de roturas evitadas y días de inventario.
  - Esfuerzo/herramientas: S; Excel/SQL + Power Automate.

- Caso: Citas y planificación inteligente (agenda)
  - Datos mínimos: agenda, duración por servicio, no‑shows.
  - Solución: predicción de no‑show + reglas para overbooking controlado.
  - Métrica: uso de agenda y cancelaciones.
  - Esfuerzo/herramientas: M; scikit‑learn + calendario/booking API.

### Ejemplos, casos, enlaces y tabla resumen — 2.4

- Enlaces útiles: [scikit‑learn tutoriales](https://scikit-learn.org/stable/tutorial/), [Prophet](https://facebook.github.io/prophet/), [Azure AI Language](https://learn.microsoft.com/azure/ai-services/language-service/), [Document Intelligence](https://learn.microsoft.com/azure/ai-services/document-intelligence/), [Power Automate](https://learn.microsoft.com/power-automate/).
- Tabla resumen (idea → dato → solución → métrica → esfuerzo):

| Caso | Datos mínimos | Solución sugerida | Métrica | Esfuerzo |
|------|---------------|-------------------|---------|----------|
| FAQ bot | FAQs + web | RAG ligero + intents | Autoservicio/CSAT | S |
| Tickets | Tickets categorizados | TF‑IDF + Reg. Log./SVM | F1 macro/FRT | S |
| Leads | CRM básico | Árboles/XGBoost | Lift@k | M |
| Recos | Ventas históricas | Co‑ocurrencia/top‑N | CTR/€ sesión | M |
| Demanda | Ventas (6–24 m) | Prophet/ARIMA | MAPE/MAE | M |
| Churn | Uso + incidencias | GBM | Recall top decil | M |
| Facturas | PDFs | OCR + NER pretrain | F1 extracción | S–M |
| Sentimiento | Reseñas/encuestas | Sentiment pretrain | F1/accuracy | S |
| Stock | Stock + ventas | Reglas + forecast | Roturas evitadas | S |
| Agenda | Historial citas | No‑show + reglas | Uso agenda | M |

---

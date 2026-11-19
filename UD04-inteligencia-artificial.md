---
title: "UD04. Aplicación de la inteligencia artificial"
---

[← UD03](UD03-cloud-y-sistemas-conectados.md) · [Inicio de la asignatura](./) · [UD05 →](UD05-evaluacion-de-datos.md)

# UD04. Aplicación de la inteligencia artificial

| Módulo | Resultado de aprendizaje | Duración orientativa |
|--------|--------------------------|----------------------|
| 1665 · Digitalización aplicada a los sectores productivos (GS) | RA4 | 5 horas |

**RA4.** Identifica aplicaciones de la inteligencia artificial (IA) en el sector y describe las mejoras que aporta su implementación.

<details markdown="1">
<summary><strong>Criterios de evaluación y contenidos de la unidad</strong></summary>

**Criterios de evaluación**

a) Se ha identificado la importancia de la IA en la automatización y optimización de procesos.  
b) Se ha relacionado la IA con la recogida masiva de datos (big data), su análisis y la rentabilidad empresarial.  
c) Se ha valorado la importancia presente y futura de la IA.  
d) Se han identificado los sectores con mayor implantación de IA.  
e) Se han identificado lenguajes de programación utilizados en IA.  
f) Se ha descrito cómo influye la IA en el sector del título.  

**Contenidos**

- IA: concepto y ejemplos de aplicación. Tipos de IA.
- Evolución de la IA.
- IA y datos: protección de datos y minería de datos.
- IA en los sectores productivos y en el título.
- Lenguajes de programación en IA.
- Regulación y principios éticos de la IA.

</details>

## Índice de la unidad
{: .no_toc}

* Índice
{:toc}

---

## Situación de partida: la IA llega a Juniverse Studio

En Juniverse Studio cada persona ha empezado a usar herramientas de IA por su cuenta: una diseñadora genera imágenes de prueba, un comercial redacta correos con un chatbot, el técnico usa un asistente para escribir scripts. La dirección tiene dudas: ¿se están subiendo datos de clientes a servicios externos?, ¿quién es el autor de una imagen generada?, ¿se puede usar la IA para algo más que «escribir textos»?, ¿qué dice la ley?

Por otra parte, la cadena de tiendas de moda (cliente de Juniverse) quiere saber si la IA puede ayudarle a **prever qué prendas va a vender** en cada tienda y a **atender consultas** de clientes fuera de horario.

> **Pregunta guía de la unidad:** ¿qué puede hacer realmente la IA por una empresa, qué no puede hacer y qué normas hay que respetar al usarla?

---

## 1. Inteligencia artificial: concepto y ejemplos

### 1.1 Qué es la IA

La **inteligencia artificial** es la rama de la informática que desarrolla sistemas capaces de realizar tareas que, cuando las hace una persona, requieren inteligencia: percibir, razonar, aprender, comprender el lenguaje, planificar o tomar decisiones.

El Reglamento europeo de IA define un **sistema de IA** como un sistema basado en máquinas que funciona con cierto grado de autonomía y que, a partir de la información que recibe, **infiere** cómo generar resultados (predicciones, contenidos, recomendaciones o decisiones) que pueden influir en entornos físicos o virtuales.

### 1.2 Qué sabe hacer la IA hoy

| Capacidad | Ejemplo cotidiano | Ejemplo empresarial |
|-----------|-------------------|---------------------|
| **Clasificar** | Filtro de spam | Clasificar incidencias de soporte por urgencia |
| **Predecir** | Tiempo estimado de llegada en el GPS | Prever la demanda de un producto |
| **Recomendar** | Series sugeridas en una plataforma | Productos recomendados en una tienda en línea |
| **Reconocer imágenes** | Desbloqueo facial del móvil | Detectar piezas defectuosas en una línea |
| **Procesar lenguaje** | Traductor automático | Resumir contratos, chatbots de atención |
| **Generar contenido** | Crear una imagen a partir de un texto | Borradores de textos, código o material formativo |
| **Optimizar** | Ruta más rápida | Planificar turnos o rutas de reparto |
| **Detectar anomalías** | Aviso del banco por un pago extraño | Detectar fraudes o intrusiones en la red |

### 1.3 IA en la automatización y optimización de procesos

La automatización clásica sigue **reglas fijas** («si pasa A, haz B»). La IA permite automatizar tareas donde las reglas son difíciles de escribir porque dependen de patrones: leer facturas con formatos distintos, decidir si una pieza es defectuosa a partir de una foto o priorizar correos.

Combinada con otras tecnologías, la IA permite:

- **Automatización inteligente**: RPA + IA para procesar documentos sin intervención humana.
- **Optimización**: encontrar la mejor combinación de recursos (turnos, rutas, stock).
- **Mantenimiento predictivo**: anticipar averías analizando datos de sensores.
- **Control de calidad**: inspección visual automática el 100 % de las piezas.

---

## 2. Tipos de IA

### 2.1 IA débil e IA fuerte

| Tipo | Definición | Situación actual |
|------|------------|------------------|
| **IA débil o estrecha** | Resuelve tareas concretas (jugar al ajedrez, traducir, reconocer caras) | Es **toda** la IA que existe hoy, incluidos los grandes modelos de lenguaje |
| **IA fuerte o general (AGI)** | Tendría una inteligencia comparable a la humana en cualquier tarea | No existe; es objeto de investigación y debate |

### 2.2 IA simbólica y subsimbólica

| Enfoque | Cómo funciona | Ejemplo | Ventaja | Inconveniente |
|---------|---------------|---------|---------|---------------|
| **Simbólica** | Representa el conocimiento con reglas y símbolos escritos por personas | Sistemas expertos de diagnóstico de los años 80 | Explicable: se sabe por qué decide | Difícil de escalar; no aprende sola |
| **Subsimbólica** | Aprende patrones a partir de datos (redes neuronales, estadística) | Reconocimiento de voz, visión artificial | Aprende de los datos, maneja problemas complejos | Funciona como «caja negra»; necesita muchos datos |

Hoy se investigan enfoques **híbridos** que combinan ambas.

### 2.3 Machine learning, deep learning e IA generativa

- **Machine learning**: el sistema aprende de ejemplos. Tipos principales:
  - **Supervisado**: aprende con ejemplos etiquetados (correos marcados como spam / no spam).
  - **No supervisado**: busca grupos o patrones sin etiquetas (segmentar clientes por comportamiento).
  - **Por refuerzo**: aprende por prueba y error con recompensas (robots, juegos).
- **Deep learning**: machine learning con redes neuronales profundas.
- **IA generativa**: modelos que **crean contenido nuevo** (texto, imagen, audio, código). Los **grandes modelos de lenguaje** (LLM) son su ejemplo más conocido.

**Idea clave:** IA ⊃ machine learning ⊃ deep learning ⊃ (gran parte de la) IA generativa.

### Autoevaluación (Capítulos 1 y 2)

- ¿Por qué los asistentes conversacionales actuales se consideran IA débil?
- Clasifica como supervisado o no supervisado: *predecir el precio de una vivienda*, *agrupar clientes por hábitos de compra*.
- Da una ventaja de la IA simbólica frente a la subsimbólica.

---

## 3. Evolución de la IA

| Año | Hito |
|-----|------|
| 1950 | Alan Turing propone el «juego de la imitación» (test de Turing) |
| 1956 | Conferencia de Dartmouth: se acuña el término *inteligencia artificial* |
| Años 70 y 80 | Sistemas expertos. Periodos de desencanto y recortes de financiación («inviernos de la IA») |
| 1997 | Deep Blue (IBM) vence al campeón mundial de ajedrez Garri Kaspárov |
| 2012 | Las redes neuronales profundas mejoran de forma espectacular el reconocimiento de imágenes |
| 2016 | AlphaGo (DeepMind) vence a uno de los mejores jugadores de go del mundo |
| 2017 | Se publica la arquitectura *Transformer*, base de los modelos de lenguaje actuales |
| 2022 | La IA generativa conversacional se populariza entre el gran público |
| 2024 | Se aprueba el Reglamento europeo de IA |

**Factores que explican el avance reciente:** enorme cantidad de **datos** disponibles, **capacidad de cálculo** (GPU y nube) y mejores **algoritmos**.

**Importancia presente y futura:** la IA se está incorporando a casi todas las herramientas de trabajo (ofimática, programación, diseño, atención al cliente). Más que sustituir profesiones completas, está cambiando **tareas**: las personas que saben usarla con criterio ganan productividad, y aparecen nuevos perfiles (ingeniería de datos, MLOps, gobierno de la IA).

---

## 4. La IA y los datos

### 4.1 Los datos, combustible de la IA

Un modelo de IA es tan bueno como los datos con los que se entrena. Los problemas de los datos se convierten en problemas del modelo:

- **Datos escasos** → el modelo no generaliza.
- **Datos sesgados** → el modelo discrimina (por ejemplo, un sistema de selección entrenado con contrataciones pasadas puede reproducir sesgos de género).
- **Datos desactualizados** → el modelo deja de acertar cuando cambia la realidad.

### 4.2 IA, big data y rentabilidad

La relación es un círculo: la empresa **recoge datos masivos** (big data) → los **analiza** con IA → obtiene **predicciones y automatizaciones** → mejora decisiones, reduce costes o aumenta ventas → genera **más datos** para seguir mejorando.

**Ejemplo:** la cadena de tiendas usa el histórico de ventas, el tiempo meteorológico y el calendario de festivos para prever la demanda de cada prenda en cada tienda. Si la previsión reduce un 10 % el stock que acaba en rebajas, la mejora de margen puede pagar el proyecto.

### 4.3 Minería de datos

La **minería de datos** (*data mining*) es el proceso de descubrir patrones útiles en grandes conjuntos de datos. Técnicas habituales:

| Técnica | Pregunta que responde | Ejemplo |
|---------|-----------------------|---------|
| **Clasificación** | ¿A qué categoría pertenece? | ¿Este cliente se dará de baja? |
| **Regresión** | ¿Qué valor numérico tendrá? | ¿Cuántas unidades venderemos? |
| **Agrupamiento (clustering)** | ¿Qué grupos naturales hay? | Tipos de clientes |
| **Reglas de asociación** | ¿Qué cosas suelen ir juntas? | Quien compra X suele comprar Y |
| **Detección de anomalías** | ¿Qué es raro? | Transacciones sospechosas |

### 4.4 Protección de datos en proyectos de IA

Cuando un sistema de IA usa **datos personales**, se aplica el RGPD:

- Debe existir una **base legal** para el tratamiento.
- Hay que **informar** a las personas y respetar sus derechos.
- Se aplica la **minimización**: usar solo los datos necesarios.
- Las personas tienen derecho a **no ser objeto de decisiones exclusivamente automatizadas** con efectos jurídicos o significativos (art. 22 RGPD), salvo excepciones.
- Puede ser necesaria una **evaluación de impacto** (EIPD).

**En la práctica:** no se deben introducir datos personales de clientes ni información confidencial en herramientas de IA públicas sin que la empresa lo haya autorizado y haya revisado las condiciones del servicio.

---

## 5. IA en los sectores productivos

### 5.1 Sectores con mayor implantación

Los sectores que más usan IA son los que tienen **muchos datos digitales** y **procesos repetitivos de alto valor**:

| Sector | Aplicaciones destacadas |
|--------|-------------------------|
| **Tecnología y telecomunicaciones** | Gestión de redes, ciberseguridad, asistentes, desarrollo de software |
| **Banca y seguros** | Detección de fraude, análisis de riesgo, atención automatizada |
| **Comercio y marketing** | Recomendaciones, precios dinámicos, previsión de demanda |
| **Industria** | Mantenimiento predictivo, control de calidad, optimización de procesos |
| **Salud** | Apoyo al diagnóstico por imagen, gestión hospitalaria |
| **Logística y transporte** | Optimización de rutas, gestión de almacenes |
| **Energía** | Previsión de producción renovable y de consumo |
| **Agroalimentación** | Agricultura de precisión, riego inteligente |
| **Administración pública** | Gestión de expedientes, atención ciudadana |

### 5.2 Relación entre las THD del sector y la IA

La IA rara vez funciona sola. Se apoya en:

- **IoT**, que aporta los datos del mundo físico.
- **Big data**, que los almacena y prepara.
- **Cloud**, que ofrece capacidad de cálculo para entrenar modelos.
- **Edge**, que ejecuta los modelos cerca de donde se necesitan respuestas inmediatas.
- **Robótica y cobots**, que convierten las decisiones en acciones físicas.
- **Gemelos digitales**, que usan IA para simular y predecir.

### 5.3 La IA y el título

Cada ciclo formativo debe analizar cómo afecta la IA a su sector. Como ejemplo, en el ámbito de la **informática y las comunicaciones** (por ejemplo, el ciclo de Administración de Sistemas Informáticos en Red):

| Área profesional | Uso de la IA |
|------------------|--------------|
| Administración de sistemas | Análisis de registros (*logs*), detección de anomalías, predicción de fallos de disco o saturación |
| Redes | Optimización del tráfico, detección de intrusiones, diagnóstico de incidencias |
| Ciberseguridad | Identificación de malware y phishing, respuesta automatizada a incidentes |
| Soporte técnico | Chatbots de primer nivel, clasificación automática de incidencias, bases de conocimiento |
| Automatización | Generación y revisión de scripts y archivos de configuración, flujos de trabajo con IA (por ejemplo, con herramientas como n8n) |
| Bases de datos | Asistentes que ayudan a escribir consultas, detección de consultas lentas |

**Riesgos profesionales:** confiar en código o configuraciones generadas sin revisarlas, exponer datos sensibles a servicios externos, no comprobar las fuentes.

**Actividad:** adapta esta tabla a otro ciclo que conozcas (administración, comercio, sanidad, mecánica…).

### Autoevaluación (Capítulos 3 a 5)

- Cita los tres factores que explican el avance reciente de la IA.
- ¿Qué técnica de minería de datos usarías para agrupar clientes?
- ¿Por qué no se deben introducir datos de clientes en un chatbot público?
- Explica cómo se combinan IoT, cloud e IA en el mantenimiento predictivo.

---

## 6. Lenguajes de programación en IA

| Lenguaje | Por qué se usa en IA | Bibliotecas o herramientas destacadas |
|----------|---------------------|---------------------------------------|
| **Python** | Sintaxis sencilla y enorme ecosistema; es el más usado | NumPy, pandas, scikit-learn, TensorFlow, PyTorch |
| **R** | Muy orientado a estadística y análisis de datos | tidyverse, caret |
| **Julia** | Alto rendimiento en cálculo científico | Flux.jl |
| **Java / Scala** | Sistemas empresariales y procesamiento distribuido | Apache Spark (MLlib), Deeplearning4j |
| **C++** | Velocidad; base interna de muchas bibliotecas y de la IA en dispositivos | TensorFlow Lite, ONNX Runtime |
| **JavaScript** | IA en el navegador y en aplicaciones web | TensorFlow.js |
| **Lisp y Prolog** | Históricos de la IA simbólica | Sistemas expertos, programación lógica |
| **SQL** | Preparar y consultar los datos que alimentan los modelos | Bases de datos relacionales |

Además, cada vez más soluciones de IA se construyen **sin programar** o con poco código, conectando servicios mediante APIs y plataformas de automatización.

---

## 7. Regulación y ética de la IA

### 7.1 El Reglamento europeo de IA

El **Reglamento (UE) 2024/1689** de inteligencia artificial es la primera ley integral sobre IA del mundo. Se aplica de forma escalonada y clasifica los sistemas **según su riesgo**:

| Nivel de riesgo | Ejemplos | Obligación |
|-----------------|----------|------------|
| **Inaceptable** | Puntuación social de ciudadanos, manipulación que causa daño, reconocimiento de emociones en el trabajo o en centros educativos (salvo excepciones) | **Prohibidos** |
| **Alto** | IA en selección de personal, evaluación educativa, concesión de créditos, infraestructuras críticas | Requisitos estrictos: gestión de riesgos, calidad de datos, documentación, supervisión humana |
| **Limitado (transparencia)** | Chatbots, contenidos generados o manipulados (*deepfakes*) | Informar de que se interactúa con una IA o de que el contenido es artificial |
| **Mínimo** | Filtros de spam, videojuegos | Sin obligaciones específicas |

En España, la **Agencia Española de Supervisión de la Inteligencia Artificial (AESIA)** es el organismo encargado de supervisar su cumplimiento.

### 7.2 IA, protección de datos y derechos de autor

- **Protección de datos**: el RGPD sigue aplicándose a cualquier sistema de IA que trate datos personales (ver apartado 4.4).
- **Derechos de autor**:
  - Entrenar modelos con obras protegidas plantea conflictos; la normativa europea permite a los titulares **reservarse** el uso de sus obras para minería de textos y datos.
  - Los proveedores de modelos de uso general deben respetar esa reserva y publicar un resumen del contenido usado para el entrenamiento.
  - En la mayoría de ordenamientos, incluido el español, la protección por derechos de autor exige una **creación humana**: un contenido generado íntegramente por IA, sin aportación creativa humana, difícilmente está protegido.
  - Quien usa la IA debe comprobar que el resultado no reproduce obras de terceros.

### 7.3 Principios éticos

Los principios más aceptados para una IA fiable (recogidos, por ejemplo, en las directrices del grupo de expertos de la Comisión Europea) son:

1. **Supervisión humana**: la persona debe poder controlar y corregir.
2. **Solidez técnica y seguridad**.
3. **Privacidad y gobernanza de los datos**.
4. **Transparencia y explicabilidad**.
5. **Diversidad, no discriminación y equidad** (evitar sesgos).
6. **Bienestar social y medioambiental**.
7. **Rendición de cuentas**: alguien es responsable de las decisiones.

**En la actividad profesional:** revisar siempre lo que genera la IA, citar su uso cuando corresponda, no presentar como propio un trabajo íntegramente generado y no usarla para engañar o suplantar a otras personas.

### Autoevaluación (Capítulos 6 y 7)

- ¿Por qué Python es el lenguaje más usado en IA?
- ¿En qué nivel de riesgo situarías un sistema de IA que filtra currículos? ¿Qué implica?
- ¿Qué obligación tiene un chatbot de atención al cliente según el Reglamento de IA?
- Explica con un ejemplo el principio de supervisión humana.

---

## Reto profesional: política de uso de IA y caso de aplicación

**Parte A. Política de uso de IA para Juniverse Studio**

Redacta una política interna de una página con:

1. Herramientas de IA autorizadas y para qué usos.
2. Qué datos **nunca** se pueden introducir en herramientas externas.
3. Cómo revisar y validar los resultados.
4. Cuándo hay que indicar que un contenido se ha generado con IA.
5. Persona responsable y canal para consultas.

**Parte B. Caso de aplicación en tu sector**

1. Elige un proceso de una empresa de tu sector que podría mejorar con IA.
2. Describe la situación actual, los datos disponibles y la solución de IA propuesta.
3. Clasifica el sistema según el nivel de riesgo del Reglamento europeo.
4. Estima beneficios (tiempo, coste, calidad) y riesgos (sesgos, privacidad, errores).
5. Indica qué perfil profesional haría falta para implantarlo.

**Entregable:** documento de 3–4 páginas.

---

## Glosario

| Término | Definición |
|---------|------------|
| **IA** | Disciplina que desarrolla sistemas capaces de realizar tareas que requieren inteligencia |
| **IA débil / fuerte** | Especializada en tareas concretas / hipotética inteligencia general |
| **IA simbólica** | Basada en reglas y conocimiento explícito |
| **IA subsimbólica** | Basada en aprender patrones a partir de datos |
| **Machine learning** | Aprendizaje automático a partir de ejemplos |
| **Deep learning** | Aprendizaje con redes neuronales de muchas capas |
| **IA generativa** | IA que crea contenido nuevo |
| **LLM** | Gran modelo de lenguaje |
| **Minería de datos** | Descubrimiento de patrones en grandes conjuntos de datos |
| **Sesgo** | Error sistemático que hace que un modelo trate de forma injusta a determinados grupos |
| **Explicabilidad** | Capacidad de entender por qué un sistema de IA toma una decisión |
| **AESIA** | Agencia Española de Supervisión de la Inteligencia Artificial |

## Preguntas de repaso

1. Define IA con tus palabras y pon tres ejemplos de uso empresarial.
2. ¿Qué diferencia hay entre automatización clásica y automatización con IA?
3. ¿Qué es un «invierno de la IA»?
4. ¿Por qué unos datos sesgados producen un modelo sesgado?
5. Cita dos prácticas prohibidas por el Reglamento europeo de IA.
6. ¿Qué lenguaje elegirías para un primer proyecto de IA y por qué?

## Enlaces para ampliar

- [Reglamento (UE) 2024/1689 de Inteligencia Artificial (EUR-Lex)](https://eur-lex.europa.eu/eli/reg/2024/1689/oj?locale=es) – Texto oficial.
- [AESIA](https://aesia.digital.gob.es/) – Agencia Española de Supervisión de la IA.
- [AEPD – Inteligencia artificial](https://www.aepd.es/) – Guías sobre IA y protección de datos.
- [Elements of AI](https://www.elementsofai.com/es/) – Curso gratuito de introducción a la IA, en español.

---

[← UD03](UD03-cloud-y-sistemas-conectados.md) · [Inicio de la asignatura](./) · [UD05 →](UD05-evaluacion-de-datos.md)

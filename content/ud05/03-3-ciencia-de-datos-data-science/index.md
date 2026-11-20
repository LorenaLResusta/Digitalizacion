+++
title = "3. Ciencia de datos (Data Science)"
weight = 3
+++

## 3.1. ¿Qué es la ciencia de datos?

La **ciencia de datos** es un campo interdisciplinar que utiliza métodos científicos, procesos y algoritmos para extraer conocimiento tanto de datos estructurados como no estructurados. No se trata de una disciplina aislada, sino de la intersección vital entre tres grandes áreas: las **matemáticas y estadística**, que aportan el rigor necesario para modelar, calcular probabilidades y encontrar patrones ocultos; las **ciencias de la computación**, que proveen la infraestructura y capacidad de programación para manejar grandes volúmenes de información; y el **conocimiento del negocio**, fundamental para formular las preguntas adecuadas e interpretar los resultados en un contexto que aporte valor real a la organización.

## 3.2. El ciclo de vida de un proyecto de datos

Un proyecto típico de ciencia de datos sigue un ciclo estructurado que consta de varias fases clave:
- **Definición del objetivo de negocio**
- **Recopilación y preparación de datos**
- **Selección y modelado**
- **Validación**
- **Interpretación y despliegue**
  
Todo proyecto de ciencia de datos comienza inevitablemente con una pregunta. La fase inicial es la **definición del objetivo de negocio**, donde se busca traducir un problema real (por ejemplo, detectar qué clientes tienen probabilidad de abandonar la compañía) en una pregunta analítica concreta. 

Una vez claro el objetivo, comienza la etapa más laboriosa, a menudo consumiendo la mayor parte del tiempo del proyecto: la **recopilación y preparación** (*data wrangling*). En dicha fase se conectan las diversas fuentes de datos (bases de datos, APIs, sensores) y se realiza una limpieza exhaustiva para corregir errores, homogeneizar formatos y validar la calidad de la información.

Con los datos listos y depurados, se procede a la **selección y modelado**. En este punto, el equipo técnico elige los algoritmos más adecuados (regresión, clasificación, agrupamiento, etc.) y los "entrena" utilizando datos históricos para que aprendan a reconocer patrones. 

Tras el entrenamiento, es crucial la fase de **validación**, donde se pone a prueba el modelo con datos nuevos que nunca ha visto antes para asegurar que sus predicciones son fiables y no fruto del azar. 

Finalmente, el ciclo se cierra con la **interpretación y despliegue**, momento en el que los resultados matemáticos se traducen en acciones de negocio o se integran en sistemas de producción para automatizar la toma de decisiones.

## 3.3. Perfiles profesionales y herramientas del ecosistema

El tratamiento profesional de los datos requiere roles especializados que colaboran estrechamente como en una cadena de montaje digital. El **Ingeniero de Datos** (*Data Engineer*) actúa como el arquitecto que construye y mantiene la infraestructura y las "tuberías" por las que fluyen los datos, asegurando que la información llegue limpia, segura y accesible a los repositorios. Sobre esa base sólida trabaja el **Científico de Datos** (*Data Scientist*), un perfil con fuerte base matemática que aplica algoritmos avanzados y aprendizaje automático para construir modelos predictivos complejos. Complementando este trabajo se encuentra el **Analista de Datos** (*Data Analyst*), quien se enfoca en explorar la información histórica para responder preguntas de negocio inmediatas y comunicar los hallazgos mediante informes y visualizaciones claras.

Para llevar a cabo estas tareas, estos profesionales se apoyan mayoritariamente en lenguajes de programación versátiles como **Python** (con librerías especializadas como Pandas o Scikit-learn) y **R**, que se han convertido en el estándar de la industria. Además, cuando el volumen de datos es masivo, es imprescindible el uso de plataformas de procesamiento distribuido como **Apache Spark** o **Hadoop**, así como herramientas de entorno visual (como KNIME o RapidMiner) que facilitan el diseño de flujos de datos y el prototipado rápido de soluciones analíticas.

<a id="analisis-datos"></a>

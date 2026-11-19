---
title: "UD05. Evaluación de datos"
---

[← UD04](UD04-inteligencia-artificial.md) · [Inicio de la asignatura](./) · [UD06 →](UD06-proyecto-transformacion-digital.md)

# UD05. Evaluación de datos

| Módulo | Resultado de aprendizaje | Duración orientativa |
|--------|--------------------------|----------------------|
| 1665 · Digitalización aplicada a los sectores productivos (GS) | RA5 | 4 horas |

**RA5.** Evalúa la importancia de los datos y su protección en una economía digital globalizada, definiendo sistemas de seguridad y ciberseguridad.

<details markdown="1">
<summary><strong>Criterios de evaluación y contenidos de la unidad</strong></summary>

**Criterios de evaluación**

a) Se ha diferenciado entre dato e información.  
b) Se ha descrito el ciclo de vida del dato.  
c) Se ha identificado la relación entre big data, análisis de datos, machine learning, deep learning e IA.  
d) Se han descrito las características que definen el big data.  
e) Se han descrito las etapas de la ciencia de datos y su papel en el proceso.  
f) Se han descrito los procedimientos de almacenamiento de datos en la cloud.  
g) Se ha descrito la importancia del cloud computing.  
h) Se han identificado los objetivos principales de la ciencia de datos en las empresas.  
i) Se ha valorado la importancia de la seguridad y su regulación en relación con los datos.  

**Contenidos**

- Dato frente a información.
- Ciclo de vida del dato.
- Análisis de datos.
- Almacenamiento de datos en la nube.
- Etapas de la ingeniería de datos.
- Aplicación de la ciencia de datos en las empresas.
- Importancia de la seguridad en el manejo de datos.

</details>

## Índice de la unidad
{: .no_toc}

* Índice
{:toc}

---

## Situación de partida: los datos de Juniverse Studio

Juniverse Studio ya trabaja en la nube y quiere empezar a usar IA, pero al preparar el primer proyecto descubre un problema: **sus datos están dispersos y no son fiables**. Hay clientes repetidos con nombres escritos de tres formas distintas, las horas de producción se apuntan cuando alguien se acuerda, las encuestas de satisfacción están en formularios distintos cada año y nadie sabe cuánto tiempo hay que conservar los datos de los alumnos de los cursos.

Además, la cadena de tiendas de moda ha sufrido un intento de **ransomware** en una de sus tiendas y pide a Juniverse que su plataforma de formación cumpla unos requisitos mínimos de seguridad.

> **Pregunta guía de la unidad:** ¿cómo se convierte un montón de datos en información útil para decidir, y cómo se protege durante todo el camino?

---

## 1. Dato frente a información

### 1.1 De los datos a la sabiduría

| Nivel | Qué es | Ejemplo |
|-------|--------|---------|
| **Dato** | Hecho o valor aislado, sin contexto | `37` |
| **Información** | Datos organizados y con contexto que responden a una pregunta | «37 alumnos abandonaron el curso de ofimática en el módulo 3» |
| **Conocimiento** | Información interpretada que permite comprender | «El módulo 3 es demasiado largo; los abandonos se concentran en el vídeo de 40 minutos» |
| **Sabiduría (decisión)** | Aplicar el conocimiento para actuar | «Dividimos ese vídeo en cuatro de 10 minutos y medimos de nuevo» |

Esta escala se conoce como **pirámide DIKW** (*Data, Information, Knowledge, Wisdom*).

### 1.2 Tipos de datos

| Tipo | Descripción | Ejemplos |
|------|-------------|----------|
| **Estructurados** | Organizados en filas y columnas con un esquema fijo | Tablas de una base de datos, hojas de cálculo |
| **Semiestructurados** | Con cierta organización, pero flexible | JSON, XML, correos electrónicos |
| **No estructurados** | Sin formato predefinido | Vídeos, imágenes, audios, documentos de texto libre |

Se estima que la mayor parte de los datos que se generan hoy son **no estructurados**, lo que exige herramientas específicas para analizarlos.

### 1.3 Calidad del dato

Un dato es de calidad cuando es **exacto**, **completo**, **coherente** entre sistemas, **actualizado**, **válido** (respeta el formato esperado) y **único** (sin duplicados). Datos de mala calidad producen decisiones malas: es el principio *garbage in, garbage out* («si entra basura, sale basura»).

---

## 2. Ciclo de vida del dato

El dato atraviesa varias fases desde que se crea hasta que se elimina. En cada una hay decisiones técnicas y obligaciones legales.

| Fase | Qué ocurre | Ejemplo en Juniverse Studio | Aspecto de seguridad |
|------|------------|------------------------------|----------------------|
| **1. Creación o captura** | El dato se genera o se recoge | Un alumno se matricula en un curso | Recoger solo lo necesario (minimización) e informar |
| **2. Almacenamiento** | Se guarda en un sistema | Base de datos de la plataforma en la nube | Cifrado, control de accesos, copias de seguridad |
| **3. Procesamiento y uso** | Se limpia, transforma y utiliza | Se calcula el progreso del alumno | Acceso solo a quien lo necesita |
| **4. Compartición** | Se envía a otros sistemas o personas | Se envía el certificado a la empresa que paga el curso | Transmisión cifrada, acuerdos con terceros |
| **5. Archivo** | Se conserva sin uso activo | Histórico de alumnos de cursos anteriores | Plazos de conservación definidos |
| **6. Destrucción** | Se elimina de forma segura | Borrado de datos cuando vence el plazo | Borrado irreversible y registro de la eliminación |

**Idea clave:** un dato que ya no se necesita es un **riesgo sin beneficio**. Conservarlo «por si acaso» aumenta el impacto de una posible brecha.

---

## 3. Big data, análisis de datos e IA

### 3.1 Las características del big data: las «V»

| V | Significado | Ejemplo |
|---|-------------|---------|
| **Volumen** | Cantidades enormes de datos | Millones de transacciones de una cadena de tiendas |
| **Velocidad** | Se generan y deben procesarse muy deprisa | Datos de sensores cada segundo |
| **Variedad** | Formatos muy distintos | Ventas, imágenes de cámaras, opiniones en redes sociales |
| **Veracidad** | Fiabilidad y calidad de los datos | Datos duplicados o erróneos que hay que depurar |
| **Valor** | Utilidad real para el negocio | Que el análisis permita decidir mejor |

Las tres primeras son las «V» clásicas; veracidad y valor se añadieron después. Algunos autores incluyen otras, como la **variabilidad** o la **visualización**.

### 3.2 Tipos de análisis de datos

| Tipo | Pregunta | Ejemplo |
|------|----------|---------|
| **Descriptivo** | ¿Qué ha pasado? | Ventas del último trimestre por tienda |
| **Diagnóstico** | ¿Por qué ha pasado? | Las ventas bajaron por la rotura de stock de dos tallas |
| **Predictivo** | ¿Qué va a pasar? | Previsión de ventas para la próxima campaña |
| **Prescriptivo** | ¿Qué debemos hacer? | Cuántas unidades enviar a cada tienda para maximizar el margen |

### 3.3 Relación entre big data, análisis, machine learning, deep learning e IA

- El **big data** aporta la materia prima: grandes volúmenes de datos.
- El **análisis de datos** los explora y resume (estadística, visualización).
- El **machine learning** aprende patrones de esos datos para predecir o clasificar.
- El **deep learning** es machine learning con redes neuronales profundas, útil con imágenes, audio y texto.
- La **IA** es el campo general que usa todas estas técnicas para construir sistemas «inteligentes».

**Resumen:** sin datos no hay IA; sin análisis, los datos no dicen nada; y sin una pregunta de negocio clara, ninguna de las dos cosas aporta valor.

### Autoevaluación (Capítulos 1 a 3)

- Clasifica: *una fila de una tabla de clientes*, *un vídeo de un curso*, *un archivo JSON con pedidos*.
- ¿En qué fase del ciclo de vida se decide cuánto tiempo se conserva un dato?
- Explica la «V» de veracidad con un ejemplo.
- ¿Qué tipo de análisis responde a «¿qué debemos hacer?»?

---

## 4. Almacenamiento de datos en la nube

### 4.1 Tipos de almacenamiento

| Tipo | Cómo organiza los datos | Uso típico | Ejemplos de servicios |
|------|-------------------------|------------|----------------------|
| **De archivos** | Carpetas y archivos, como en un disco | Documentos compartidos | Unidades compartidas, servicios de archivos en red |
| **De bloques** | Bloques de tamaño fijo, como un disco duro virtual | Discos de máquinas virtuales y bases de datos | Discos de servidores en la nube |
| **De objetos** | Objetos con identificador y metadatos, en «contenedores» o *buckets* | Copias de seguridad, vídeos, imágenes, datos para análisis | Amazon S3, Azure Blob Storage, Google Cloud Storage |

### 4.2 Bases de datos y repositorios de datos

| Sistema | Para qué sirve |
|---------|----------------|
| **Base de datos relacional (SQL)** | Datos estructurados y transacciones (pedidos, facturas, matrículas) |
| **Base de datos NoSQL** | Datos flexibles o con gran volumen (catálogos, sesiones, datos de sensores) |
| **Data warehouse (almacén de datos)** | Datos limpios y estructurados de varias fuentes, preparados para informes |
| **Data lake (lago de datos)** | Datos en bruto de cualquier formato, para análisis y entrenamiento de IA |
| **Data lakehouse** | Combina la flexibilidad del lago con la organización del almacén |

### 4.3 Procedimientos de almacenamiento en la nube

1. **Clasificar los datos** según su sensibilidad (públicos, internos, confidenciales, datos personales).
2. **Elegir la ubicación** (región del proveedor). Si hay datos personales, preferir la UE o asegurarse de que la transferencia internacional cumple el RGPD.
3. **Elegir la clase de almacenamiento** según la frecuencia de uso:
   - *Caliente*: acceso frecuente, más caro.
   - *Frío* o *archivo*: acceso ocasional, mucho más barato, con recuperación más lenta.
4. **Aplicar cifrado** en reposo y en tránsito.
5. **Configurar permisos** con el principio de **mínimo privilegio** y revisar que nada sea público por error.
6. **Activar versionado y copias de seguridad**, siguiendo la regla **3-2-1**: 3 copias, en 2 soportes distintos, 1 fuera de la ubicación principal (y, a ser posible, una copia inmutable o desconectada frente al ransomware).
7. **Definir políticas de ciclo de vida**: mover automáticamente a almacenamiento frío y borrar cuando vence el plazo.
8. **Monitorizar** accesos y costes.

### 4.4 Importancia del cloud computing para los datos

La nube ha hecho accesible a cualquier empresa lo que antes solo tenían las grandes: almacenamiento prácticamente ilimitado, capacidad de cálculo para analizar grandes volúmenes, servicios de IA listos para usar y pago por uso. Sin la nube, el big data y la IA estarían fuera del alcance de la mayoría de las pymes. (Repasa la [UD03](UD03-cloud-y-sistemas-conectados.md).)

---

## 5. Ingeniería de datos y ciencia de datos

### 5.1 Etapas de la ingeniería de datos

La **ingeniería de datos** construye los «tubos» por los que circulan los datos (*pipelines*):

| Etapa | Qué se hace |
|-------|-------------|
| **1. Ingesta** | Recoger datos de las fuentes: bases de datos, APIs, archivos, sensores |
| **2. Almacenamiento** | Guardarlos en el repositorio adecuado (lago, almacén, base de datos) |
| **3. Transformación** | Limpiar, unificar formatos, eliminar duplicados, enriquecer (procesos **ETL** o **ELT**: extraer, transformar y cargar) |
| **4. Orquestación** | Programar y encadenar los procesos para que se ejecuten automáticamente |
| **5. Servicio** | Poner los datos a disposición de informes, cuadros de mando o modelos de IA |
| **6. Gobierno y calidad** | Documentar, controlar accesos y vigilar la calidad |

### 5.2 Etapas de la ciencia de datos

La **ciencia de datos** usa esos datos para responder preguntas. Un proceso típico:

1. **Entender el negocio**: ¿qué problema queremos resolver?
2. **Obtener los datos.**
3. **Preparar los datos**: limpieza y transformación (suele llevar la mayor parte del tiempo).
4. **Explorar**: estadística descriptiva y gráficos para descubrir patrones.
5. **Modelar**: aplicar técnicas estadísticas o de machine learning.
6. **Evaluar**: ¿el modelo responde bien a la pregunta inicial?
7. **Comunicar y desplegar**: informes, cuadros de mando o integración en una aplicación.
8. **Mantener**: vigilar que el modelo siga funcionando con datos nuevos.

| Perfil | Papel |
|--------|-------|
| **Ingeniería de datos** | Construye y mantiene la infraestructura y los flujos de datos |
| **Análisis de datos** | Explora, crea informes y cuadros de mando |
| **Ciencia de datos** | Crea modelos predictivos y responde preguntas complejas |
| **Ingeniería de ML / MLOps** | Lleva los modelos a producción y los mantiene |

### 5.3 Objetivos de la ciencia de datos en la empresa

- **Conocer mejor al cliente**: segmentación, personalización, prevención de bajas.
- **Optimizar operaciones**: previsión de demanda, rutas, inventarios, turnos.
- **Reducir riesgos**: detección de fraude, mantenimiento predictivo, ciberseguridad.
- **Crear nuevos productos y servicios** basados en datos.
- **Tomar decisiones basadas en evidencias** en lugar de en intuiciones.

**Ejemplo en Juniverse Studio:** analizar en qué minuto abandonan los alumnos los vídeos para rediseñar los cursos, y prever qué temas tendrán más demanda el próximo trimestre.

### Autoevaluación (Capítulos 4 y 5)

- ¿Qué tipo de almacenamiento elegirías para guardar los vídeos de los cursos? ¿Por qué?
- Explica la regla 3-2-1.
- ¿Qué diferencia hay entre un data lake y un data warehouse?
- ¿Cuál suele ser la etapa que más tiempo consume en un proyecto de ciencia de datos?

---

## 6. Seguridad y regulación en el manejo de datos

### 6.1 Principios de seguridad

La seguridad de la información se apoya en la tríada **CIA**:

- **Confidencialidad**: solo acceden las personas autorizadas.
- **Integridad**: los datos no se alteran sin autorización.
- **Disponibilidad**: los datos están accesibles cuando se necesitan.

Se suelen añadir **autenticidad** (saber quién es quién) y **trazabilidad** (saber quién hizo qué y cuándo).

### 6.2 Amenazas más habituales

| Amenaza | Descripción | Medida principal |
|---------|-------------|------------------|
| **Phishing** | Engaños para robar credenciales o instalar malware | Formación y doble factor de autenticación |
| **Ransomware** | Cifra los datos y pide un rescate | Copias de seguridad aisladas, actualizaciones, segmentación |
| **Robo o filtración de datos** | Acceso no autorizado y publicación o venta | Cifrado, mínimo privilegio, monitorización |
| **Errores de configuración** | Almacenamiento en la nube abierto al público por error | Revisiones periódicas y herramientas de auditoría |
| **Amenaza interna** | Empleados que filtran o borran datos | Control de accesos, registros, salida ordenada de empleados |
| **Pérdida de dispositivos** | Portátiles o móviles extraviados | Cifrado de discos y borrado remoto |

### 6.3 Medidas de ciberseguridad básicas para una pyme

1. Inventario de equipos, servicios y datos.
2. Contraseñas robustas, gestor de contraseñas y **doble factor** en todos los servicios.
3. Actualizaciones automáticas de sistemas y aplicaciones.
4. Copias de seguridad 3-2-1 y **pruebas de restauración** periódicas.
5. Cuentas con el mínimo privilegio y sin compartir usuarios.
6. Cifrado de dispositivos y comunicaciones.
7. Formación periódica del personal.
8. Plan de respuesta ante incidentes: qué hacer, a quién avisar, cómo recuperar.

### 6.4 Marco legal

| Norma | Qué regula |
|-------|-----------|
| **RGPD** (Reglamento UE 2016/679) | Protección de datos personales en toda la UE: principios, derechos, obligaciones y sanciones |
| **LOPDGDD** (Ley Orgánica 3/2018) | Adapta el RGPD a España y añade derechos digitales |
| **Directiva NIS2** (UE 2022/2555) | Ciberseguridad de entidades esenciales e importantes de sectores críticos |
| **Esquema Nacional de Seguridad (ENS)** | Seguridad de los sistemas de la Administración pública española y de sus proveedores |
| **Reglamento de IA** (UE 2024/1689) | Requisitos de calidad y gobierno de datos para sistemas de IA de alto riesgo |

**Principios del RGPD** que debe conocer cualquier profesional: licitud, lealtad y transparencia; limitación de la finalidad; minimización; exactitud; limitación del plazo de conservación; integridad y confidencialidad; y responsabilidad proactiva.

**Brechas de datos personales:** si suponen un riesgo para las personas, hay que notificarlas a la **AEPD** en un máximo de **72 horas** y, si el riesgo es alto, informar también a los afectados.

### Autoevaluación (Capítulo 6)

- ¿Qué elemento de la tríada CIA ataca principalmente el ransomware?
- Cita tres principios del RGPD.
- ¿Por qué es importante probar la restauración de las copias de seguridad?
- ¿Qué plazo hay para notificar una brecha de datos personales a la AEPD?

---

## Reto profesional: plan de datos de Juniverse Studio

**Objetivo:** diseñar cómo gestionará Juniverse Studio los datos de su plataforma de cursos.

**Tareas:**

1. **Inventario de datos**: lista al menos ocho tipos de datos que maneja la plataforma (alumnos, progreso, pagos, vídeos, encuestas…) y clasifícalos por tipo (estructurado, semiestructurado, no estructurado) y por sensibilidad.
2. **Ciclo de vida**: para dos de ellos (uno personal y otro no), describe qué ocurre en cada fase del ciclo de vida y cuánto tiempo se conservan.
3. **Almacenamiento**: decide dónde se guarda cada tipo de dato en la nube (objetos, base de datos, almacén…) y con qué clase de almacenamiento.
4. **Pregunta de negocio**: plantea una pregunta que los datos podrían responder y describe las etapas de ciencia de datos que seguirías.
5. **Seguridad**: propón cinco medidas concretas de seguridad y relaciona cada una con una amenaza.
6. **Cumplimiento**: indica qué obligaciones del RGPD afectan a la plataforma.

**Práctica opcional con datos reales:** descarga un conjunto de datos abiertos del portal [datos.gob.es](https://datos.gob.es/), límpialo con una hoja de cálculo (duplicados, formatos, valores vacíos) y crea un pequeño cuadro de mando con tres indicadores.

**Entregable:** documento de 3–4 páginas.

---

## Glosario

| Término | Definición |
|---------|------------|
| **Dato** | Valor o hecho aislado sin contexto |
| **Información** | Datos organizados con contexto que responden a una pregunta |
| **Ciclo de vida del dato** | Fases por las que pasa un dato desde su creación hasta su destrucción |
| **Big data** | Datos con gran volumen, velocidad y variedad, y técnicas para tratarlos |
| **ETL / ELT** | Procesos de extraer, transformar y cargar datos |
| **Data lake** | Repositorio de datos en bruto de cualquier formato |
| **Data warehouse** | Repositorio de datos limpios y estructurados para análisis |
| **Almacenamiento de objetos** | Almacenamiento en la nube por objetos con identificador y metadatos |
| **Regla 3-2-1** | Tres copias, dos soportes distintos, una fuera de la ubicación principal |
| **Tríada CIA** | Confidencialidad, integridad y disponibilidad |
| **Brecha de datos** | Incidente que provoca la pérdida, alteración o acceso no autorizado a datos |
| **Minimización** | Principio que obliga a tratar solo los datos personales necesarios |

## Preguntas de repaso

1. Pon un ejemplo propio de dato, información y conocimiento.
2. ¿Por qué conservar datos innecesarios es un riesgo?
3. Explica las cinco «V» del big data.
4. ¿Qué diferencia hay entre análisis predictivo y prescriptivo?
5. ¿Qué es una política de ciclo de vida en el almacenamiento en la nube?
6. Cita dos normas que regulan la seguridad de los datos y qué ámbito cubre cada una.

## Enlaces para ampliar

- [AEPD](https://www.aepd.es/) – Guías del RGPD, herramienta *Facilita* y notificación de brechas.
- [INCIBE – Protege tu empresa](https://www.incibe.es/empresas) – Recursos de ciberseguridad para pymes.
- [datos.gob.es](https://datos.gob.es/) – Catálogo de datos abiertos de España.
- [Directiva NIS2 (EUR-Lex)](https://eur-lex.europa.eu/eli/dir/2022/2555/oj?locale=es) – Texto oficial.

---

[← UD04](UD04-inteligencia-artificial.md) · [Inicio de la asignatura](./) · [UD06 →](UD06-proyecto-transformacion-digital.md)

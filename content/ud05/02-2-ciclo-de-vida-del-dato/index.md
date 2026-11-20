+++
title = "2. Ciclo de vida del dato"
weight = 2
+++

El dato no es un elemento estático, sino un activo dinámico que fluye a través de la organización. Desde el instante en que nace en un sensor o una aplicación hasta que finalmente se archiva o elimina, atraviesa una serie de etapas críticas. Gestionar correctamente este ciclo vital es lo que diferencia a una empresa que simplemente almacena “muchos datos” de una organización verdaderamente **data-driven**, capaz de extraer valor real de su información.

## Tabla resumen: ciclo de vida del dato

| Fase | Nombre de la Etapa | Descripción | Actividades Clave | Herramientas o Ejemplos | Objetivo Principal |
|---:|---|---|---|---|---|
| 1 | Generación y recopilación (ingesta) | Captura de la realidad identificando y absorbiendo información de todas las fuentes relevantes para crear un flujo de materia prima digital. | Identificación de fuentes<br>Captura de datos estructurados, no estructurados y semiestructurados<br>Digitalización en tiempo real | ERPs<br>CRMs<br>Logs de servidores<br>Sensores IoT<br>GPS<br>Ejemplo de Tesla (datos de conducción) | Convertir el flujo constante de datos del mundo físico y digital en materia prima disponible para la organización. |
| 2 | Preprocesamiento y limpieza (preparación) | Tratamiento de los datos en bruto para eliminar imperfecciones, errores o duplicados que puedan contaminar análisis posteriores. | Limpieza y depuración<br>Normalización<br>Estandarización de formatos (fechas, divisas)<br>Gestión de valores atípicos (outliers) | Plataformas como Airbnb (depuración de reservas para evitar fraudes). | Asegurar una base sólida y de calidad evitando que entre “basura” al sistema (*garbage in, garbage out*). |
| 3 | Almacenamiento y gestión | Conservación eficiente de los datos limpios utilizando arquitecturas escalables y flexibles. | Organización de datos en repositorios<br>Escalado de capacidad elástica<br>Gestión de infraestructuras en la nube | Data Lake<br>Data Warehouse<br>AWS S3<br>Microsoft Azure<br>Google Cloud | Mantener los datos accesibles y organizados según su nivel de refinamiento para su consumo posterior. |
| 4 | Análisis y modelado | Transformación de la materia prima almacenada en conocimiento mediante inteligencia matemática y algoritmos. | Entrenamiento de modelos de Machine Learning<br>Descubrimiento de patrones ocultos (minería de datos)<br>Iteración y mejora continua | Algoritmos de aprendizaje automático<br>Técnicas de minería de datos | Extraer conocimiento y reglas complejas que son invisibles al análisis tradicional o a la intuición humana. |
| 5 | Interpretación, visualización y uso | Traducción de la complejidad matemática a un lenguaje de negocio claro y accionable para los tomadores de decisiones. | Creación de cuadros de mando<br>Generación de gráficos intuitivos<br>Ejecución de acciones basadas en predicciones | Power BI<br>Tableau<br>Mantenimiento preventivo<br>Ofertas personalizadas | Habilitar la toma de decisiones informada y transformar indicadores en acciones concretas de negocio. |
| 6 | Gobernanza, archivado y borrado | Gestión de la responsabilidad corporativa, protección legal de los datos y su ciclo final de vida. | Cumplimiento normativo (RGPD)<br>Anonimización<br>Ciberseguridad<br>Archivado en almacenamiento frío<br>Borrado seguro | Protocolos de acceso<br>Normativas de privacidad<br>Procesos de destrucción de datos | Garantizar privacidad, ética y eficiencia legal reduciendo costes y riesgos asociados al almacenamiento. |

## 2.1. Fase 1: generación y recopilación (ingesta)

Todo comienza con la captura de la realidad. En esta primera fase, conocida como ingesta, la organización despliega sus redes para identificar y absorber información de todas las fuentes relevantes, creando un flujo constante de "materia prima" digital.

- **Fuentes internas corporativas:** Son los datos que la propia empresa genera en su operación diaria, provenientes de sistemas transaccionales como ERPs (planificación de recursos), CRMs (gestión de clientes) o los registros técnicos (logs) de sus servidores.
- **Fuentes externas y ecosistema IoT:** Gracias a la hiperconectividad, los sensores conectados actúan como los sentidos de la organización, capturando datos del mundo físico —como temperatura, ubicación GPS o vibraciones de maquinaria— y digitalizándolos en tiempo real.
- **Variedad de formatos:** La ingesta no discrimina; acepta datos estructurados en tablas, pero también debe manejar el caos de los datos no estructurados (vídeos, textos libres) y semiestructurados, integrándolos en un flujo común.

> **Ejemplo:** Tesla no solo fabrica coches, sino que recopila millones de kilómetros de datos de conducción real de su flota para entrenar continuamente sus sistemas de asistencia y conducción autónoma.

## 2.2. Fase 2: preprocesamiento y limpieza (preparación)

Una vez capturados, nos enfrentamos a la realidad de que los datos en bruto (*raw data*) suelen ser imperfectos. Contienen errores, duplicados o huecos que, si no se tratan, contaminarían cualquier análisis posterior bajo el principio de "si entra basura, sale basura".

- **Limpieza y depuración:** Es el proceso higiénico fundamental consistente en detectar y eliminar registros corruptos, corregir imprecisiones obvias y unificar duplicados para asegurar una base sólida.
- **Normalización y estandarización:** Para poder comparar peras con manzanas, es necesario ajustar escalas y homogeneizar formatos (como fechas o divisas), permitiendo que datos de orígenes dispares hablen un idioma común.
- **Gestión de valores atípicos (*outliers*):** Requiere un análisis inteligente para discernir si un dato anómalo es un simple error de medición que debe descartarse o un evento extraordinario que contiene información valiosa de negocio.

> **Ejemplo:** Plataformas como Airbnb depuran exhaustivamente los datos de sus reservas para evitar precios irreales o fraudes antes de alimentar sus modelos predictivos de precios.

## 2.3. Fase 3: almacenamiento y gestión

Con los datos limpios, el desafío se traslada a su conservación eficiente. El volumen masivo del Big Data ha dejado obsoletos los servidores locales tradicionales, impulsando la adopción de arquitecturas escalables y flexibles, mayoritariamente en la nube.

- **Data Lake (lago de datos):** Funciona como un vasto reservorio donde se vierten los datos en su estado natural o crudo. Es una opción económica y flexible, ideal para que los científicos de datos exploren sin las restricciones de una estructura rígida previa.
- **Data Warehouse (almacén de datos):** Representa la biblioteca ordenada de la empresa. Aquí se guardan los datos que ya han sido estructurados, procesados y refinados, listos para ser consumidos rápidamente en informes ejecutivos y consultas de negocio.
- **Infraestructura Cloud (pública/híbrida):** Servicios globales como AWS S3, Microsoft Azure o Google Cloud permiten a las empresas escalar su capacidad de almacenamiento de forma elástica, pagando solo por lo que usan y olvidándose de las limitaciones físicas del hardware.

## 2.4. Fase 4: análisis y modelado

Llegamos al corazón del proceso, el momento en que la "materia prima" almacenada se transforma en conocimiento mediante la aplicación de inteligencia matemática y algoritmos avanzados.

- **Entrenamiento de modelos de IA:** Se alimentan algoritmos de aprendizaje automático (*Machine Learning*) con grandes volúmenes de datos históricos, "enseñando" a la máquina a reconocer comportamientos y reglas complejas.
- **Descubrimiento de patrones ocultos:** Mediante técnicas de minería de datos, se sacan a la luz tendencias, correlaciones y causalidades que permanecían invisibles a la intuición humana o al análisis tradicional.
- **Iteración y mejora continua:** El modelado no es un evento único; los modelos deben ser reentrenados y ajustados periódicamente con nuevos datos para mantener su precisión y adaptarse a la realidad cambiante.

## 2.5. Fase 5: interpretación, visualización y uso

Para que el análisis tenga impacto, debe salir del laboratorio y llegar a los tomadores de decisiones. Esta fase se encarga de traducir la complejidad matemática a un lenguaje de negocio claro y accionable.

- **Visualización de datos:** El uso de herramientas de Business Intelligence (como Power BI o Tableau) y cuadros de mando interactivos convierte las filas de números en gráficos intuitivos que cuentan una historia visual comprensible de un vistazo.
- **Toma de decisiones informada:** Es el objetivo último: habilitar a directivos y empleados para que transformen las predicciones e indicadores en acciones concretas, como realizar un mantenimiento preventivo antes de una avería o lanzar una oferta personalizada.

## 2.6. Fase 6: gobernanza, archivado y borrado

Finalmente, el ciclo se cierra con la responsabilidad corporativa. Gestionar el dato implica también protegerlo, cumplir la ley y saber cuándo despedirse de él para mantener la eficiencia y la legalidad.

- **Privacidad y ética (Compliance):** Garantizar el cumplimiento estricto de normativas como el RGPD es innegociable, incluyendo procesos de anonimización y la gestión transparente del consentimiento de los usuarios.
- **Ciberseguridad y protección:** Implementar barreras robustas y protocolos de acceso para blindar la información estratégica frente a accesos no autorizados, fugas o ciberataques, que podrían ser devastadores.
- **Archivado o destrucción segura:** Cuando el dato pierde su utilidad inmediata pero debe conservarse por ley, se mueve a un almacenamiento "frío" y barato. Si ya no es necesario, se procede a su borrado seguro para reducir costes y riesgos legales.

<a id="ciencia-datos"></a>

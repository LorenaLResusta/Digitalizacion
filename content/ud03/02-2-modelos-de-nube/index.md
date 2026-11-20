+++
title = "2. Modelos de nube"
weight = 2
+++

## 2.1 Nube pública

La **nube pública** es un modelo de computación en la nube donde los recursos, como **servidores**, **almacenamiento** y aplicaciones, son propiedad y están gestionados por proveedores externos como **Amazon Web Services (AWS)**, **Microsoft Azure** o **Google Cloud Platform (GCP)**. Este modelo se caracteriza por ofrecer un entorno compartido entre múltiples clientes, aunque cada uno dispone de entornos **virtualizados** y aislados que garantizan la **seguridad** y la **privacidad** de sus datos. Su gran ventaja es la **escalabilidad**, ya que las empresas pueden aumentar o reducir recursos según sus necesidades, pagando únicamente por lo que consumen, sin necesidad de hacer inversiones iniciales importantes en infraestructura. Esto lo hace ideal para startups, pymes o proyectos con demanda variable, donde el **coste** y la **flexibilidad** son cruciales.
[Nube pública 1 (enlace)](https://datatrust.sv/blog/que-es-una-nube-publica/)

Además, la **nube pública** permite acceder a tecnologías avanzadas como **inteligencia artificial**, análisis de datos a gran escala y servicios gestionados, sin requerir especialistas internos. Sin embargo, también implica cierta **dependencia del proveedor**, lo que puede generar riesgos si hay caídas de servicio o cambios en los precios. La **personalización** es limitada: las empresas no pueden modificar la infraestructura subyacente según sus políticas internas, lo que puede ser un inconveniente para sectores con alta regulación o necesidades de cumplimiento normativo.
[Nube pública 2 (enlace)](https://blog.prodwaregroup.com/es/perfiles/por-que-las-empresas-confian-cada-vez-mas-en-la-nube-publica/)

Este modelo es especialmente atractivo por su **agilidad y rapidez de implementación**: cualquier empresa puede lanzar servicios o aplicaciones en cuestión de minutos. Además, la **nube pública** facilita la **colaboración remota**, ya que los datos y aplicaciones son accesibles desde cualquier ubicación con conexión a **Internet**. A medida que la demanda de **digitalización** crece, la adopción de la **nube pública** sigue aumentando, especialmente entre empresas que buscan **innovar sin comprometer su liquidez**.
[Nube pública 3 (enlace)](https://www.ionos.mx/digitalguide/servidores/know-how/public-cloud/)

**Ejemplos y casos reales:**

- **Ejemplo:** **Spotify** utiliza **AWS** para escalar su infraestructura según demanda de usuarios, optimizando costes en picos estacionales.
- **Caso real:** El gobierno del **Reino Unido** emplea **GCP** para análisis de datos no críticos, mejorando eficiencia pública sin grandes inversiones.
- **Enlace:** [AWS Nube Pública](https://aws.amazon.com/es/what-is-cloud-computing/) – Tutorial interactivo con demos para explorar escalabilidad en tiempo real.
- **Tabla comparativa rápida:**

| Característica | Ventaja      | Desventaja                |
| -------------- | ------------ | ------------------------- |
| Escalabilidad  | Alta         | Dependencia del proveedor |
| Coste          | Pago por uso | Limitada personalización  |
| Seguridad      | Aislada      | Regulación sectorial      |

**Resumen:** La **nube pública** destaca por su **escalabilidad** y **coste bajo**, ideal para innovación rápida, como en **Spotify** y el gobierno del **Reino Unido**, pero requiere gestión de **dependencia** y **personalización limitada** para cumplir regulaciones.

## 2.2 Nube privada

La **nube privada** es un modelo de nube diseñado para el **uso exclusivo de una sola organización**, lo que le permite mantener un control total sobre la infraestructura y los datos. Puede estar alojada **dentro de la propia empresa** (**on-premises**) o ser gestionada por un proveedor externo dedicado, pero siempre con acceso restringido. Esto la hace ideal para sectores que manejan información **sensible**, como banca, salud o administración pública, donde la **seguridad**, el cumplimiento normativo y la **personalización** son prioridades. Las empresas pueden configurar la nube según sus necesidades exactas, aplicando políticas internas de **seguridad**, gestión de datos y control de accesos.
[Nube privada 1 (enlace)](https://whitestack.com/es/blog/que-es-una-nube-privada/)

El principal beneficio de la **nube privada** es el **control absoluto**: se puede ajustar la infraestructura a los requerimientos internos, asegurando confidencialidad y cumplimiento normativo. Además, permite integrar **sistemas heredados** y optimizar el rendimiento para cargas de trabajo críticas. Sin embargo, este modelo es **más costoso**, ya que requiere inversión en **servidores dedicados**, mantenimiento y personal especializado para gestión, monitorización y **seguridad**. La **escalabilidad** también está limitada comparada con la **nube pública**, aunque puede mejorarse mediante **virtualización** y automatización avanzada.
[Nube privada 2 (enlace)](https://www.abast.es/blog/nube-privada-nube-publica-o-nube-hibrida-que-tipo-de-cloud-es-mejor-para-mi-empresa/)
Otro punto relevante es que la **nube privada** proporciona **alta fiabilidad** y continuidad de negocio, ya que la organización tiene la capacidad de implementar redundancia y recuperación ante desastres según sus estándares internos. Esto la convierte en un recurso estratégico para empresas donde los tiempos de inactividad y la pérdida de datos pueden tener consecuencias graves, como pérdidas económicas o daños reputacionales.
[Nube privada 3 (enlace)](https://www.apd.es/que-es-una-nube-privada/)
**Ejemplos y casos reales:**

- **Ejemplo:** **BBVA** utiliza **nube privada** para datos críticos y sistemas financieros internos, asegurando cumplimiento regulatorio en banca.
- **Caso real:** **NASA** implementa nubes privadas para gestionar información científica y misiones espaciales, priorizando control y fiabilidad en datos sensibles.
- **Enlace:** [Microsoft Azure Nube Privada](https://azure.microsoft.com/es-es/overview/private-cloud/) – Caso de estudio con videos explicativos sobre implementación en sectores regulados.
- **Tabla comparativa rápida:**

| Característica  | Ventaja | Desventaja             |
| --------------- | ------- | ---------------------- |
| Control         | Total   | Costosa                |
| Seguridad       | Alta    | Escalabilidad limitada |
| Personalización | Máxima  | Requiere especialistas |

**Resumen:** La **nube privada** ofrece **control total** y **alta seguridad** para datos sensibles, como en **BBVA** y **NASA**, pero implica **costes elevados** y **escalabilidad limitada**, ideal para sectores regulados donde la personalización es esencial.

## 2.3 Nube híbrida

La **nube híbrida** combina características de los modelos **público y privado**, permitiendo que una organización decida qué cargas de trabajo mantener en cada entorno según criterios de **coste**, **seguridad** y **rendimiento**. Por ejemplo, datos altamente sensibles pueden permanecer en la **nube privada**, mientras que aplicaciones de menor criticidad se ejecutan en la **nube pública**. Este enfoque ofrece **flexibilidad**, optimizando recursos y **costes** sin comprometer la **seguridad**. Es especialmente útil para empresas que requieren **escalabilidad** rápida para ciertos proyectos sin exponer su información más crítica.
[Nube híbrida 1 (enlace)](https://www.sapia.com.pe/sin-categoria/que-es-una-nube-hibrida/)

El principal reto de la **nube híbrida** es la **gestión de la interoperabilidad**: integrar sistemas, aplicaciones y datos entre nubes públicas y privadas requiere herramientas de administración avanzadas y protocolos claros de **seguridad**. Sin embargo, bien implementada, permite **resiliencia**, redundancia y optimización de la infraestructura. La **nube híbrida** también facilita la **innovación**, ya que las empresas pueden experimentar con nuevas aplicaciones en la **nube pública** sin modificar su infraestructura privada.
[Nube híbrida 2 (enlace)](https://www.masip.es/blog/el-valor-de-la-nube-hibrida-y-la-inteligencia-artificial-para-las-empresas/)

Además, este modelo es estratégico para empresas que buscan un **equilibrio entre control, coste y escalabilidad**. Permite ajustar la inversión en infraestructura según necesidades específicas, reduciendo el gasto innecesario en recursos dedicados mientras se mantiene el cumplimiento normativo en sistemas críticos. Cada vez más organizaciones adoptan estrategias híbridas para aprovechar lo mejor de ambos mundos, convirtiéndola en una tendencia global creciente.
[Nube híbrida 3 (enlace)](https://www.teamnet.com.mx/blog/5-consejos-para-construir-una-nube-hibrida)
**Ejemplos y casos reales:**

- **Ejemplo:** **General Electric (GE)** combina **Azure** y su **nube privada** para operaciones globales, equilibrando escalabilidad y control en manufactura.
- **Caso real:** **Volkswagen** utiliza **nube híbrida** para conectar datos de vehículos con sistemas internos, optimizando rendimiento en automoción.
- **Enlace:** [IBM Nube Híbrida](https://www.ibm.com/cloud/hybrid) – Estudios de caso con diagramas interactivos que muestran integración paso a paso.
- **Tabla comparativa rápida:**

| Característica | Ventaja         | Desventaja                |
| -------------- | --------------- | ------------------------- |
| Flexibilidad   | Alta            | Gestión compleja          |
| Seguridad      | Control parcial | Requiere estrategia clara |
| Coste          | Optimizado      | Integración costosa       |

**Resumen:** La **nube híbrida** equilibra **flexibilidad** y **seguridad** combinando público y privado, como en **GE** y **Volkswagen**, permitiendo innovación sin riesgos, aunque exige gestión de **interoperabilidad** para optimizar costes y rendimiento.

## 2.4 Nube comunitaria

La **nube comunitaria** es un modelo compartido por varias organizaciones que tienen **intereses comunes**, como universidades, hospitales o consorcios de investigación. Permite que los participantes **compartan recursos y costes**, manteniendo cierto nivel de control sobre la infraestructura y **seguridad**. Este modelo combina ventajas de la **nube privada** (control) y la **pública** (**coste compartido**), fomentando la **colaboración**, la **innovación conjunta** y la investigación entre entidades.
[Nube comunitaria 1 (enlace)](https://www.innovaciondigital360.com/cloud/nube-comunitaria-comparta-sus-recursos/)

La **nube comunitaria** es útil cuando varias organizaciones necesitan **estándares de seguridad y cumplimiento homogéneos**, como en proyectos de investigación clínica, intercambio de datos académicos o cooperación gubernamental. Sin embargo, la **coordinación de la gobernanza** puede ser complicada: se deben establecer normas claras sobre acceso, **seguridad**, **costes** y responsabilidades, ya que los participantes pueden tener diferentes políticas internas. Aun así, permite **optimizar recursos**, evitando que cada institución tenga que invertir en infraestructura propia para proyectos similares.
[Nube comunitaria 2 (enlace)](https://blog.itqscr.com/diferencias-nube-publica-privada-hibrida)

Además, este modelo facilita **la interoperabilidad y el intercambio de conocimiento** entre entidades afines, acelerando el desarrollo de proyectos conjuntos y reduciendo duplicidades. La **nube comunitaria** puede ser gestionada por una organización líder o un proveedor externo, siempre con protocolos comunes que aseguren la **seguridad** y eficiencia del entorno compartido.
[Nube comunitaria 3 (enlace)](https://www.freepik.es/vector-premium/plantilla-diseno-logotipo-nube-comunitaria_20565132.htm)
**Ejemplos y casos reales:**

- **Ejemplo:** **EduCloud** en Europa, una **nube comunitaria** para universidades e institutos de investigación, compartiendo recursos para proyectos académicos colaborativos.
- **Caso real:** Consorcios hospitalarios en **EE.UU.** utilizan **nube comunitaria** para compartir datos clínicos de forma segura, mejorando investigación médica colectiva.
- **Enlace:** [Nube Comunitaria - NIST](https://www.nist.gov/itl/cloud-computing) – Guía con casos educativos y frameworks para implementación colaborativa.
- **Tabla comparativa rápida:**

| Característica | Ventaja    | Desventaja              |
| -------------- | ---------- | ----------------------- |
| Colaboración   | Alta       | Gobernanza compleja     |
| Coste          | Compartido | Normas heterogéneas     |
| Control        | Medio      | Dependencia de acuerdos |

**Resumen:** La **nube comunitaria** promueve **colaboración** y **optimización de costes** para entidades con intereses comunes, como **EduCloud** y consorcios hospitalarios en **EE.UU.**, pero requiere fuerte **gobernanza** para manejar interoperabilidad y seguridad homogénea.

## 2.5 Comparación entre modelos

La **nube híbrida** integra recursos de **nube pública** y **nube privada**, permitiendo ubicar cargas según criterios de **seguridad**, **coste** y **rendimiento**. Ofrece la **flexibilidad** de mantener datos sensibles en entornos privados mientras se aprovecha la **capacidad de escalado** de la nube pública para picos de carga (técnica conocida como **cloud bursting**). En este modelo son críticos la **portabilidad** (mover cargas entre nubes), la **interoperabilidad** (**APIs** y formatos comunes) y la **orquestación** para gestionar despliegues y políticas de **seguridad** de forma centralizada. La **nube híbrida** facilita migraciones graduales y soporta estrategias **multicloud** cuando se usan varios proveedores públicos. Sus retos principales son la complejidad de redes y **seguridad**, la gobernanza de datos y la necesidad de herramientas de gestión unificada. Bien diseñada, la **nube híbrida** ofrece un equilibrio entre control y agilidad, optimizando **costes** y cumplimiento normativo.
[Comparación modelos 1 (enlace)](https://iberiza.es/universo-iberiza/tipos-de-almacenamiento-en-la-nube/)

La **nube híbrida** combina **nube pública** y privada, y está pensada para ubicar cargas según **seguridad**, **latencia** y **coste**. Plataformas y soluciones que facilitan híbridos: [AWS Outposts](https://aws.amazon.com/outposts/), [Azure Arc / Azure Stack](https://azure.microsoft.com/en-us/overview/azure-arc/), [Google Anthos](https://cloud.google.com/anthos).

[Comparación modelos 2 (enlace)](https://digitnow.com.mx/en/cual-nube-de-internet-es-la-mejor/)
La **nube privada** proporciona recursos exclusivos para una sola organización, alojada **on-premises** o en centros de datos gestionados. Sus fortalezas son el **control**, el **aislamiento** y la **personalización** de políticas de **seguridad** y cumplimiento. Tecnologías y enlaces útiles: [OpenStack](https://www.openstack.org), [VMware vSphere](https://www.vmware.com/products/vsphere.html), [Azure Stack](https://azure.microsoft.com/en-us/overview/azure-stack/).
[Comparación modelos 3 (enlace)](https://es.venngage.com/templates/infographics/3-types-of-clouds-comparison-chart-e24b74d8-186f-4ed8-9e3f-f25d4ee088b4)

**Ejemplos y casos reales:**

- **Ejemplo:** **GE** usa **nube híbrida** con **Azure** para equilibrar control privado y escalabilidad pública en operaciones industriales.
- **Caso real:** **Volkswagen** integra **nube híbrida** para datos de vehículos, combinando privacidad y análisis en tiempo real.
- **Enlace:** [Comparación de modelos - IBM](https://www.ibm.com/cloud/hybrid) – Comparador interactivo con casos reales y calculadora de costes.
- **Tabla comparativa rápida:**

| Modelo          | Ventajas clave          | Desafíos                  | Caso real     |
| --------------- | ----------------------- | ------------------------- | ------------- |
| Pública         | Escalabilidad, coste bajo | Dependencia, menos control | Spotify (AWS) |
| Privada         | Seguridad, personalización | Alto coste, escalabilidad limitada | NASA (on-premises) |
| Híbrida         | Flexibilidad, equilibrio | Interoperabilidad compleja | GE (Azure)    |
| Comunitaria     | Colaboración, coste compartido | Gobernanza heterogénea | EduCloud (Europa) |

**Resumen:** Comparando modelos, la **pública** prioriza **escalabilidad** (ej. Spotify), **privada** **seguridad** (ej. NASA), **híbrida** **flexibilidad** (ej. GE), y **comunitaria** **colaboración** (ej. EduCloud), guiando la elección por necesidades de **coste**, **seguridad** y rendimiento.

## Tabla decisión rápida (elige modelo)

| Criterio | Pública | Privada | Híbrida | Comunitaria |
|---------|---------|---------|--------|-------------|
| Datos muy sensibles | ❌ | ✅ | ✅ (parcial) | ✅ (si normas comunes) |
| Picos impredecibles | ✅ | ⚠️ (dimensionar) | ✅ | ⚠️ |
| Presupuesto limitado inicial | ✅ | ❌ | ⚠️ | ✅ (compartido) |
| Cumplimiento estricto | ⚠️ | ✅ | ✅ | ✅ |
| Time-to-market crítico | ✅ | ⚠️ | ✅ | ⚠️ |

## Autoevaluación (Capítulo 2)

- ¿Qué riesgo operativo añade la nube híbrida?
- ¿Cuándo conviene comunitaria frente a privada?
- Indica un trade-off típico entre pública y privada.
- Define "cloud bursting" en una frase.
- Da un ejemplo de regulación que empuje a privada.

---

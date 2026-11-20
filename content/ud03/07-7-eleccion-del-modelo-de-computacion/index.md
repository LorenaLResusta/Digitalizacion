+++
title = "7. Elección del modelo de computación"
weight = 7
+++

## 7.1 Factores técnicos

La elección de un modelo de computación, ya sea **nube pública, privada, híbrida o comunitaria**, depende en gran medida de factores técnicos relacionados con las necesidades operativas y la infraestructura existente. Entre los aspectos más importantes están la **compatibilidad de aplicaciones**, la **capacidad de integración con sistemas heredados**, la **latencia aceptable** y la **capacidad de procesamiento y almacenamiento requerida**. Por ejemplo, una aplicación que requiere respuesta en tiempo real puede beneficiarse de un modelo **híbrido** o **edge/fog computing** para reducir **latencia**.

También se debe considerar la **resiliencia y redundancia**: si la empresa depende de sistemas críticos, necesitará un modelo que permita recuperación ante desastres y alta disponibilidad, lo que puede inclinar la elección hacia nubes **privadas** o **híbridas** con nodos redundantes. La **virtualización y contenedorización** de aplicaciones es otro factor técnico clave, ya que facilita la migración entre distintos entornos sin interrumpir operaciones.

**Ejemplos y casos reales:**
* **Ejemplo:** **Netflix** utiliza una arquitectura **híbrida** para equilibrar **streaming** en tiempo real y análisis global de datos, integrando legacy con edge.
* **Caso real:** **BBVA** integra sistemas bancarios **legacy** en **nube privada** para asegurar compatibilidad y **seguridad** en transacciones.
* **Enlace:** [Factores técnicos en nube - IBM](https://www.ibm.com/cloud/learn/cloud-computing) – Evaluador interactivo para mapear requisitos técnicos.
* **Tabla comparativa rápida:**

| Factor técnico | Implicación                                         |
| -------------- | --------------------------------------------------- |
| Latencia       | Determina si se requiere nube híbrida o edge/fog    |
| Compatibilidad | Influye en integración con sistemas existentes      |
| Resiliencia    | Elección de nubes privadas/híbridas con redundancia |
| Virtualización | Facilita migración y escalabilidad                  |

**Resumen:** **Factores técnicos** como **latencia** y **resiliencia** guían la elección, con **híbrida** para real-time (ej. Netflix) y **privada** para legacy (ej. BBVA), usando **virtualización** para migraciones fluidas.

## 7.2 Factores económicos

Los **factores económicos** son decisivos al elegir un modelo de computación. La **nube pública** suele ser más atractiva por su **pago por uso**, eliminando **costes** de infraestructura inicial y mantenimiento. La **nube privada**, en cambio, requiere inversión en **servidores dedicados**, licencias, personal y energía, aunque puede ofrecer mayor control y **seguridad**. El modelo **híbrido** permite equilibrar **coste** y rendimiento, asignando cargas críticas a la **nube privada** y el resto a la pública.

Es importante evaluar el **retorno de inversión (ROI)**, considerando tanto el ahorro en hardware y personal como los **costes** de migración, capacitación y mantenimiento. También hay que analizar los **costes de escalabilidad futura**, ya que empresas en crecimiento pueden beneficiarse de modelos flexibles que ajusten recursos automáticamente según demanda. Otro factor económico es la **optimización del consumo energético**, que impacta en empresas con grandes centros de datos locales.

**Ejemplos y casos reales:**
* **Ejemplo:** **Spotify** utiliza **nube pública** para escalar usuarios en picos de demanda, reduciendo **costes** de infraestructura en 50%.
* **Caso real:** **Walmart** combina **nube pública** y **privada** para optimizar **costes** en logística y análisis de datos, ahorrando millones anuales.
* **Enlace:** [Coste de la nube - Microsoft](https://learn.microsoft.com/es-es/azure/cost-management-billing/costs/) – Calculadora de TCO con escenarios reales.
* **Tabla comparativa:**

| Factor económico   | Implicación                                        |
| ------------------ | -------------------------------------------------- |
| Pago por uso       | Escalabilidad rentable en nube pública             |
| Costes iniciales   | Nube privada requiere inversión significativa      |
| ROI                | Evaluar ahorro vs. costes de migración             |
| Consumo energético | Impacta en costes operativos de servidores locales |

**Resumen:** **Factores económicos** priorizan **pago por uso** en pública (ej. Spotify) vs. inversión en privada (ej. Walmart híbrida), evaluando **ROI** y escalabilidad para optimizar consumo energético y crecimiento.

## 7.3 Factores de seguridad

La **seguridad** es uno de los factores más críticos en la elección del modelo de computación. Incluye **protección de datos**, cumplimiento normativo, control de accesos y **cifrado**. Las empresas que manejan información sensible, como bancos, hospitales o instituciones gubernamentales, suelen optar por **nubes privadas o híbridas**, donde pueden controlar quién accede a los datos y aplicar políticas estrictas de **seguridad**.

Además, la **seguridad** no se limita al almacenamiento, sino que abarca **transmisión de datos**, autenticación y monitoreo constante. Los modelos públicos requieren confianza en los proveedores y revisiones periódicas de certificaciones de **seguridad**, como **ISO 27001** o **SOC 2**. También hay que considerar la **resiliencia frente a ciberataques** y la capacidad de implementar **copias de seguridad** y recuperación ante desastres.

**Ejemplos y casos reales:**
* **Ejemplo:** **Capital One** migró parte de su infraestructura a la **nube pública**, implementando controles estrictos de **cifrado** y monitoreo para banca segura.
* **Caso real:** Hospitales europeos utilizan **nubes privadas** para cumplir **GDPR** en datos médicos, protegiendo privacidad paciente.
* **Enlace:** [Seguridad en la nube - NIST](https://www.nist.gov/news-events/news/2021/03/cloud-computing-security) – Framework con checklists y casos de cumplimiento.
* **Tabla comparativa :**

| Factor de seguridad         | Implicación                           |
| --------------------------- | ------------------------------------- |
| Control de datos            | Privada/híbrida ofrece mayor control  |
| Cumplimiento normativo      | Obligatorio en sectores regulados     |
| Cifrado                     | Protege datos en tránsito y reposo    |
| Recuperación ante desastres | Necesario para continuidad de negocio |

**Resumen:** **Seguridad** favorece **privadas/híbridas** para control (ej. Capital One pública con cifrado, hospitales GDPR), evaluando **resiliencia** y certificaciones como **ISO 27001** para mitigar ciberataques.

## 7.4 Escalabilidad y flexibilidad

La **escalabilidad y flexibilidad** determinan si un modelo puede adaptarse a cambios en la demanda y crecimiento de la organización. La **nube pública** destaca por su **escalado automático**, ajustando recursos en tiempo real según número de usuarios o volumen de datos. La **nube privada** permite **escalabilidad**, pero suele requerir planificación de infraestructura y recursos humanos. El modelo **híbrido** combina ambos, asignando cargas críticas a la **nube privada** y el resto a la pública según necesidad.

La **flexibilidad** también implica **capacidad de migración**, integración de nuevas aplicaciones y despliegue rápido de servicios. Empresas con alta innovación tecnológica o picos estacionales de demanda, como **comercio electrónico** o **streaming**, se benefician de entornos que permiten cambiar rápidamente recursos sin afectar usuarios finales.

**Ejemplos y casos reales:**
* **Ejemplo:** **Netflix** ajusta servidores en la **nube pública** para picos de **streaming** durante estrenos, escalando globalmente.
* **Caso real:** **Amazon Web Services** permite **escalado automático** en picos de ventas en **Black Friday**, manejando millones de transacciones.
* **Enlace:** [Escalabilidad en la nube - AWS](https://aws.amazon.com/what-is-cloud-computing/) – Simulador interactivo de escalado.
* **Tabla comparativa :**

| Factor        | Nube pública      | Nube privada               | Nube híbrida    |
| ------------- | ----------------- | -------------------------- | --------------- |
| Escalabilidad | Alta y automática | Limitada, planificada      | Alta y flexible |
| Flexibilidad  | Rápida            | Requiere recursos internos | Equilibrada     |
| Integración   | Mediana           | Alta                       | Alta            |

**Resumen:** **Escalabilidad** y **flexibilidad** inclinan hacia pública para picos (ej. Netflix Black Friday en AWS), híbrida para equilibrio, facilitando migración y despliegue rápido en innovación.

## 7.5 Toma de decisiones estratégicas

La **decisión estratégica** sobre el modelo de computación debe considerar **objetivos de negocio**, riesgos, **costes** y tecnología. No se trata solo de elegir la opción más barata o segura, sino de alinear la infraestructura con la visión corporativa. Empresas que dependen de datos críticos y cumplimiento normativo pueden priorizar **privacidad y control**, mientras que startups buscan **agilidad y escalabilidad**.

Además, la estrategia debe incluir **planificación de migración**, contingencias de **seguridad**, monitoreo y soporte. Es fundamental evaluar proveedores, certificaciones, ecosistema tecnológico y capacidad de crecimiento futuro. La elección correcta permite mejorar eficiencia operativa, innovación y ventaja competitiva, mientras que una decisión errónea puede generar sobrecostes, problemas de **seguridad** y falta de flexibilidad.

**Ejemplos y casos reales:**
* **Ejemplo:** **Spotify** eligió **nube pública** por **agilidad** y **escalabilidad** global en recomendaciones musicales.
* **Caso real:** **Banco Santander** combina **nube privada** y pública para cumplir regulación y escalar servicios digitales en banca.
* **Enlace:** [Decisión estratégica en la nube - Gartner](https://www.gartner.com/en/information-technology/glossary/cloud-computing) – Marco de madurez con evaluador de riesgos.

**Resumen:** **Decisiones estratégicas** alinean modelos con **objetivos** y riesgos, como **pública** para agilidad (Spotify) o híbrida para cumplimiento (Santander), evaluando migración y crecimiento para ROI óptimo.

**Autoevaluación (Capítulo 7)**
- Da un ejemplo de métrica para evaluar lock-in.
- ¿Qué factor técnico empuja a híbrida?
- Diferencia entre coste directo y coste de oportunidad.
- ¿Por qué FinOps es continuo y no único?
- ¿Qué rol cumple un plan de salida temprano?

---

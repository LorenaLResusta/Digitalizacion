+++
title = "3. Servicios en la nube"
weight = 3
+++

## 3.1 IaaS (Infraestructura como servicio)

La Infraestructura como Servicio (IaaS) ofrece una capa base donde se trasladan máquinas virtuales, redes y almacenamiento a un entorno gestionado por terceros. En términos prácticos, IaaS es la opción cuando una organización necesita conservar control sobre el sistema operativo, las configuraciones de red y la personalización del stack, pero quiere evitar la gestión del hardware físico. En este primer párrafo explicamos dónde encaja IaaS: es habitual en migraciones tipo "lift-and-shift", en aplicaciones legacy que requieren configuraciones especiales, y en entornos que necesitan control fino de la seguridad a nivel de sistema operativo. Desde el punto de vista de costes y operaciones, permite escalado rápido (provisión de instancias por demanda) y modelos de facturación por uso, aunque introduce responsabilidades operativas como parcheo, backups y gestión de imágenes.

[IaaS 1 (enlace)](https://gtsperu.com/servicios/infraestructura-como-servicio-iaas/)

Al elegir IaaS conviene evaluar no sólo el coste por hora de las instancias, sino también el coste total de propiedad asociado a operaciones: personal DevOps, gestión de parches, monitorización y cumplimiento. En este segundo párrafo abordamos cómo calcular esa ecuación práctica. Un ejercicio útil es comparar escenarios: mantener la carga on‑premises vs migrar a IaaS vs re‑arquitecturar para PaaS. Para cargas estables y predecibles, la opción de instancias reservadas o acuerdos a largo plazo suele mejorar la eficiencia económica; para picos, la capacidad de escalar on‑demand evita gastar en hardware ocioso. Además, la latencia y la cercanía a otros servicios (p. ej. bases de datos gestionadas) son factores operativos que influyen en la selección de región y tipo de instancia.

[IaaS 2 (enlace)](https://www.tecnoera.cl/contenido/blog/que-es-iaas)

Desde la perspectiva operativa y de seguridad, IaaS exige prácticas maduras de administración: infraestructura como código (IaC), pipelines de CI/CD para imágenes, gestión centralizada de logs y alertas, y políticas de hardening para sistemas operativos. En este tercer párrafo describimos las tareas diarias y las métricas que justifican IaaS frente a alternativas: tiempo medio de despliegue, MTTR, coste por transacción y porcentaje de automatización. También conviene planificar backups, tests de restauración y políticas de redundancia. Para visualizar conceptos, la imagen siguiente muestra recursos típicos en un despliegue IaaS.

[IaaS 3 (enlace)](https://www.ninjaone.com/blog/what-is-infrastructure-as-a-service-iaas/)

Caso real: **Netflix** utiliza servicios de **IaaS** en la nube (principalmente **AWS**) para escalar dinámicamente su capacidad de **streaming** a millones de usuarios. Gracias a **IaaS**, puede aprovisionar recursos para picos de tráfico (estrenos) y pagar solo por lo consumido, optimizando costes en un 30% anual según informes de AWS.

Ventajas: **control**, **personalización**, posibilidad de ejecutar cargas **legacy**. Inconvenientes: requiere operaciones y conocimiento **DevOps**, gestión de actualizaciones y **seguridad** a nivel de sistema.

**Ejemplos y casos reales:**

- **Ejemplo:** **Capital One** usa **AWS EC2** para migrar mainframes legacy a la nube, manteniendo control sobre OS sin hardware propio.
- **Caso real:** **Airbnb** emplea **Google Compute Engine** para servidores virtuales en reservas globales, escalando con demanda estacional.
- **Enlace:** [IaaS en AWS - Caso Netflix](https://aws.amazon.com/solutions/case-studies/netflix/) – Estudio detallado con métricas de escalabilidad y ROI.
- **Tabla comparativa rápida:**

| Aspecto       | Ventaja                  | Desafío                  |
| ------------- | ------------------------ | ------------------------ |
| Control       | Alto sobre OS/apps       | Requiere DevOps          |
| Escalabilidad | Instantánea              | Gestión de seguridad     |
| Coste         | Pago por uso             | Actualizaciones manuales |

**Resumen:** **IaaS** ofrece **control granular** y **escalabilidad** para infraestructuras personalizadas, como en **Netflix** y **Airbnb**, ideal para migraciones legacy, aunque demanda expertise en **DevOps** para maximizar beneficios.

## 3.2 PaaS (Plataforma como servicio)

La Plataforma como Servicio (PaaS) es la capa que abstrae la infraestructura subyacente para que los equipos puedan centrarse en construir y desplegar aplicaciones. En este primer párrafo explicamos su propuesta de valor: PaaS proporciona runtimes, bases de datos gestionadas, y herramientas de despliegue que reducen tareas operativas, acelerando el desarrollo y permitiendo a equipos pequeños lanzar productos rápidamente. Para organizaciones que priorizan tiempo al mercado y productividad del desarrollador, PaaS reduce la carga de operaciones y facilita la adopción de practicas automatizadas como CI/CD y despliegues blue/green sin necesidad de gestionar servidores.

[PaaS 1 (enlace)](https://www.tecnologias-informacion.com/paas.html)

Elegir PaaS implica sopesar beneficios y riesgos. En este segundo párrafo abordamos criterios prácticos: si la aplicación requiere dependencias específicas del sistema o configuraciones no soportadas por la plataforma, PaaS puede resultar limitante; si el objetivo es iterar rápidamente y beneficiarse de escalado gestionado, PaaS es idónea. También hay que evaluar el riesgo de vendor lock‑in y la estrategia de migración: mantener contenedores portables y evitar APIs propietarias cuando se requiera flexibilidad a futuro. Un análisis de escenarios (MVP, producción y picos) ayuda a comparar coste y velocidad de entrega.

[PaaS 2 (enlace)](https://www.grupocsi.com/blog/plataforma-como-servicio-paas-que-es-y-sus-beneficios)

Operativamente, PaaS requiere integración con pipelines de entrega, monitorización y políticas de seguridad que cubran desde el código hasta la configuración de servicios gestionados. En este tercer párrafo describimos buenas prácticas: usar IaC para definir servicios, instrumentar métricas de rendimiento y error, y aplicar controles de acceso y cifrado a datos gestionados. También conviene diseñar planes de contingencia para migrar cargas críticas si la plataforma cambia o surgen requisitos no compatibles. La imagen siguiente ilustra ejemplos y casos de uso de PaaS.

[PaaS 3 (enlace)](https://www.channelpartner.es/cloud/paas-la-revolucion-en-el-desarrollo-de-aplicaciones/)

Caso real: Muchas startups adoptan **PaaS** (por ejemplo, aplicaciones prototipo en **Heroku**) porque reduce el tiempo de puesta en marcha y simplifica el pipeline de despliegue. Plataformas **PaaS** han permitido a equipos pequeños lanzar productos en semanas en lugar de meses, como en el caso de **Shopify**, que usa **Google App Engine** para escalar e-commerce global.

Ventajas: **productividad**, despliegue rápido, mantenimiento reducido. Riesgos: posible **vendor lock-in** y limitaciones si se requiere control fino de la infraestructura o configuraciones inusuales.

**Ejemplos y casos reales:**

- **Ejemplo:** **Red Hat OpenShift** en **PaaS** permite a desarrolladores enfocarse en código sin gestionar servidores, acelerando innovación.
- **Caso real:** **Capital One** usa **Azure App Service** para apps de banca móvil, reduciendo tiempo de desarrollo en 40%.
- **Enlace:** [PaaS en Google - Caso Shopify](https://cloud.google.com/customers/shopify) – Video testimonial con métricas de productividad.
- **Tabla comparativa rápida:**

| Aspecto       | Ventaja                  | Desafío                  |
| ------------- | ------------------------ | ------------------------ |
| Productividad | Enfoque en código        | Vendor lock-in           |
| Despliegue    | Rápido y automatizado    | Limitaciones de control  |
| Mantenimiento | Reducido por proveedor   | Configuraciones fijas    |

**Resumen:** **PaaS** acelera **desarrollo** y **despliegue** al abstraer infraestructura, como en **Shopify** y **Capital One**, fomentando **productividad**, pero con riesgos de **lock-in** que requieren planificación para flexibilidad.

## 3.3 SaaS (Software como servicio)

El modelo SaaS entrega aplicaciones completas gestionadas por el proveedor; para usuarios y negocios representa la forma más rápida de adoptar software sin preocuparse por infraestructura ni actualizaciones. En este primer párrafo explicamos el impacto de SaaS en procesos empresariales: reduce barreras de entrada, permite escalado de usuarios mediante suscripciones y traslada la responsabilidad de mantenimiento y seguridad del proveedor al cliente en términos de configuración y gobernanza. SaaS es especialmente valioso para funciones estándar (correo, CRM, colaboración) donde el valor principal está en la funcionalidad y la integración con otros servicios.

[SaaS 1 (enlace)](https://blog.wearedrew.co/abc-del-software-como-servicio-saas)

Al adoptar SaaS, es crucial planificar la integración y la protección de datos. En este segundo párrafo tratamos retos prácticos: cómo conectar APIs, sincronizar identidades (SSO, SCIM), y gestionar flujos de datos entre SaaS y sistemas internos. También hay que evaluar acuerdos de nivel de servicio (SLA), políticas de retención de datos y requisitos regulatorios que puedan imponer límites a la localización de la información. La elección de SaaS no excluye la necesidad de estrategias de backup y exportación de datos para mitigar dependencia del proveedor.

[SaaS 2 (enlace)](https://www.cloudflare.com/es-es/learning/cloud/what-is-saas/)

Finalmente, la gobernanza y la gestión de cambios son clave en entornos SaaS: controles de acceso, procesos de aprobación para nuevas integraciones, y métricas que midan adopción, coste por usuario y valor aportado. En este tercer párrafo describimos buenas prácticas operativas: inventario de aplicaciones, procesos de onboarding/offboarding, y revisión periódica de permisos. Una imagen complementaria ayuda a recordar diferencias entre modelos y casos de uso típicos.

[SaaS 3 (enlace)](https://kinsta.com/es/blog/productos-saas/)

Caso real: Empresas de todos los tamaños usan **Salesforce** para gestionar ventas y atención al cliente, evitando desarrollar y mantener su propia solución **CRM**. Las organizaciones reducen **costes** de mantenimiento y aceleran procesos comerciales, como **HubSpot**, que escaló su SaaS para millones de usuarios gratuitos.

Ventajas: bajo **coste de entrada**, manejo de actualizaciones y soporte por parte del proveedor. Inconvenientes: menor control sobre datos, dependencia de las políticas de **privacidad** y **seguridad** del proveedor.

**Ejemplos y casos reales:**

- **Ejemplo:** **Slack** como **SaaS** para comunicación interna, integrando con herramientas existentes sin instalación.
- **Caso real:** **Zoom** usó **SaaS** para videollamadas remotas durante la pandemia, escalando a 300 millones de usuarios diarios.
- **Enlace:** [SaaS en Salesforce - Caso HubSpot](https://www.salesforce.com/customer-success-stories/hubspot/) – Estudio con datos de crecimiento y ROI.
- **Tabla comparativa rápida:**

| Aspecto       | Ventaja                  | Desafío                  |
| ------------- | ------------------------ | ------------------------ |
| Coste         | Bajo, suscripción        | Dependencia proveedor    |
| Actualizaciones | Automáticas              | Control limitado datos   |
| Soporte       | Incluido                 | Políticas privacidad     |

**Resumen:** **SaaS** simplifica acceso a software gestionado, como en **Zoom** y **HubSpot**, reduciendo **costes** y acelerando adopción, pero exige evaluar **dependencia** y **privacidad** para usos sensibles.

## 3.4 Funciones como servicio (FaaS)

FaaS o serverless representa un cambio de paradigma: en lugar de servicios siempre activos, se despliegan unidades de ejecución que responden a eventos puntuales. En este primer párrafo explicamos por qué FaaS es eficaz: reduce costes para cargas intermitentes (pago por ejecución), facilita la escalabilidad automática y simplifica el modelo operativo al quitar la necesidad de gestionar servidores. Es ideal para tareas de backend livianas, procesamiento de eventos, pipelines de datos y microservicios que no requieren un tiempo de ejecución continuo.

[FaaS 1 (enlace)](https://kinsta.com/es/blog/funcion-como-servicio/)

Sin embargo, diseñar con FaaS exige abordar limitaciones y patrones de diseño. En este segundo párrafo tratamos aspectos prácticos: gestionar cold starts, diseñar funciones idempotentes, optimizar paquetes para reducir latencia de arranque, y organizar funciones en torno a eventos bien definidos. También se debe planificar la observabilidad (tracing, logs centralizados) y la orquestación de flujos complejos (ej. Step Functions o Workflows) cuando la lógica supera lo que puede hacerse en una única función.

[FaaS 2 (enlace)](https://www.cloudflare.com/es-es/learning/serverless/glossary/function-as-a-service-faas/)

Operativamente, FaaS precisa integración con sistemas de CI/CD, tests automáticos y reclasificación de responsabilidades entre equipos. En este tercer párrafo describimos buenas prácticas: versionado de funciones, pruebas de carga para medir cold starts, y límites de tiempo/memoria adecuados para evitar fallos en producción. También se recomienda definir métricas específicas (latencia 95p, coste por ejecución) y políticas de retry/backoff. La siguiente imagen ilustra conceptos clave y casos de uso comunes.

[FaaS 3 (enlace)](https://blog.infranetworking.com/faas-funcion-como-servicio-que-es-y-para-que-sirve/)

Caso real: Equipos de producto utilizan **Lambda** para procesar cargas asíncronas (transformación de imágenes, ingestión de logs, webhooks) logrando **costes** muy bajos para cargas intermitentes y alta **escalabilidad** sin gestión de servidores, como **Coca-Cola**, que procesa datos IoT en tiempo real.

Ventajas: **coste eficiente** para cargas **event-driven**, simplicidad operativa. Limitaciones: tiempo de ejecución limitado, desafíos de **cold start**, complejidad en tracing y observabilidad en arquitecturas distribuidas.

**Ejemplos y casos reales:**

- **Ejemplo:** **Pinterest** usa **Google Cloud Functions** para personalización de feeds, escalando eventos sin servidores dedicados.
- **Caso real:** **iRobot** emplea **Azure Functions** para análisis de datos de aspiradoras Roomba, reduciendo latencia en 50%.
- **Enlace:** [FaaS en AWS - Caso Coca-Cola](https://aws.amazon.com/solutions/case-studies/coca-cola/) – Demo con métricas de eficiencia.
- **Tabla comparativa rápida:**

| Aspecto       | Ventaja                  | Desafío                  |
| ------------- | ------------------------ | ------------------------ |
| Coste         | Por ejecución            | Cold starts              |
| Escalabilidad | Automática               | Tiempo limitado          |
| Operativa     | Sin servidores           | Tracing complejo         |

**Resumen:** **FaaS** optimiza **event-driven** con escalabilidad sin servidores, como en **Coca-Cola** y **iRobot**, bajando **costes**, pero enfrenta **cold starts** y complejidad en observabilidad para arquitecturas distribuidas.

## 3.5 Comparativa de modelos de servicio

Comparar modelos de servicio no es solo enumerar ventajas; es entender qué problemas resuelve cada opción y cómo encajan en una estrategia operativa. En este primer párrafo presentamos una visión integradora: IaaS proporciona control y flexibilidad para cargas específicas, PaaS acelera desarrollo con plataformas gestionadas, SaaS externaliza funcionalidades completas, y FaaS permite arquitecturas basadas en eventos. La elección depende de factores como criticidad, necesidad de control, velocidad de entrega y coste operativo.

[Comparativa servicios 1 (enlace)](https://www.stackscale.com/es/blog/modelos-de-servicio-cloud/)

Para decidir, conviene hacer ejercicios prácticos: mapear las cargas de trabajo a criterios (latencia, criticidad, coste, cumplimiento) y construir escenarios (MVP, producción, picos). En este segundo párrafo explicamos una metodología útil: priorizar cargas críticas en infraestructuras controladas, experimentar nuevas funciones en PaaS y manejar piezas event‑driven con FaaS. Además, incorporar FinOps desde el inicio ayuda a cuantificar costes y optimizar gasto en la nube.

[Comparativa servicios 2 (enlace)](https://www.infortisalabs.com/blog/aws-vs-azure-vs-google-cloud/)

Finalmente, desde la gobernanza y la operación, la recomendación es adoptar una estrategia híbrida y medible: definir KPIs (tiempo de despliegue, MTTR, coste por transacción), establecer políticas de seguridad y responsabilidades claras entre proveedor y cliente. El tercer párrafo aborda estas prácticas operativas y su traducción en políticas internas que permiten escalar con control. La imagen siguiente resume comparativas y casos de uso.

[Comparativa servicios 3 (enlace)](https://www.coremain.com/saas-paas-iaas-diferencias-cloud/)

Estrategia recomendada: muchas organizaciones adoptan una **combinación**: infraestructura base en **IaaS**, plataformas de desarrollo en **PaaS** para nuevas aplicaciones, **SaaS** para funciones estándar (correo, colaboración) y **FaaS** para piezas **event-driven**. Esto permite optimizar **costes**, **agilidad** y control según cada caso de uso.

**Ejemplos y casos reales:**

- **Ejemplo:** **Netflix** combina **IaaS** (AWS EC2) para control, **PaaS** para desarrollo y **SaaS** para colaboración, escalando streaming.
- **Caso real:** **Spotify** usa **PaaS** (Google App Engine) con **FaaS** para recomendaciones, migrando de **on-premise** a híbrido.
- **Enlace:** [Comparativa IaaS/PaaS/SaaS - BMC](https://www.bmc.com/blogs/saas-vs-paas-vs-iaas-whats-the-difference-and-how-to-choose/) – Infografía interactiva con pros/contras y calculadora de elección.
- **Tabla comparativa rápida:**

| Modelo | Control | Coste | Ejemplo          |
| ------ | ------- | ----- | ---------------- |
| IaaS   | Alto    | Medio | Netflix (EC2)    |
| PaaS   | Medio   | Bajo  | Spotify (App Engine) |
| SaaS   | Bajo    | Muy bajo | Zoom (colaboración) |
| FaaS   | Bajo    | Muy bajo | Coca-Cola (Lambda) |

**Resumen:** La **comparativa** de **IaaS**, **PaaS**, **SaaS** y **FaaS** resalta equilibrio entre control y coste, con estrategias híbridas como en **Netflix** y **Spotify** optimizando agilidad para casos variados.

## Checklist rápida selección servicio

- ¿Necesito acceso root / kernel? → IaaS.
- ¿Prioridad es reducir time-to-market? → PaaS.
- ¿Funcionalidad estándar (correo/CRM)? → SaaS.
- ¿Procesos intermitentes / event-driven? → FaaS.
- ¿Necesito portabilidad multi proveedor? → Minimizar dependencias PaaS propietarias.

## Autoevaluación (Capítulo 3)

- Diferencia productiva clave entre PaaS e IaaS.
- Riesgo principal de PaaS mal planificado.
- Métrica útil para evaluar FaaS además de coste.
- ¿Cuándo preferir SaaS frente a desarrollar propio?
- Explica por qué combinar FaaS e IaaS puede ser eficiente.

---

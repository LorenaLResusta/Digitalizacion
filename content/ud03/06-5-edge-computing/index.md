+++
title = "5. Edge computing"
weight = 6
+++

> Mapa rápido edge/fog/mist
>
> - Mist: sensor / micro-dispositivo.
> - Fog: nodo intermedio agregador.
> - Edge: gateway / micro-centro cercano.
> - Cloud: entrenamiento, almacenamiento histórico.
> - Flujo: datos crudos → filtrado → agregación → analítica profunda.
>

**Resumen visual (texto):** Latencia decrece al acercar el cómputo; capacidad de cómputo aumenta hacia la nube.

## 5.1 Concepto y fundamentos

**Edge computing** desplaza procesamiento y toma de decisiones hacia la periferia de la red, en dispositivos, gateways y micro-centros locales. Esta sección unifica conceptos ya expuestos en el documento y amplía aspectos prácticos: arquitectura, técnicas, herramientas, **seguridad**, economía y ejemplos reales.

El despliegue de arquitecturas **edge** no es solamente una decisión tecnológica, sino una estrategia organizativa que implica rediseñar flujos de datos, responsabilidades operativas y modelos de negocio. Un proyecto **edge** bien planteado parte de un análisis de requisitos (**latencia** máxima tolerable, volumen y sensibilidad de datos, disponibilidad requerida y **coste** por nodo) y suele arrancar con pilotos acotados: un número reducido de dispositivos, métricas claras y un plan de rollback. Técnico y operativo deben converger: ingenieros de datos, equipos de redes, **seguridad** y operaciones (**DevOps/IoT Ops**) deben coordinarse para definir pipelines de datos locales y remotos, políticas de gobernanza y procesos de actualización (**OTA**). La gestión del cambio es clave: los equipos necesitan formación en nuevas herramientas (orquestadores ligeros, runtimes de inferencia) y en prácticas de **seguridad** específicas del borde. Además, la naturaleza distribuida del **edge** obliga a pensar en monitorización y observabilidad desde el inicio: telemetría sobre rendimiento, estado de hardware, uso de modelos y **latencia** end-to-end. Este enfoque minimiza riesgos, facilita iteraciones rápidas y ayuda a demostrar el **retorno de inversión** antes de una escala masiva.

Desde el punto de vista técnico, diseñar para el **edge** significa aceptar heterogeneidad: distintos procesadores (**ARM**, **x86**), aceleradores (**GPU**, **NPU**, **TPU**), capacidades de memoria y conectividades. Esto obliga a abstraer despliegues mediante **contenedores ligeros** y runtimes que soporten cross-compilation y modelos quantizados que reduzcan tamaño y **latencia** de inferencia. El uso de formatos estándar como **ONNX** facilita portar modelos entre plataformas; al mismo tiempo, frameworks como **TensorFlow Lite** o **PyTorch Mobile** permiten optimizaciones específicas. En redes, los patrones híbridos (procesado local + sincronización eventual con la nube) reducen el ancho de banda consumido y mejoran **resiliencia**. Para cargas críticas, el diseño debe contemplar redundancia local y estrategias de failover, por ejemplo replicando funciones clave entre varios nodos o manteniendo capacidades mínimas en la nube para tomar el control si el borde falla. Finalmente, la automatización del pipeline — desde **CI/CD** de modelos hasta despliegues **OTA** seguros— es vital para mantener consistencia operativa en miles de nodos distribuidos.
![Decision flow](decision-flow.svg)

Mirando al futuro, varias tendencias acelerarán la adopción del **edge**: la consolidación del **5G** de baja **latencia**, la aparición de procesadores especializados para inferencia en dispositivos de bajo consumo y la maduración de plataformas de orquestación ligera que facilitan despliegues a escala. Asimismo, veremos una convergencia entre prácticas de **seguridad** cloud-native (**mTLS**, **Zero Trust**) y requisitos de hardware (**TPM**, arranque seguro) que permitirá implementar modelos de confianza distribuidos. Por otro lado, el **edge** fomentará nuevos servicios digitales que monetizan la **latencia** —por ejemplo, experiencias inmersivas en eventos deportivos o aplicaciones industriales que cobran por garantía de respuesta en tiempo real—. A medida que la tecnología y el ecosistema maduren, el desafío será mantener **interoperabilidad** y gestionar la complejidad operativa sin sacrificar **seguridad** ni gobernanza de datos.
![Edge vs Cloud](edge-vs-cloud.svg)

El **edge computing** acerca el procesamiento de datos al lugar donde se generan para reducir **latencia**, ahorrar ancho de banda y permitir respuestas en tiempo real. Se aplica en escenarios donde la rapidez de respuesta o la **privacidad** de los datos son críticas: control industrial, vehículos autónomos, dispositivos médicos conectados y análisis de video en cámaras de vigilancia.
![Fog vs Mist](fog-mist-hierarchy.svg)

Técnicas comunes: microservicios y **contenedores ligeros** (ej. **Docker**), orquestación local (**Kubernetes/K3s**), modelos de inferencia optimizados (quantization, pruning) y runtime especializados (**TensorRT**, **ONNX Runtime**). Protocolos habituales: **MQTT**, **CoAP**, **gRPC** y **HTTP/2** para comunicación eficiente.
![Cloud ROI](cloud-roi.svg)

### Ejemplos

- Clasificador de vibraciones en un **PLC** que solo transmite alertas al sistema central para ahorrar ancho de banda.
- Cámara de seguridad que ejecuta detección de personas localmente y solo sube clips tras confirmación.

### Casos reales

- **Siemens** y **Bosch**: inferencia local para **mantenimiento predictivo** en líneas de producción, reduciendo downtime en 30%.
- **Philips Healthcare**: procesamiento local en equipos de diagnóstico para acelerar resultados, mejorando precisión en IA médica.

### Enlaces

- **ONNX**: [onnx.ai](https://onnx.ai) – Estándar abierto para portabilidad de modelos, con tutoriales prácticos.
- **TensorFlow Lite**: [tensorflow.org/lite](https://www.tensorflow.org/lite) – Framework para edge, con ejemplos de código para dispositivos móviles.
- **MQTT**: [mqtt.org](https://mqtt.org) – Protocolo ligero para IoT, con guías de implementación.

### Infografía

**Resumen:** **Edge computing** fundamental para **latencia baja** y **privacidad**, con arquitectura híbrida y herramientas como **ONNX** y **TensorFlow Lite**, aplicadas en **Siemens** y **Philips** para mantenimiento y diagnóstico, equilibrando eficiencia y resiliencia.

## 5.2 Diferencias con la nube tradicional

El **edge** complementa la nube en una jerarquía: **mist** (dispositivo) → **edge** (gateway/local node) → **fog** (regional aggregation) → nube (entrenamiento/almacenamiento global). La nube se encarga de entrenamiento de modelos, almacenamiento histórico y coordinación; el **edge** ejecuta inferencias, acciones locales y preprocesado de datos.

Patrones arquitectónicos: procesamiento en el borde para filtrado y agregación, **cloud-assisted inference** (modelos ligeros en edge con reentrenamiento en la nube) y control híbrido (decisiones locales con sincronización eventual con la nube).

La arquitectura de **edge** debe planificarse pensando en límites de consistencia, sincronización y gobernanza. En sistemas distribuidos con nodos en el borde, es frecuente aplicar modelos de consistencia eventual para los datos menos críticos y mecanismos de consenso o replicación local para los elementos críticos de control. Esto requiere definir claramente qué datos se procesan y retienen localmente (por ejemplo: señales de control, alertas, metadatos) y qué datos se consolidan en la nube para análisis históricos y reentrenamiento de modelos. La **latencia**, la calidad de servicio de la red y la previsión de picos de carga son entradas clave para decidir la profundidad del procesamiento local: cuando la **latencia** es determinante, el borde tomará las decisiones, y la nube actuará como plano de coordinación y auditoría.

Desde el punto de vista de integración, conviene diseñar **APIs** y contratos de datos estables, emplear formatos interoperables (**JSON**, **CBOR**, **Protobuf/gRPC**) y adoptar patrones como sidecar para servicios auxiliares (telemetría, **seguridad**) que simplifican despliegues heterogéneos. Los gateways suelen actuar como puntos de agregación y de traducción de protocolos (**CoAP** ↔ **MQTT** ↔ **HTTP**), ejecutando funciones de enrutamiento, normalización y filtrado. También es habitual separar el plano de control (orquestación, políticas) del plano de datos (telemetría, inferencia) para facilitar actualizaciones y escalar cada capa de forma independiente.

El **edge** y la nube son compañeros de trabajo: la nube aporta memoria, contexto y aprendizaje a largo plazo; el **edge** aporta rapidez y respuesta local. Desde un punto de vista práctico, hay que decidir qué datos deben ser procesados al instante (alertas, controles, inferencias críticas) y cuáles pueden agregarse y enviarse a la nube para análisis históricos o reentrenamiento. Esa decisión depende de la **latencia** aceptable, del **coste** de transmitir datos y de requisitos regulatorios.

Para que esta colaboración funcione se recomienda usar **APIs** estables y formatos interoperables (por ejemplo **JSON** o **Protobuf**), diseñar contratos de datos claros y emplear gateways como puntos de agregación y traducción de protocolos. Separar el plano de control (orquestación, políticas) del plano de datos (telemetría e inferencia) hace que las actualizaciones sean más seguras y sencillas. En términos cotidianos: el borde reduce la cantidad de información que viaja; la nube aporta el conocimiento que mejora las decisaiones futuras.

### Ejemplos, casos y recursos
- Ejemplo práctico: un gateway que agrega datos de sensores y solo envía resúmenes o alertas, reduciendo ancho de banda.
- Caso real: **Amazon Wavelength / MEC**, que integra **edge** con operadores móviles para servicios de baja **latencia** en 5G.
- Recursos útiles: **NIST Edge Computing report** (https://www.nist.gov/publications) – Marco estandarizado con diagramas arquitectónicos.
- **GSMA MEC** (https://www.gsma.com/future-networks/) – Casos de telecom con infografías de jerarquías edge-nube.

**Resumen:** **Edge** difiere de la nube tradicional por su enfoque en **latencia baja** y procesamiento local, complementándola en jerarquías híbridas, como en **Amazon Wavelength**, con patrones como **cloud-assisted inference** para equilibrar rapidez y escalabilidad.

**Tabla jerarquía y características**
| Capa | Latencia objetivo | Persistencia | Ejemplo acción | Energía disponible |
|------|------------------|--------------|----------------|--------------------|
| Mist | < 5 ms           | Mínima       | Interrumpir motor | Muy baja |
| Edge | 5–20 ms          | Local parcial| Agregar eventos | Moderada |
| Fog  | 20–100 ms        | Agregada     | Correlacionar sitios | Media |
| Cloud| >100 ms (no crítica) | Completa | Entrenar modelo | Alta |

**Checklist decisión edge**
- ¿La latencia de ida y vuelta supera el SLA? → Llevar lógica al borde.
- ¿Coste de transmisión > coste de cómputo local? → Filtrado local.
- ¿Datos sensibles legales? → Preprocesar / anonimizar en edge.
- ¿Necesito reentrenar con histórico amplio? → Sincronizar batch a nube.

## 5.3 Casos de uso actuales

El diseño de casos de uso para **edge** exige una aproximación por dominio: en el sector industrial la prioridad es la disponibilidad y la determinación temporal (**hard real-time** en control de procesos), en salud la **privacidad** y la trazabilidad, y en telco la integración con infraestructura de red y gestión de slices. Para cada dominio conviene definir un mapa de requisitos que incluya **latencia** objetivo, criticidad de la decisión, volumen de datos por hora y requisitos regulatorios. Este mapeo guía la selección de hardware (por ejemplo, usar **Jetson/NVIDIA** cuando hay vídeo y modelos pesados o microcontroladores con aceleradores **NPU** para sensores con baja potencia) y la estrategia de despliegue (centrado en gateways vs. completamente distribuido).

La validación de casos de uso debe incluir pruebas en entorno representativo: simulación de cargas (emular sensores a escala), pruebas de desconexión forzada, escenarios de degradación y tests de **seguridad** (**pen testing** en nodos). Además, es recomendable instrumentar pipelines que registren métricas de precisión de modelos locales frente a su contraparte en la nube, **latencia** de decisión y **coste** por transacción para iterar sobre el diseño. Sólo con métricas reproducibles es posible justificar ampliaciones o cambios de arquitectura y comparar alternativas (más nube vs. más borde) en términos de **TCO** y calidad de servicio.

El **edge** resulta especialmente valioso cuando la rapidez de respuesta importa, cuando hay mucho volumen de datos o cuando la **privacidad** exige que cierta información no salga del entorno local. En la industria, el objetivo suele ser evitar paradas y reducir fallos; en salud, proteger datos sensibles y avisar a tiempo a personal médico; en telecomunicaciones, aprovechar **5G** para ofrecer experiencias interactivas sin **latencia** apreciable.

Antes de diseñar una solución, es útil mapear los requisitos: **latencia** objetivo, volumen de datos por hora, criticidad de la decisión y obligaciones regulatorias. Con esos datos se decide el hardware (por ejemplo, usar aceleradores para vídeo) y la estrategia (más lógica en gateways o en el propio dispositivo).

Las pruebas deben incluir simulaciones a escala, desconexiones controladas y medidas de comparación entre la precisión del modelo local y su versión centralizada. Estos ensayos permiten estimar el **retorno de la inversión** y decidir si escalar el despliegue.

### Ejemplos, casos y recursos
- Ejemplos prácticos: plataformas de gestión de flotas, sistemas de monitoreo de salud que alertan solo ante anomalías, cámaras que procesan video y envían metadatos.
- Casos reales: **Siemens**, **Bosch**, **Jaguar Land Rover**, **Philips Healthcare** – En manufactura, **Siemens** usa **edge** para mantenimiento predictivo, reduciendo downtime 30%.
- Recursos: **Intel Edge AI** (https://www.intel.com/content/www/us/en/artificial-intelligence/edge-ai.html) – Kit de desarrollo con casos prácticos.
- Infografía: ![Fog vs Mist](fog-mist-hierarchy.svg)

**Resumen:** Casos de **edge** varían por dominio, con mapeo de **latencia** y pruebas para validación, como en **Siemens** para industrial y **Philips** para salud, optimizando **TCO** y calidad en despliegues distribuidos.

**Preguntas de reflexión**
- ¿Qué métrica justifica mantener un modelo local frente a uno central?
- ¿Cómo simularías desconexiones para probar resiliencia?
- ¿Qué trade-off aceptas al quantizar un modelo?

## 5.4 Herramientas y plataformas
- **AWS IoT Greengrass / AWS Wavelength**
- **Azure IoT Edge / Azure Stack Edge**
- **Google Distributed Cloud Edge**
- **EdgeX Foundry**, **K3s (Rancher)**, **Balena**, **OpenNESS**
- Frameworks **ML**: **TensorFlow Lite**, **ONNX Runtime**, **NVIDIA Jetson/TensorRT**

### Ejemplos
- Despliegue de **K3s** en gateways con **contenedores** que exponen **APIs REST** para la lógica local.

### Casos reales
- **EdgeX Foundry** implementado por integradores para unificar telemetría en fábricas, como en **Bosch** para IoT industrial.

### Enlaces
- **EdgeX Foundry**: https://www.edgexfoundry.org – Plataforma open-source con demos para IoT edge.
- **K3s**: https://k3s.io – Guía ligera de Kubernetes para edge, con ejemplos de código.
- **Balena**: https://www.balena.io – Casos de despliegue OTA en dispositivos remotos.

### Infografía
![Cloud ROI](cloud-roi.svg)

## 5.5 Ventajas clave del edge computing

El valor del **edge** suele entenderse mejor con ejemplos prácticos: imagina una línea de producción en la que un sensor detecta vibraciones anómalas. Si ese dato tiene que viajar hasta la nube y volver, la reacción puede llegar demasiado tarde; con procesamiento en el borde, la máquina puede reducir ritmo o apagarse automáticamente, evitando daños mayores. Ese tipo de mejoras se traducen en métricas sencillas y útiles para la toma de decisiones: **latencia** desde la detección hasta la acción, porcentaje de decisiones resueltas localmente, ahorro en GB transferidos y reducción del tiempo de parada no planificado. Para proyectos educativos o pilotos, medir estas variables antes y después del despliegue proporciona una historia clara sobre el impacto del **edge**.

En un lenguaje claro: si el objetivo del negocio es reducir tiempos de respuesta o ahorrar en comunicaciones, el **edge** puede ser la herramienta adecuada. Los equipos deben definir desde el principio las métricas clave (**SLA** de **latencia**, umbrales de alertas, volumen de datos esperado) y diseñar experimentos que permitan medir mejoras de forma objetiva. Estas métricas facilitan también la comunicación con dirección y finanzas, porque enlazan el trabajo técnico con resultados medibles que impactan al negocio.

- **Latencia reducida**: Procesar datos cerca de su origen permite respuestas en tiempo real, crucial en aplicaciones como vehículos autónomos o control industrial.
![Edge vs Cloud](edge-vs-cloud.svg)
- **Ahorro de ancho de banda**: Al filtrar y procesar datos localmente, se reduce la cantidad de información que viaja a la nube, lo que ahorra **costes** de transmisión.
- **Mayor privacidad**: Los datos sensibles pueden ser procesados y almacenados localmente, minimizando riesgos de exposición.
- **Resiliencia operacional**: La capacidad de operar de forma autónoma en caso de pérdida de conexión con la nube.

### Ejemplos
- Medir **latencia** antes y después del despliegue para validar cumplimiento de **SLA**.
- Cuantificar GB/día ahorrados tras implementar filtrado local.

### Casos reales
- Empresas manufactureras como **Siemens** que han reducido tiempos de parada tras implementar detección local de fallos, ahorrando millones en mantenimiento.

### Enlaces
- **Azure IoT Edge**: https://azure.microsoft.com/en-us/services/iot-edge/ – Tutoriales con labs virtuales para probar ventajas en resiliencia.

### Infografía

**Resumen:** Las **ventajas** del **edge** incluyen **latencia reducida**, **ahorro de ancho de banda** y **mayor privacidad**, con herramientas como **K3s** y **EdgeX**, aplicadas en **Siemens** para mantenimiento, midiendo impacto con KPIs como **SLA** para ROI claro.

## 5.6 Limitaciones y retos

Desplegar **edge** a escala introduce retos operativos que conviene explicar sin tecnicismos: imagina tener cientos de pequeñas cajas conectadas por la ciudad. Cada una necesita actualizaciones, parches y supervisión; sin una plataforma que automatice estos procesos, el **coste** humano crece rápido. Por eso las mejores prácticas pasan por automatizar despliegues (**OTA**), monitorizar de forma centralizada y diseñar planes de recuperación que permitan que los dispositivos sigan funcionando con capacidades limitadas cuando la conexión a la nube falla.

En **seguridad**, la recomendación práctica es combinar medidas de software y hardware: usar arranque seguro para evitar que un dispositivo ejecute código malicioso, almacenar claves en módulos seguros tipo **TPM**, y cifrar comunicaciones. Pero no basta con tecnologías: hay que operar con procesos claros: inventario de dispositivos, ciclos de parcheo definidos, y pruebas periódicas de **seguridad**. Con estas prácticas se reduce el riesgo y se facilita la escalabilidad del proyecto.
Retos: mayor complejidad operativa (despliegue y parcheo masivo), **coste inicial** por nodos distribuidos, gestión de versiones de modelos y heterogeneidad de hardware.
**Seguridad**: cada nodo **edge** es una superficie de ataque. Medidas recomendadas: arranque seguro (**Secure Boot**), uso de **TPM/HSM** para gestión de claves, cifrado en tránsito y reposo, autenticación mutua (**mTLS**), gestión centralizada de parches y monitoreo (**SIEM/EDR**). También es importante diseñar estrategias de fallback para operar en modo desconectado.

### Ejemplos
- Estrategia **OTA** para actualizar modelos de inferencia con canary rolls y rollback automático.

### Casos reales
- Operadores telco como **Verizon** que automatizan parches de **seguridad** en nodos **MEC** y gateways, reduciendo vulnerabilidades en 5G.

### Enlaces
- Guía **mTLS / TLS mutuo**: https://www.openssl.org – Documentación técnica con ejemplos de código para autenticación edge.
- **OWASP IoT Security**: https://owasp.org/www-project-internet-of-things/ – Checklist didáctica para mitigar riesgos en despliegues distribuidos.

### Infografía
![Decision flow](decision-flow.svg)

**Resumen:** Los **retos** del **edge** incluyen complejidad operativa y **seguridad distribuida**, como en **Verizon** con parches **OTA**, requiriendo **TPM** y **mTLS** para fallback y escalabilidad, equilibrando beneficios con gestión proactiva.

**Tabla retos vs mitigación ampliada**
| Reto | Causa raíz | Impacto negocio | Mitigación técnica | Métrica seguimiento |
|------|-----------|----------------|--------------------|---------------------|
| Gestión masiva | Heterogeneidad HW | Escala lenta | Orquestación ligera (K3s) | Nº nodos gestionados/operador |
| Seguridad física | Acceso a dispositivos | Compromiso datos | Secure Boot + TPM | % dispositivos con firmware verificado |
| Versionado modelos | Releases frecuentes | Inconsistencia inferencia | Registro + canary | Tasa éxito despliegues |
| Latencia variable | Red inestable | SLA incumplido | Buffer + fallback local | p95 latencia acción |
| Coste oculto | Tráfico no filtrado | Gasto banda | Preprocesado en gateway | GB ahorrados/mes |

## 5.7 Costes y retorno de la inversión (ROI)

Hablar de **costes** suele asustar a las organizaciones, pero lo más útil es transformar **costes** en hipótesis que podamos validar con pilotos. Un piloto bien diseñado estima tanto **costes directos** (hardware, energía, comunicaciones) como beneficios tangibles (reducción de paradas, ahorro en ancho de banda, mejora en tiempos de respuesta). Una vez puestos números sobre la mesa, se puede comparar la alternativa «todo en la nube» frente a «procesado parcial en el borde» con claridad.

Además, hay modelos mixtos: en lugar de comprar y mantener todo el hardware, es posible contratar servicios gestionados de **edge** o alquilar nodos en modalidad "**as-a-service**". Estos modelos reducen la barrera de entrada y permiten validar hipótesis sin comprometer grandes inversiones iniciales. Para presentar **ROI**, conviene mostrar escenarios (optimista, realista, conservador) y el plazo esperado de recuperación, normalmente en meses a uno o dos años dependiendo del caso.

**Ejemplos y casos reales:**

- **Ejemplo:** **Jaguar Land Rover** calculó **ROI** de **edge** en telemetría vehicular, recuperando inversión en 12 meses por reducción de downtime.
- **Caso real:** **Amazon Wavelength** ofrece **edge as-a-service** para desarrolladores, bajando **costes** iniciales en 70% vs. hardware propio.
- **Enlace:** [ROI Edge - CloudTweaks](https://cloudtweaks.com/2025/09/cloud-exit-economics-real-world-roi-financial-models/) – Modelo financiero con calculadoras interactivas para escenarios edge.
- **Tabla comparativa rápida:**

| Escenario     | Coste Inicial | ROI Tiempo | Ejemplo              |
| ------------- | ------------- | ---------- | -------------------- |
| Piloto        | Bajo          | 6 meses    | Jaguar Land Rover    |
| As-a-service  | Medio         | 12 meses   | Amazon Wavelength    |
| Full Deploy   | Alto          | 18-24 meses| Siemens (industrial) |

**Resumen:** **Costes** en **edge** se validan con pilotos para **ROI** rápido, como en **Jaguar Land Rover** (12 meses), usando modelos **as-a-service** para minimizar inversión inicial y maximizar resiliencia.

### Mini calculadora conceptual (texto)

> ROI ≈ (Ahorro anual paradas + Ahorro ancho de banda + Reducción soporte) – (CapEx hardware + OpEx gestión + Formación)

### Indicadores recomendados

- % reducción downtime
- p95 latencia decisión
- GB filtrados local vs crudos
- Tiempo despliegue nodo (min)
- Coste operativo mensual / nodo

## 5.8 Lecturas, referencias y cierre práctico

Para cerrar, proponemos una pequeña guía práctica: empezar por un piloto corto y medible, seleccionar 3 **KPIs** (**latencia**, GB/día, reducción de downtime), automatizar despliegues y asegurar trazabilidad de cambios. A partir de los resultados del piloto se decide escala y modelo de operación.

### Ejemplos, casos, enlaces y tabla resumen
- Casos reales: **Siemens**, **Bosch**, **Philips Healthcare**, **Jaguar Land Rover**, **Amazon Wavelength** – **Siemens** integra **edge** con IA para fábricas inteligentes.
- Enlaces y recursos: [AWS Edge overview](https://aws.amazon.com/edge/) – Portal con whitepapers y labs gratuitos.
- [Intel Edge AI](https://www.intel.com/content/www/us/en/artificial-intelligence/edge-ai.html) – Recursos educativos con videos.
- [EdgeX Foundry](https://www.edgexfoundry.org) – Comunidad open-source con foros.
- [Balena](https://www.balena.io) – Plataforma con casos de IoT edge.
- Ejemplos prácticos: cámaras que envían metadatos, **PLCs** con detección local de vibraciones, gateways que agregan y normalizan telemetría.

Tabla resumen (**KPIs / Beneficio / Ejemplo**):

| KPI | Beneficio | Ejemplo |
|---|---|---|
| Latencia E2E | Respuesta en tiempo real | Frenado asistido en vehículos (**ADAS**) |
| GB transferidos/día | Ahorro de comunicaciones | Cámaras que envían metadatos en vez de video crudo |
| % decisiones locales | Resiliencia y rapidez | Control local de robots industriales |
| Reducción downtime | Ahorro operativo | Detección temprana de fallos en líneas de producción |
| TCO por nodo | Planificación financiera | Comparativa coste transmisión vs. coste nodo edge |

**Resumen:** Guía práctica para **edge**: inicia con pilotos midiendo **KPIs** clave, usando recursos como **AWS** y **Intel**, con casos como **Siemens** demostrando escalabilidad, cerrando con automatización para operación eficiente.

## Tabla síntesis — Capítulo 5

| Capa | Latencia típica | Ejemplo | Decisión local |
|------|-----------------|---------|----------------|
| Mist | < 10 ms | Wearable | Muy limitada |
| Edge | 10–50 ms | Gateway industrial | Alta |
| Fog | 50–200 ms | Nodo regional | Media |
| Nube | > 200 ms | Región cloud | Baja |

## Tips y curiosidades — Capítulo 5

- Tip: mide P95/P99 de latencia end‑to‑end en pilotos edge, no solo media.
- Tip: automatiza OTA con firmas y rollback seguro.
- Curiosidad: algunas fábricas ya operan “islas” edge desconectadas durante horas.

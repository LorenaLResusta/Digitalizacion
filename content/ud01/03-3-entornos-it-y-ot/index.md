+++
title = "3. Entornos IT y OT"
weight = 3
+++

La convergencia entre los entornos IT (Tecnologías de la Información) y OT (Tecnologías de Operación) es fundamental en la digitalización industrial. Ambos entornos tienen características y objetivos distintos, pero su integración permite optimizar procesos y mejorar la toma de decisiones.

## 3.1 Entorno IT

El entorno IT se centra en la gestión de datos, aplicaciones y comunicaciones. Incluye sistemas que permiten el procesamiento y análisis de información, así como la interacción con los usuarios y otros sistemas. Las principales características son:

- **Enfoque de la información**: garantizar la disponibilidad, integridad y confidencialidad de los datos que soportan los procesos de negocio.
- **Sistemas empresariales**: ERP, CRM, SCM, etc.
- **Desarrollo de Software**: metodologías ágiles, DevOps, integración continua, pruebas automatizadas.
- **Comunicaciones**: gestiona la comunicación interna y externa, incluyendo correo electrónico, mensajería instantánea y videoconferencias.
- **Ciberseguridad**: protección de datos y redes, gestión de identidades y accesos, cumplimiento normativo.

Normalmente las empresas, los departamentos típicos de IT incluyen:

- Desarrollo de Software
- Infraestructura y Redes
- Soporte Técnico
- Seguridad Informática
 
## 3.2 Entorno OT

El entorno OT se enfoca en el control y supervisión en tiempo real de procesos físicos y maquinaria, priorizando la seguridad de personas y activos, la disponibilidad y el determinismo. Los cambios se planifican en paradas controladas y los equipos tienen ciclos de vida largos. La continuidad operativa y la estabilidad pesan más que la rapidez de cambio típica de IT.

Elementos característicos:

- Enfoque en operaciones físicas: Se centran en los sistemas que interactúan directamente con los procesos físicos del mundo real. PLC/PAC, DCS, SIS (sistemas instrumentados de seguridad), lazos de control e instrumentación (sensores y actuadores).
- Tiempo real: Respuesta inmediata, para controlar y supervisar eventos y condiciones cambiantes.
- Automatización industrial: SCADA, HMI y servidores de históricos (data historians).
- Seguridad industrial: Protección de personas y activos, gestión de riesgos y cumplimiento normativo. Actualmente la ciberseguridad irrumpe con fuerza debido al IoT.

## 3.3 Diferencias entre IT y OT

| Característica | IT (Tecnologías de la Información) | OT (Tecnologías de Operación) |
|----------------|------------------------------------|-------------------------------|
| Objetivo | Gestión de datos, aplicaciones y comunicaciones | Control y supervisión de procesos físicos y maquinaria |
| Alcance | Procesos de negocio y soporte | Procesos productivos y de campo |
| Ejemplos | ERP, CRM, correo, portales, BI | SCADA/HMI, PLC/DCS, sensores/actuadores |
| Prioridades | Confidencialidad > Integridad > Disponibilidad (CIA) | Seguridad de personas/activos > Disponibilidad > Integridad > Confidencialidad |
| Disponibilidad | Alta, tolera paradas planificadas | Muy alta 24/7, paradas mínimas y controladas |
| Tiempo real | No determinista; latencias variables | Determinista; baja latencia y respuesta inmediata |
| Ventanas de mantenimiento | Frecuentes y flexibles | En paradas programadas de planta |
| Ciclo de vida | 3–5 años (hardware/software) | 10–20+ años (equipos industriales) |
| Protocolos | TCP/IP, HTTP(S), REST, SQL, MQTT | Modbus, OPC UA, Profibus/Profinet, EtherNet/IP, DNP3 |
| Arquitectura de red | VLAN/SDN, firewalls TI, Zero Trust | Zonas y conductos (ISA/IEC 62443), DMZ industrial, segmentación celda/área |
| Cambios y despliegues | Frecuentes, CI/CD, automatizados | Poco frecuentes, gestión de cambios estricta, validación previa |
| Ciberseguridad | EDR/SIEM, IAM/MFA, parcheo regular | Hardening de controladores, listas blancas, control de puertos/protocolos, gestión de firmware |
| Cumplimiento | ISO 27001, RGPD, SOX | IEC 62443, ISA-95, IEC 61508/61511 (seguridad funcional) |
| Entorno operativo | Oficinas, CPD, nube | Planta industrial, condiciones ambientales severas |
| Consecuencias del fallo | Pérdida de servicio o datos, impacto financiero/reputacional | Riesgo para personas, daños a equipos, paradas de producción |
| Monitorización | APM/NPM, SIEM, observabilidad | SCADA/HMI, historiadores (data historians), OEE |
| Integración y datos | ESB/APIs, data lakes/warehouses, ACID | Gateways OT/IT, edge computing, precisión de señales y trazabilidad |
| Personal y competencias | Desarrolladores, sysadmins, DevOps, seguridad TI | Ingenieros de control/automatización, instrumentación, mantenimiento, ciberseguridad OT |

## 3.4 Integración IT/OT

La integración IT/OT alinea datos y control operativo con sistemas corporativos, que tradicionalmente han estado aislados. La IT se centra en la gestión de datos y la analítica y la OT se enfoca en el control de procesos. La convergencia IT/OT permite:

## Beneficios de la integración IT/OT

- Mayor visibilidad y control sobre los procesos productivos.
- Optimización de recursos y reducción de costes operativos.
- Mejora en la toma de decisiones basada en datos en tiempo real.
- Incremento de la flexibilidad y capacidad de respuesta ante incidencias.

## Ejemplo de integración IT/OT

La conexión de sensores industriales (OT) con sistemas de análisis de datos (IT) permite monitorizar el estado de la maquinaria y anticipar posibles fallos, facilitando el mantenimiento predictivo.

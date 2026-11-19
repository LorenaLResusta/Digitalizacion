+++
title = "4. Entornos IT y OT"
weight = 5
+++

## 4.1 Concepto

- **IT (Information Technology, tecnologías de la información)**: sistemas que gestionan **datos e información** de negocio: ordenadores, servidores, redes corporativas, correo, ERP, CRM, bases de datos.
- **OT (Operational Technology, tecnologías de operación)**: sistemas que **supervisan y controlan procesos físicos**: autómatas programables (PLC), sistemas SCADA, sensores, actuadores, robots, sistemas de control de climatización o energía.

## 4.2 Diferencias y similitudes

| Aspecto | IT | OT |
|---------|----|----|
| Objetivo | Gestionar información | Controlar procesos físicos |
| Prioridad | Confidencialidad de los datos | Disponibilidad y seguridad física de las personas |
| Tiempo de respuesta | Segundos son aceptables | Milisegundos, a menudo en tiempo real |
| Vida útil de los equipos | 3–5 años | 15–20 años o más |
| Actualizaciones | Frecuentes, automáticas | Escasas y planificadas (parar una línea cuesta dinero) |
| Protocolos | TCP/IP, HTTP, SQL | Modbus, Profinet, OPC UA, protocolos de campo |
| Quién lo gestiona | Departamento de sistemas | Ingeniería, mantenimiento, producción |

**Similitudes:** ambos usan hardware y software, ambos trabajan cada vez más sobre redes IP, ambos generan datos valiosos y ambos son objetivo de ciberataques.

## 4.3 La convergencia IT/OT y su importancia

Durante décadas, IT y OT vivieron separados. Hoy se tiende a la **convergencia IT/OT**: los datos de la planta llegan a los sistemas de gestión y las decisiones de negocio llegan a la planta.

**Por qué es importante conectarlos:**

- La dirección ve en tiempo real cuánto se produce y cuánto cuesta.
- Los pedidos de clientes se trasladan directamente a la planificación de producción.
- El mantenimiento pasa de reactivo (arreglar cuando se rompe) a **predictivo** (anticipar la avería con datos).
- Se reduce el consumo energético al medir y ajustar.
- Se mejora la trazabilidad: se sabe qué lote se fabricó, cuándo, con qué materiales y para qué cliente.

**Riesgos:** al conectar OT con IT, la planta queda expuesta a amenazas que antes no llegaban a ella. Por eso la convergencia exige **segmentar las redes**, controlar accesos y aplicar normas específicas de ciberseguridad industrial (por ejemplo, la familia de normas **IEC 62443**).

## 4.4 La pirámide de automatización

La integración IT/OT se suele representar con la **pirámide de automatización** (modelo ISA-95):

| Nivel | Nombre | Sistemas | Entorno |
|-------|--------|----------|---------|
| 4 | Gestión empresarial | ERP, CRM | IT |
| 3 | Gestión de la producción | MES | Frontera IT/OT |
| 2 | Supervisión | SCADA, HMI | OT |
| 1 | Control | PLC, controladores | OT |
| 0 | Campo | Sensores y actuadores | OT |

## 4.5 Tecnologías típicas en planta y en negocio

| En planta (OT) | En negocio (IT) |
|----------------|-----------------|
| Sensores IoT y PLC | ERP y CRM |
| SCADA y HMI | Comercio electrónico |
| Robots y cobots | Herramientas colaborativas en la nube |
| Visión artificial para control de calidad | Business intelligence y cuadros de mando |
| Gemelos digitales de máquinas | Firma y facturación electrónicas |
| Mantenimiento predictivo | Automatización de procesos (RPA) |

**Ejemplo en Juniverse Studio:** el plató tiene focos, climatización y un sistema de control de energía (OT). Si esos datos se conectan con el sistema de planificación de rodajes (IT), la empresa podría saber el coste energético real de cada curso y programar los rodajes en las horas de energía más barata.

## Autoevaluación (Capítulo 4)

- ¿Por qué en OT la disponibilidad es más importante que la confidencialidad?
- Clasifica como IT u OT: *SCADA*, *CRM*, *PLC*, *correo corporativo*, *sensor de temperatura*, *ERP*.
- Explica un riesgo de conectar la planta a la red corporativa y una medida para reducirlo.

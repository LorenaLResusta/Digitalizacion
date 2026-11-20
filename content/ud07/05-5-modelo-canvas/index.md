+++
title = "5. Modelo canvas"
weight = 5
+++

El **Business Model Canvas** es una herramienta visual para describir cómo una organización crea, entrega y captura valor. Es especialmente útil en proyectos de transformación porque obliga a mirar **el conjunto**, no solo la tecnología.

```mermaid
flowchart TB
    subgraph CANVAS[Business Model Canvas (resumen)]
        VP[Propuesta de valor]
        CS[Segmentos de clientes]
        CH[Canales]
        CR[Relación con clientes]
        R[Fuentes de ingresos]
        K[Recursos clave]
        A[Actividades clave]
        P[Socios clave]
        C[Estructura de costes]
    end
    CS --> VP --> CH
    VP --> R
    K --> A --> VP
    P --> A
    C --> R
```

_Canvas como “mapa” del modelo de negocio y sus dependencias._

## ¿Cómo usarlo en un proyecto de transformación?

1. Rellenar una versión **actual (AS-IS)**.
2. Proponer una versión **objetivo (TO-BE)** tras la transformación.
3. Identificar qué bloques cambian y qué implica (procesos, datos, roles).

## Ejemplo (muy simplificado)

- Propuesta de valor: “Trámites 100% online con seguimiento en tiempo real”.
- Canales: web, app, kioscos.
- Recursos clave: plataforma de identidad, soporte, integraciones.
- Costes: licencias, formación, mantenimiento.

**Conceptos clave:** **Canvas**, **AS-IS / TO-BE**, **propuesta de valor**, **costes**, **ingresos**.

**Caso real (simplificado):** una academia quería “clases híbridas”. Con Canvas, vieron que también cambiaban canales, relación con clientes, actividades clave y costes (soporte, grabación, plataforma). Eso evitó subestimar el esfuerzo.

## Autoevaluación

1. ¿Qué significa trabajar con un Canvas **AS-IS** y un Canvas **TO-BE**?
2. Si cambia el bloque “Canales”, ¿qué otros bloques podrían verse afectados? (cita al menos dos)
3. ¿Qué bloque del Canvas crees que más se subestima en proyectos de transformación y por qué?

> **Enlace recomendado:** [Business Model Canvas (Wikipedia)](https://es.wikipedia.org/wiki/Business_Model_Canvas).

Volver al índice

---

<a id="gestion-proyectos"></a>

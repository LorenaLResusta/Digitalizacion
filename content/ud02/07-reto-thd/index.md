+++
title = "Reto THD"
weight = 7
+++

## Objetivo (UD02)

Caracterizar y aplicar las Tecnologías Habilitadoras Digitales (THD) en el contexto de Moda Urbana. Selecciona 2–3 THD (p. ej., IoT/RFID, IA/ML, Big Data/Analítica, Nube/Edge/5G, RA/RV, Blockchain, Impresión 3D, Ciberseguridad IT/OT, Gemelos digitales, Robótica colaborativa) y define casos de uso con valor claro para negocio y cliente.

## THD y capas (qué usar y para qué)

- IoT/RFID: sensores y etiquetas para stock en tiempo real, condiciones de transporte y mantenimiento.
- IA/ML: recomendaciones, previsión de demanda, detección de fraude/devoluciones anómalas.
- Big Data/Analítica: métricas unificadas (único punto de verdad), paneles y decisiones casi en tiempo real.
- Nube/Edge/5G: procesamiento en el borde para baja latencia; escalado en nube; conectividad en tienda.
- RA/RV: probadores aumentados, formación y soporte de mantenimiento.
- Blockchain: trazabilidad de proveedores, certificados de prendas y cadena de custodia.
- Impresión 3D: útiles y repuestos rápidos; pilotos de personalización limitada.
- Ciberseguridad IT/OT: protección de POS, redes de tienda y datos de clientes.
- Gemelos digitales: simulación de layouts y flujos de tienda para mejorar conversión y operaciones.
- Robótica colaborativa: apoyo en almacén/tienda (reposición, conteo) donde sea viable.

## Ejemplos de uso clave

- IoT + 5G/Edge: inventario con RFID en tiempo real y alertas de rotura de stock.
- IA/ML: recomendador de outfits y previsión de tallas por tienda.
- RA en probador: sugerencia de tallas y combinaciones sin cambiarse.
- Blockchain: trazabilidad de origen y materiales en prendas “eco”.
- Gemelo digital: simular disposición de tienda para aumentar conversión y reducir colas.

## Áreas a cubrir
 
- Conectividad y plataforma (nube, edge, 5G/Wi‑Fi).
- IoT/RFID y logística.
- Datos y analítica (lakehouse/BI) y gobierno del dato.
- IA/ML y personalización.
- Ciberseguridad (IT y OT) y privacidad (RGPD/consentimiento).
- RA/RV, impresión 3D, blockchain y gemelos digitales (si aplica al caso).

## Entregables (UD02)

- Mapa THD → caso de uso (qué tecnología y para qué).
- Diseño de 2–3 casos de uso con flujos simples y diagrama por caso.
- Riesgos y consideraciones (seguridad, privacidad, coste, viabilidad).
- Referencia a UD03 para dependencias técnicas y seguridad.

## Paso a paso (UD02, 90–120 min)

1. Elige 2–3 THD y el problema a resolver (p. ej., roturas de stock, colas, baja conversión, trazabilidad).
2. Define el caso de uso por THD: objetivo, entradas de datos, proceso y salida/acción.
3. Dibuja un flujo sencillo (cajas y flechas) y anota las dependencias técnicas.
4. Define 3 KPIs por caso y un objetivo (p. ej., “latencia < 200 ms”, “precisión ≥ 80%”, “reducción de roturas −30%”).
5. Señala riesgos y cómo mitigarlos (seguridad, privacidad, costes, operación).

## Ejemplo de Plantilla de entrega (UD02). No es un modelo, es un ejemplo

Título: THD aplicadas a Moda Urbana (UD02)

Casos de uso (resumen):

| THD | Caso de uso | Valor esperado | KPIs | Riesgos/Mitigación |
|---|---|---|---|---|
| IoT/RFID + Edge | Inventario en tiempo real | Menos roturas, reposición más rápida | % stock correcto, alertas/semana, latencia | Privacidad en tienda, coste RFID → pilotos por sección |
| IA/ML (recomendador) | Outfit personalizado | + Conversión y ticket medio | Conversión, AOV, precisión | Sesgos → revisar métricas por segmento |
| RA en probador | Talla sugerida | Menos devoluciones, mejor experiencia | % acierto de talla, NPS | Higiene de dispositivos, mantenimiento |

Flujo simple (un ejemplo):

```text
Sensor/Evento -> Edge/Nube -> Lógica/Modelo -> Acción (alerta/recomendación) -> KPI medido
```

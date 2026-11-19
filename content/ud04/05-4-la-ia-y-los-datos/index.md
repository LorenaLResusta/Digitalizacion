+++
title = "4. La IA y los datos"
weight = 5
+++

## 4.1 Los datos, combustible de la IA

Un modelo de IA es tan bueno como los datos con los que se entrena. Los problemas de los datos se convierten en problemas del modelo:

- **Datos escasos** → el modelo no generaliza.
- **Datos sesgados** → el modelo discrimina (por ejemplo, un sistema de selección entrenado con contrataciones pasadas puede reproducir sesgos de género).
- **Datos desactualizados** → el modelo deja de acertar cuando cambia la realidad.

## 4.2 IA, big data y rentabilidad

La relación es un círculo: la empresa **recoge datos masivos** (big data) → los **analiza** con IA → obtiene **predicciones y automatizaciones** → mejora decisiones, reduce costes o aumenta ventas → genera **más datos** para seguir mejorando.

**Ejemplo:** la cadena de tiendas usa el histórico de ventas, el tiempo meteorológico y el calendario de festivos para prever la demanda de cada prenda en cada tienda. Si la previsión reduce un 10 % el stock que acaba en rebajas, la mejora de margen puede pagar el proyecto.

## 4.3 Minería de datos

La **minería de datos** (*data mining*) es el proceso de descubrir patrones útiles en grandes conjuntos de datos. Técnicas habituales:

| Técnica | Pregunta que responde | Ejemplo |
|---------|-----------------------|---------|
| **Clasificación** | ¿A qué categoría pertenece? | ¿Este cliente se dará de baja? |
| **Regresión** | ¿Qué valor numérico tendrá? | ¿Cuántas unidades venderemos? |
| **Agrupamiento (clustering)** | ¿Qué grupos naturales hay? | Tipos de clientes |
| **Reglas de asociación** | ¿Qué cosas suelen ir juntas? | Quien compra X suele comprar Y |
| **Detección de anomalías** | ¿Qué es raro? | Transacciones sospechosas |

## 4.4 Protección de datos en proyectos de IA

Cuando un sistema de IA usa **datos personales**, se aplica el RGPD:

- Debe existir una **base legal** para el tratamiento.
- Hay que **informar** a las personas y respetar sus derechos.
- Se aplica la **minimización**: usar solo los datos necesarios.
- Las personas tienen derecho a **no ser objeto de decisiones exclusivamente automatizadas** con efectos jurídicos o significativos (art. 22 RGPD), salvo excepciones.
- Puede ser necesaria una **evaluación de impacto** (EIPD).

**En la práctica:** no se deben introducir datos personales de clientes ni información confidencial en herramientas de IA públicas sin que la empresa lo haya autorizado y haya revisado las condiciones del servicio.

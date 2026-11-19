+++
title = "5. Ingeniería de datos y ciencia de datos"
weight = 6
+++

## 5.1 Etapas de la ingeniería de datos

La **ingeniería de datos** construye los «tubos» por los que circulan los datos (*pipelines*):

| Etapa | Qué se hace |
|-------|-------------|
| **1. Ingesta** | Recoger datos de las fuentes: bases de datos, APIs, archivos, sensores |
| **2. Almacenamiento** | Guardarlos en el repositorio adecuado (lago, almacén, base de datos) |
| **3. Transformación** | Limpiar, unificar formatos, eliminar duplicados, enriquecer (procesos **ETL** o **ELT**: extraer, transformar y cargar) |
| **4. Orquestación** | Programar y encadenar los procesos para que se ejecuten automáticamente |
| **5. Servicio** | Poner los datos a disposición de informes, cuadros de mando o modelos de IA |
| **6. Gobierno y calidad** | Documentar, controlar accesos y vigilar la calidad |

## 5.2 Etapas de la ciencia de datos

La **ciencia de datos** usa esos datos para responder preguntas. Un proceso típico:

1. **Entender el negocio**: ¿qué problema queremos resolver?
2. **Obtener los datos.**
3. **Preparar los datos**: limpieza y transformación (suele llevar la mayor parte del tiempo).
4. **Explorar**: estadística descriptiva y gráficos para descubrir patrones.
5. **Modelar**: aplicar técnicas estadísticas o de machine learning.
6. **Evaluar**: ¿el modelo responde bien a la pregunta inicial?
7. **Comunicar y desplegar**: informes, cuadros de mando o integración en una aplicación.
8. **Mantener**: vigilar que el modelo siga funcionando con datos nuevos.

| Perfil | Papel |
|--------|-------|
| **Ingeniería de datos** | Construye y mantiene la infraestructura y los flujos de datos |
| **Análisis de datos** | Explora, crea informes y cuadros de mando |
| **Ciencia de datos** | Crea modelos predictivos y responde preguntas complejas |
| **Ingeniería de ML / MLOps** | Lleva los modelos a producción y los mantiene |

## 5.3 Objetivos de la ciencia de datos en la empresa

- **Conocer mejor al cliente**: segmentación, personalización, prevención de bajas.
- **Optimizar operaciones**: previsión de demanda, rutas, inventarios, turnos.
- **Reducir riesgos**: detección de fraude, mantenimiento predictivo, ciberseguridad.
- **Crear nuevos productos y servicios** basados en datos.
- **Tomar decisiones basadas en evidencias** en lugar de en intuiciones.

**Ejemplo en Juniverse Studio:** analizar en qué minuto abandonan los alumnos los vídeos para rediseñar los cursos, y prever qué temas tendrán más demanda el próximo trimestre.

## Autoevaluación (Capítulos 4 y 5)

- ¿Qué tipo de almacenamiento elegirías para guardar los vídeos de los cursos? ¿Por qué?
- Explica la regla 3-2-1.
- ¿Qué diferencia hay entre un data lake y un data warehouse?
- ¿Cuál suele ser la etapa que más tiempo consume en un proyecto de ciencia de datos?

+++
title = "4. Almacenamiento de datos en la nube"
weight = 5
+++

## 4.1 Tipos de almacenamiento

| Tipo | Cómo organiza los datos | Uso típico | Ejemplos de servicios |
|------|-------------------------|------------|----------------------|
| **De archivos** | Carpetas y archivos, como en un disco | Documentos compartidos | Unidades compartidas, servicios de archivos en red |
| **De bloques** | Bloques de tamaño fijo, como un disco duro virtual | Discos de máquinas virtuales y bases de datos | Discos de servidores en la nube |
| **De objetos** | Objetos con identificador y metadatos, en «contenedores» o *buckets* | Copias de seguridad, vídeos, imágenes, datos para análisis | Amazon S3, Azure Blob Storage, Google Cloud Storage |

## 4.2 Bases de datos y repositorios de datos

| Sistema | Para qué sirve |
|---------|----------------|
| **Base de datos relacional (SQL)** | Datos estructurados y transacciones (pedidos, facturas, matrículas) |
| **Base de datos NoSQL** | Datos flexibles o con gran volumen (catálogos, sesiones, datos de sensores) |
| **Data warehouse (almacén de datos)** | Datos limpios y estructurados de varias fuentes, preparados para informes |
| **Data lake (lago de datos)** | Datos en bruto de cualquier formato, para análisis y entrenamiento de IA |
| **Data lakehouse** | Combina la flexibilidad del lago con la organización del almacén |

## 4.3 Procedimientos de almacenamiento en la nube

1. **Clasificar los datos** según su sensibilidad (públicos, internos, confidenciales, datos personales).
2. **Elegir la ubicación** (región del proveedor). Si hay datos personales, preferir la UE o asegurarse de que la transferencia internacional cumple el RGPD.
3. **Elegir la clase de almacenamiento** según la frecuencia de uso:
   - *Caliente*: acceso frecuente, más caro.
   - *Frío* o *archivo*: acceso ocasional, mucho más barato, con recuperación más lenta.
4. **Aplicar cifrado** en reposo y en tránsito.
5. **Configurar permisos** con el principio de **mínimo privilegio** y revisar que nada sea público por error.
6. **Activar versionado y copias de seguridad**, siguiendo la regla **3-2-1**: 3 copias, en 2 soportes distintos, 1 fuera de la ubicación principal (y, a ser posible, una copia inmutable o desconectada frente al ransomware).
7. **Definir políticas de ciclo de vida**: mover automáticamente a almacenamiento frío y borrar cuando vence el plazo.
8. **Monitorizar** accesos y costes.

## 4.4 Importancia del cloud computing para los datos

La nube ha hecho accesible a cualquier empresa lo que antes solo tenían las grandes: almacenamiento prácticamente ilimitado, capacidad de cálculo para analizar grandes volúmenes, servicios de IA listos para usar y pago por uso. Sin la nube, el big data y la IA estarían fuera del alcance de la mayoría de las pymes. (Repasa la [UD03]({{% relref "/ud03" %}}).)

+++
title = "2. Características de las principales THD"
weight = 3
+++

## 2.1 Inteligencia artificial, machine learning y deep learning

La **inteligencia artificial (IA)** es la disciplina que desarrolla sistemas capaces de realizar tareas que normalmente requieren inteligencia humana: reconocer imágenes, comprender lenguaje, predecir o tomar decisiones.

- **Machine learning (aprendizaje automático)**: los sistemas aprenden patrones a partir de datos en lugar de programar cada regla.
- **Deep learning (aprendizaje profundo)**: tipo de machine learning basado en redes neuronales de muchas capas, muy eficaz con imágenes, voz y texto.

**Aplicaciones:** recomendación de productos, chatbots, detección de fraude, previsión de demanda, visión artificial para control de calidad. La estudiaremos a fondo en la UD04.

## 2.2 Internet de las cosas (IoT)

El **IoT** es la conexión a internet de objetos físicos (sensores, máquinas, electrodomésticos, vehículos) que **recogen e intercambian datos** sin intervención humana. Cuando se aplica a la industria se habla de **IIoT** (*Industrial IoT*).

**Elementos:** dispositivo con sensor → conectividad (wifi, Bluetooth, LoRaWAN, 5G) → plataforma que recibe los datos → aplicación que los muestra o actúa.

**Ejemplo en tienda:** etiquetas RFID en la ropa que permiten saber en tiempo real qué prendas hay en el almacén, en el probador o en caja.

## 2.3 Redes 5G

La **quinta generación de telefonía móvil** aporta tres mejoras sobre 4G:

| Capacidad | Qué permite |
|-----------|-------------|
| **Gran ancho de banda** (eMBB) | Vídeo de alta calidad, realidad virtual móvil |
| **Muy baja latencia** (URLLC) | Control remoto de máquinas, vehículos conectados |
| **Conexión masiva de dispositivos** (mMTC) | Miles de sensores IoT en un área reducida |

Las empresas pueden desplegar **redes 5G privadas** en fábricas, puertos o almacenes.

## 2.4 Fibra óptica

La **fibra óptica** transmite datos mediante pulsos de luz por hilos de vidrio o plástico. Ofrece gran velocidad, baja latencia, inmunidad a interferencias electromagnéticas y largas distancias. Es la base de las redes troncales de internet y de los centros de datos, y la conexión habitual de empresas y hogares. Sin fibra no hay 5G útil: las antenas se conectan a la red mediante fibra.

## 2.5 Computación en la nube y computación difusa (edge/fog)

La **computación en la nube** ofrece recursos informáticos (servidores, almacenamiento, software) a través de internet, con pago por uso. La **computación en el borde (edge)** y la **niebla (fog)** acercan el procesamiento al lugar donde se generan los datos para reducir la latencia. Se desarrollan en profundidad en la [UD03]({{% relref "/ud03" %}}).

## 2.6 Tecnologías de procesamiento masivo de datos (big data)

El **big data** engloba las técnicas y herramientas para almacenar y analizar volúmenes de datos tan grandes, variados o rápidos que las herramientas tradicionales no pueden gestionarlos. Permite convertir datos en conocimiento para decidir. Lo veremos en la [UD05]({{% relref "/ud05" %}}).

## 2.7 Blockchain y tecnologías de registro distribuido (DLT)

Una **DLT** (*Distributed Ledger Technology*) es una base de datos compartida y sincronizada entre varios participantes, sin una autoridad central. **Blockchain** es un tipo de DLT en el que los registros se agrupan en **bloques encadenados** mediante funciones criptográficas (*hash*), de forma que modificar un bloque antiguo invalidaría todos los posteriores.

| | Blockchain | Otras DLT |
|---|-----------|-----------|
| Estructura | Cadena de bloques ordenados | Puede ser un grafo u otras estructuras |
| Consenso | Mecanismos como prueba de trabajo o de participación | Variado, a menudo más ligero |
| Similitudes | Registro distribuido, inmutable y verificable por los participantes | |

**Aplicaciones:** trazabilidad en la cadena de suministro (origen de un alimento o de una prenda), certificados académicos verificables, contratos inteligentes (*smart contracts*), criptomonedas.

**Cuándo no usarla:** si hay una autoridad de confianza y una base de datos tradicional resuelve el problema, blockchain suele añadir coste y complejidad sin beneficio.

## 2.8 Realidades inmersivas

| Tecnología | Qué hace | Ejemplo |
|------------|----------|---------|
| **Realidad virtual (RV)** | Sumerge a la persona en un entorno completamente digital | Simulador de formación en prevención de riesgos |
| **Realidad aumentada (RA)** | Superpone información digital sobre el entorno real | Ver instrucciones de montaje sobre la propia máquina con una tablet |
| **Realidad mixta (RM)** | Los objetos digitales interactúan con el entorno real | Técnico que manipula un modelo 3D anclado a una pieza real |

**Ejemplo en tienda:** un probador virtual que muestra cómo queda una prenda sin ponérsela (RA).

## 2.9 Robótica colaborativa (cobótica)

Los **cobots** son robots diseñados para **trabajar junto a las personas**, sin jaulas de seguridad, gracias a sensores que detectan contacto y limitan fuerza y velocidad. Se programan con facilidad (a veces moviéndoles el brazo) y se usan en tareas repetitivas, pesadas o de precisión: paletizado, atornillado, empaquetado, preparación de pedidos.

## 2.10 Gemelos digitales

Un **gemelo digital** es una **réplica virtual** de un objeto, proceso o sistema real que se actualiza con datos del original en tiempo real. Permite simular «qué pasaría si…» sin riesgo: probar una nueva distribución del almacén, predecir el desgaste de una máquina o ensayar el impacto de un cambio antes de invertir.

## 2.11 Otras THD

- **Fabricación aditiva (impresión 3D)**: fabricación capa a capa a partir de un diseño digital. Prototipos rápidos y piezas personalizadas.
- **Automatización robótica de procesos (RPA)**: «robots de software» que repiten tareas administrativas (copiar datos entre programas, descargar facturas).
- **Computación cuántica**: en fase de investigación, promete resolver problemas de optimización y criptografía inabordables hoy.
- **Ciberseguridad**: no es una tecnología más, sino una condición para que todas las demás funcionen con garantías.

## Autoevaluación (Capítulo 2)

- ¿Qué capacidad del 5G es clave para conectar miles de sensores?
- ¿En qué se diferencian la realidad virtual y la aumentada?
- ¿Por qué un bloque de una blockchain no se puede modificar sin que se note?
- Pon un ejemplo de gemelo digital fuera de la industria.

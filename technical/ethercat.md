# **EtherCAT Layer — Documentación Técnica Oficial**

**Topología · PDO/SDO · Drivers · Sincronización DC · Integración CNC‑CAT**

# **1. Propósito de la capa EtherCAT**

La capa EtherCAT es la **columna vertebral industrial** del ecosistema CNC‑CAT. Su misión es:

> “hablar con EtherCAT, controlar motores, leer sensores, ejecutar homing real, manejar límites físicos.”

Y además:

- proporcionar comunicación determinista,

- sincronizar ejes,

- exponer IO al PLC,

- alimentar el ciclo de control CNC.

# **2. Arquitectura general**

Según tu UML oficial:

Código

```
`\[RealMotionController\]`

`          ↓`

`       \[RealIO\]`

`          ↓`

` ┌────────┬──────────┬──────────┬──────────┐`

` │ Servo  │ Encoder  │ IO DIO   │ IO Analog │ ...`

` └────────┴──────────┴──────────┴──────────┘`
```

> “RealMotionController → RealIO → dispositivos EtherCAT.”

# **3. Módulos internos**

La capa EtherCAT se divide en:

Código

```
`ethercat/`

`    master/`

`    topology/`

`    diagnostics/`

`    io\_mapping/`

`    devices/`

`    sync/`
```

> “Vista general del subsistema de drivers.”

# **4. Componentes principales**

## **4.1 EtherCAT Master**

Responsable de:

- inicializar la red

- escanear esclavos

- configurar PDOs

- leer/escribir SDOs

- gestionar estados INIT → PRE‑OP → SAFE‑OP → OP

- enviar frames cíclicos

> “El motor real habla con EtherCAT.”

## **4.2 Topología EtherCAT**

Detecta automáticamente:

- número de esclavos

- orden físico

- tipo de dispositivo

- perfiles

- capacidades

- estados

> “Topología EtherCAT: detección y representación de la red.”

## **4.3 Diagnóstico**

Cada esclavo reporta:

- estado (INIT, PRE‑OP, SAFE‑OP, OP)

- errores

- warnings

- fallos de comunicación

- fallos de sincronización

- fallos de PDO/SDO

> “Diagnóstico completo de la red.”

## **4.4 IO Mapping**

El mapeo debe ser:

- claro

- estable

- accesible desde UI, PLC y CNC

Incluye:

- entradas digitales

- salidas digitales

- entradas analógicas

- salidas analógicas

- estados de servos

- sensores

- actuadores

> “El PLC puede leer cualquier variable EtherCAT.”

## **4.5 Perfiles de dispositivos**

La capa EtherCAT soporta:

- servomotores

- encoders

- IO digital

- IO analógico

- sensores

- actuadores

- variadores

- módulos de seguridad

Cada dispositivo define:

- PDOs

- SDOs

- modos de operación

- alarmas

- parámetros

## **4.6 Sincronización distribuida (DC)**

Es esencial para:

- interpolación precisa

- control multi‑eje

- homing sincronizado

- estabilidad del ciclo de control

> “El motor real debe sincronizarse con EtherCAT.”

# **5. Integración con el motor CNC‑CAT**

El motor real usa EtherCAT para:

- leer encoders

- controlar servos

- activar salidas

- leer sensores

- detectar límites

- ejecutar homing

- sincronizar ejes

> “El motor real controla motores, lee sensores, ejecuta homing real.”

# **6. Integración con el ciclo de control**

El ciclo de control:

> “read\_inputs → update\_state → planner\_step → write\_outputs → send\_events → wait”

Se alimenta de EtherCAT:

- `read\_inputs` ← encoders, sensores, IO

- `write\_outputs` → servos, actuadores

# **7. Integración con el PLC**

El PLC puede:

- leer cualquier variable EtherCAT

- escribir salidas

- activar secuencias

- controlar periféricos

> “El PLC integrado tiene acceso directo al IO EtherCAT.”

# **8. Integración con la UI LINCAT**

La UI muestra:

- topología

- estados de esclavos

- alarmas

- PDO/SDO

- variables en tiempo real

- gráficas de diagnóstico

> “La UI debe mostrar la topología en tiempo real.”

# **9. Seguridad**

La capa EtherCAT debe:

- detectar fallos en milisegundos

- proteger estados críticos

- impedir movimiento en ERROR o ESTOP

- validar límites físicos

- supervisar watchdogs

> “maneja límites físicos, controla motores, ejecuta homing real.”

# **10. Objetivo final de la capa EtherCAT**

Crear una capa:

- profesional

- robusta

- clara

- moderna

- industrial

- totalmente integrada

EtherCAT es el **sistema nervioso** del ecosistema CNC‑CAT.


# **Drivers — Documentación Técnica Oficial**

**Abstracción de hardware · IO · Servos · Sensores · EtherCAT**

# **1. Propósito de la capa Drivers**

La capa **drivers/** es la responsable de conectar CNC‑CAT con el mundo físico.

Su misión es:

> “abstraer hardware, unificar interfaces, permitir reemplazar hardware sin tocar el motor real, mantener independencia del CORE.”

Los drivers son la **capa más cercana al hardware**, pero siguen siendo software puro.

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

La carpeta drivers contiene:

Código

```
`drivers/`

`    base/`

`    ethercat/`

`    devices/`

`    io/`

`    safety/`
```

Cada módulo tiene una responsabilidad clara.

# **4. Componentes principales**

## **4.1 Base Drivers**

Define interfaces abstractas:

- `BaseServoDriver`

- `BaseEncoderDriver`

- `BaseIODriver`

- `BaseAnalogDriver`

- `BaseSafetyDriver`

> “El módulo drivers abstrae hardware y unifica interfaces.”

Estas interfaces permiten que:

- el motor real funcione con cualquier hardware,

- el simulador implemente versiones virtuales,

- la UI no dependa del hardware.

## **4.2 EtherCAT Drivers**

Implementan:

- PDOs

- SDOs

- sincronización DC

- estados INIT → OP

- watchdogs

- perfiles de dispositivos

> “El motor real habla con EtherCAT.”

Incluye drivers para:

- servomotores

- encoders

- IO digital

- IO analógico

- sensores

- actuadores

## **4.3 Drivers de servomotores**

Responsables de:

- habilitar servo

- deshabilitar servo

- setpoint de posición

- setpoint de velocidad

- modos de operación

- lectura de estado

- alarmas del servo

> “Controla motores, ejecuta homing real, maneja límites físicos.”

## **4.4 Drivers de encoders**

Responsables de:

- leer posición absoluta

- leer posición incremental

- detectar errores

- sincronizar con DC

- filtrar ruido

## **4.5 Drivers de IO digital**

Incluyen:

- entradas digitales (DI)

- salidas digitales (DO)

- sensores

- actuadores

- señales de máquina

Usos típicos:

- finales de carrera

- sensores de puerta

- relés

- válvulas

- señales de seguridad

## **4.6 Drivers de IO analógico**

Incluyen:

- entradas analógicas (AI)

- salidas analógicas (AO)

Usos típicos:

- sensores de presión

- sensores de temperatura

- control de variadores

- control de potencia

## **4.7 Drivers de seguridad**

Incluyen:

- E‑STOP

- Safety Door

- Safety Relay

- Safety IO

> “maneja límites físicos, controla motores, ejecuta homing real.”

# **5. Integración con el motor real**

El motor real usa los drivers para:

- leer encoders

- escribir setpoints

- leer sensores

- activar actuadores

- ejecutar homing

- validar límites

- detectar fallos

> “El motor real controla motores, lee sensores, ejecuta homing real.”

# **6. Integración con el ciclo de control**

El ciclo de control:

> “read\_inputs → update\_state → planner\_step → write\_outputs → send\_events → wait”

Los drivers participan en:

- `read\_inputs` (encoders, sensores, IO)

- `write\_outputs` (servos, actuadores)

# **7. Integración con EtherCAT**

Los drivers EtherCAT implementan:

- PDO mapping

- SDO configuration

- estados de esclavos

- sincronización DC

- diagnóstico

> “Drivers + EtherCAT: vista general del subsistema.”

# **8. Integración con el PLC**

El PLC accede al IO a través de los drivers:

- lectura de entradas

- escritura de salidas

- lectura de sensores

- control de actuadores

> “El PLC puede leer cualquier variable EtherCAT.”

# **9. Seguridad**

Los drivers deben:

- validar límites físicos

- detectar fallos de servo

- detectar fallos de encoder

- detectar fallos de IO

- detener el sistema en caso crítico

- activar ESTOP

> “maneja límites físicos, controla motores, ejecuta homing real.”

# **10. Objetivo final de la capa Drivers**

Crear una capa:

- robusta

- segura

- clara

- modular

- industrial

- independiente del hardware

- fácil de extender

Los drivers son la **puerta de entrada al mundo físico**.


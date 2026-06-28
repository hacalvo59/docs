# **Motor Real — Documentación Técnica Oficial**

**Control físico · EtherCAT · Homing · Límites · Seguridad · IO real**

# **1. Propósito del motor real**

El motor real es la implementación física del ecosistema CNC‑CAT.

Su misión es:

> “hablar con EtherCAT, controlar motores, leer sensores, ejecutar homing real, manejar límites físicos, controlar el husillo.”

Es el módulo que convierte:

- trayectorias → movimiento real

- estados → señales físicas

- IO → sensores y actuadores

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

# **3. Componentes principales**

## **3.1 RealMotionController**

Implementa la Motion API:

- start / pause / resume / stop

- jog

- homing real

- ejecución de G‑code

- overrides

- estados

- alarmas

- control del husillo

> “El motor real implementa la Motion API y controla el hardware.”

## **3.2 RealIO**

Responsable de:

- leer entradas digitales

- leer entradas analógicas

- leer encoders

- escribir salidas digitales

- escribir salidas analógicas

- enviar setpoints a servos

> “El motor real lee sensores y controla actuadores.”

## **3.3 Drivers EtherCAT**

Incluyen:

- servomotores

- encoders

- IO digital

- IO analógico

- sensores

- actuadores

> “El motor real habla con EtherCAT.”

## **3.4 Planner + Interpolador**

El motor real usa:

- planner del CORE

- interpolador del CORE

Para generar:

- puntos interpolados

- velocidades

- aceleraciones

- sincronización multi‑eje

> “Planner → Interpolator → TrajectoryPoint (1 kHz).”

# **4. Ciclo de control real**

El motor real ejecuta el ciclo determinista:

> “read\_inputs → update\_state → planner\_step → write\_outputs → send\_events → wait”

### **4.1 read\_inputs**

Lee:

- encoders

- sensores

- IO

- estados de servos

- límites físicos

### **4.2 update\_state**

Actualiza:

- estado de máquina

- alarmas

- homing

- límites

- sincronización

### **4.3 planner\_step**

Genera:

- siguiente punto interpolado

- velocidades

- aceleraciones

### **4.4 write\_outputs**

Envía:

- setpoints a servos

- señales a actuadores

- control de husillo

### **4.5 send\_events**

Notifica a:

- Motion API

- UI LINCAT

- PLC

# **5. Homing real**

El motor real ejecuta homing físico:

- búsqueda de sensor

- retroceso

- aproximación fina

- validación

- sincronización DC

- actualización de offsets

> “El motor real ejecuta homing real y maneja límites físicos.”

# **6. Límites físicos**

El motor real debe:

- leer finales de carrera

- validar límites software

- validar límites hardware

- detener movimiento si se exceden

- generar alarmas

> “maneja límites físicos.”

# **7. Control del husillo**

Incluye:

- encendido/apagado

- velocidad

- rampas

- frenado

- alarmas

- sensores de estado

# **8. Seguridad**

El motor real debe:

- detenerse en ESTOP

- validar watchdog EtherCAT

- validar watchdog interno

- detectar fallos de servo

- detectar fallos de encoder

- detectar fallos de IO

- proteger estados críticos

> “maneja límites físicos, controla motores, ejecuta homing real.”

# **9. Integración con EtherCAT**

El motor real depende completamente de EtherCAT para:

- control de servos

- lectura de encoders

- IO

- sincronización DC

- diagnóstico

> “Drivers + EtherCAT: vista general del subsistema.”

# **10. Integración con la Motion API**

El motor real implementa:

Código

```
`RealMotionController implements MotionAPI`
```

Esto permite:

- UI LINCAT → motor real

- PLC → motor real

- CAM → motor real

Sin dependencias directas.

# **11. Integración con la UI LINCAT**

La UI muestra:

- estados

- alarmas

- posiciones

- overrides

- IO

- topología EtherCAT

- diagnóstico

- homing

- límites

# **12. Objetivo final del motor real**

Crear un motor:

- industrial

- robusto

- seguro

- determinista

- sincronizado

- modular

- profesional

El motor real es el **corazón físico** del ecosistema CNC‑CAT.


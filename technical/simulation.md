# **Motor Simulado — Documentación Técnica Oficial**

**Primer motor funcional · Validación de arquitectura · Ejecución sin hardware**

# **1. Propósito del motor simulado**

El motor simulado es la **primera implementación funcional** del ecosistema CNC‑CAT.

Su misión es:

> “permitir probar la UI sin hardware, validar la Motion API, simular movimientos, ejecutar G‑code, depurar el planner y probar el ciclo de control.”

Es el entorno seguro donde todo se prueba antes de conectar hardware real.

# **2. Arquitectura general**

Según tu documentación:

Código

```
`simulation/`

`    sim\_motion\_controller/`

`    sim\_io/`

`    sim\_planner/`

`    sim\_interpolator/`

`    sim\_machine/`
```

> “El motor simulado implementa la Motion API y permite probar toda la arquitectura sin hardware.”

# **3. Componentes principales**

## **3.1 SimMotionController**

Implementa la Motion API:

- start / pause / resume / stop

- jog

- homing simulado

- carga de G‑code

- ejecución paso a paso

- overrides

- estados

> “El motor simulado es compatible 1:1 con la Motion API.”

Esto permite que la UI funcione **exactamente igual** que con el motor real.

## **3.2 SimIO**

Simula:

- entradas digitales

- salidas digitales

- entradas analógicas

- salidas analógicas

- sensores

- actuadores

> “El motor simulado permite probar IO sin hardware.”

## **3.3 SimPlanner**

Simula el planificador real:

- convierte G‑code en trayectorias

- respeta límites

- respeta velocidades

- respeta aceleraciones

- genera segmentos

> “Planner → Interpolator → TrajectoryPoint (1 kHz).”

## **3.4 SimInterpolator**

Genera puntos interpolados:

- posición

- velocidad

- aceleración

- timestamp

A 1 kHz (simulado).

## **3.5 SimMachine**

Simula la máquina completa:

- ejes

- límites

- offsets

- herramientas

- homing

- estados

> “El motor simulado permite validar estados, alarmas y límites.”

# **4. Integración con el ciclo de control**

El motor simulado ejecuta el ciclo:

> “read\_inputs → update\_state → planner\_step → write\_outputs → send\_events → wait”

Pero todo ocurre en memoria, sin hardware.

Esto permite:

- depurar

- probar

- validar

- simular

- reproducir errores

# **5. Integración con la Motion API**

El motor simulado implementa **exactamente** la misma interfaz que el motor real:

Código

```
`SimMotionController implements MotionAPI`
```

Esto garantiza:

- la UI no sabe si es sim o real

- el PLC funciona igual

- EtherCAT no es necesario

- el comportamiento es determinista

> “Permite intercambiar motores sin tocar la UI.”

# **6. Integración con la UI LINCAT**

La UI puede probar:

- jog

- homing

- ejecución de G‑code

- offsets

- herramientas

- alarmas

- estados

- overrides

- simulación 3D

> “El motor simulado permite probar la UI sin hardware.”

# **7. Integración con el PLC**

El PLC puede:

- leer IO simulado

- escribir IO simulado

- activar secuencias

- probar lógica

- depurar

Esto permite probar automatización **sin riesgo**.

# **8. Alarmas y estados simulados**

El motor simulado reproduce:

- límites

- errores de interpolación

- errores de G‑code

- estados inválidos

- ESTOP simulado

> “El motor simulado permite validar estados y alarmas.”

# **9. Objetivo final del motor simulado**

Crear un motor:

- seguro

- determinista

- completo

- compatible

- rápido

- ideal para desarrollo

- ideal para testing

- ideal para depuración

El motor simulado es el **laboratorio oficial** del ecosistema CNC‑CAT.


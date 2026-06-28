# 📘 **OPERATIONS\_GUIDE.md**

**Guía oficial de operación del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Esta guía explica **cómo operar el sistema** en condiciones reales:

- cómo iniciar el sistema

- cómo detenerlo

- cómo ejecutar programas

- cómo usar la UI LINCAT

- cómo interpretar estados y alarmas

- cómo trabajar con motores (sim/real)

- cómo operar de forma segura

Es la guía que usaría un **operador industrial**.

# ⭐ 2. Inicio del sistema

## **2.1 Inicio en simulación**

bash

```
`python3 main\_simulation.py`
```

## **2.2 Inicio en hardware real**

bash

```
`sudo python3 main\_real.py`
```

## **2.3 Inicio de la UI LINCAT**

bash

```
`python3 lincat.py`
```

# ⭐ 3. Flujo de operación estándar

El flujo de operación recomendado es:

Código

```
`1. Encender máquina`

`2. Iniciar motor (sim/real)`

`3. Abrir UI LINCAT`

`4. Realizar homing`

`5. Cargar programa`

`6. Ejecutar`

`7. Supervisar`

`8. Detener`

`9. Apagar`
```

# ⭐ 4. Homing

## **4.1 Homing simulado**

- No requiere sensores

- No requiere límites físicos

- Se usa para pruebas

## **4.2 Homing real**

- Requiere sensores

- Requiere límites mecánicos

- Requiere E‑STOP operativo

- Requiere supervisión humana

## **4.3 Estados del homing**

- `HOMING\_START`

- `HOMING\_SEARCH`

- `HOMING\_LATCH`

- `HOMING\_OFFSET`

- `HOMING\_DONE`

# ⭐ 5. Jog (movimiento manual)

## **5.1 Modos**

- continuo

- incremental

- por velocidad

- por distancia

## **5.2 Reglas**

- Jog solo permitido en estado `READY`

- Jog bloqueado en `RUNNING`

- Jog bloqueado en `ERROR`

- Jog bloqueado en `ESTOP`

# ⭐ 6. Carga de programas

## **6.1 Formatos soportados**

- `.nc`

- `.gcode`

- `.tap`

## **6.2 Validaciones**

- sintaxis

- límites

- offsets

- herramientas

- movimientos rápidos

# ⭐ 7. Ejecución de programas

## **7.1 Estados**

- `RUNNING`

- `PAUSED`

- `STOPPING`

- `STOPPED`

## **7.2 Controles**

- iniciar

- pausar

- reanudar

- detener

- detener seguro

- E‑STOP

# ⭐ 8. Estados del sistema

Los estados principales del ecosistema:

Código

```
`INIT → IDLE → READY → RUNNING → STOPPING → ERROR → ESTOP`
```

## **8.1 INIT**

Sistema arrancando.

## **8.2 IDLE**

Sistema encendido pero sin homing.

## **8.3 READY**

Sistema homing completado.

## **8.4 RUNNING**

Programa en ejecución.

## **8.5 PAUSED**

Ejecución detenida temporalmente.

## **8.6 STOPPING**

Detención controlada.

## **8.7 ERROR**

Fallo recuperable.

## **8.8 ESTOP**

Fallo crítico. Requiere intervención humana.

# ⭐ 9. Alarmas

## **9.1 Tipos**

- límites

- servo

- EtherCAT

- IO

- planner

- interpolador

- PLC

- UI

## **9.2 Reglas**

- alarmas menores → STOPPING

- alarmas mayores → ERROR

- alarmas críticas → ESTOP

# ⭐ 10. Operación segura

## **10.1 Reglas**

- E‑STOP siempre accesible

- operador presente

- no operar sin límites

- no operar sin homing

- no operar con alarmas activas

## **10.2 Supervisión**

- posición

- velocidad

- carga

- temperatura

- estado EtherCAT

- estado servo

# ⭐ 11. Apagado del sistema

## **11.1 Apagado normal**

1. Detener programa

2. Volver a `IDLE`

3. Cerrar UI

4. Apagar motor

5. Apagar máquina

## **11.2 Apagado de emergencia**

- pulsar E‑STOP

- cortar alimentación

- revisar máquina

# ⭐ 12. Objetivo final

Garantizar que el ecosistema LINCAT / CNC‑CAT pueda operarse:

- de forma segura

- de forma profesional

- de forma industrial

- de forma predecible

- de forma confiable


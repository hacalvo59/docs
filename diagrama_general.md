markdown

```
`\# ⭐ Diagrama general del ecosistema LINCAT / CNC‑CAT`


`\#\# 1. Vista global de capas`


`\`\`\`text`

`\[ Usuario \]`

`     ↓`

`\[ UI LINCAT \]`

`     ↓`

`\[ Motion API \]`

`     ↓`

`\[ CNC‑CAT Core \]`

`     ↓`

`\[ Motores \]`

`   ├─ \[ Motor simulado \]`

`   └─ \[ Motor real \]`

`         ↓`

`     \[ EtherCAT Layer \]`

`         ↓`

`     \[ Drivers \]`

`         ↓`

`     \[ Hardware físico \]`
```

## 2. Detalle por subsistemas

text

```
`\[ UI LINCAT \]`

`   ├─ Panel CNC (ejecución, offsets, herramientas, MDI, alarmas)`

`   ├─ Panel PLC (editor ST, debugger, IO)`

`   ├─ Panel EtherCAT (topología, diagnóstico)`

`   └─ Panel Sistema (logs, configuración, remoto)`


`\[ Motion API \]`

`   ├─ Comandos (start, stop, pause, resume, jog, homing)`

`   ├─ Estados (INIT, IDLE, READY, RUNNING, PAUSED, STOPPING, ERROR, ESTOP)`

`   ├─ Programas (cargar, validar, ejecutar)`

`   └─ Eventos (alarmas, cambios de estado, progreso)`
```

text

```
`\[ CNC‑CAT Core \]`

`   ├─ models/      (Axis, MachineState, Tool, Offset, Program, TrajectoryPoint)`

`   ├─ gcode/       (parser, comandos, programa)`

`   ├─ planner/     (trayectorias)`

`   ├─ states/      (estados, alarmas)`

`   └─ utils/       (math, validación, conversión)`
```

text

```
`\[ Motores \]`

`   ├─ Motor simulado`

`   │    ├─ SimMotionController (implementa Motion API)`

`   │    ├─ SimPlanner / SimInterpolator`

`   │    └─ SimIO (IO virtual)`

`   └─ Motor real`

`        ├─ RealMotionController (implementa Motion API)`

`        ├─ RealIO (lectura/escritura física)`

`        └─ Planner + Interpolador (puntos a 1 kHz)`
```

text

```
`\[ EtherCAT Layer \]`

`   ├─ Master (estados INIT, PRE-OP, SAFE-OP, OP)`

`   ├─ Topología (esclavos, orden, perfiles)`

`   ├─ PDO / SDO`

`   ├─ Sync DC`

`   └─ Diagnóstico`
```

text

```
`\[ Drivers \]`

`   ├─ Servos`

`   ├─ Encoders`

`   ├─ IO digital`

`   ├─ IO analógico`

`   └─ Seguridad (E-STOP, puertas, relés)`
```

text

```
`\[ Hardware físico \]`

`   ├─ Máquina CNC (ejes, husillo)`

`   ├─ Sensores`

`   ├─ Actuadores`

`   └─ Periféricos`
```

## 3. Ciclo de control integrado

text

```
`read\_inputs`

`    ↓`

`update\_state`

`    ↓`

`planner\_step`

`    ↓`

`write\_outputs`

`    ↓`

`send\_events`

`    ↓`

`wait`
```

- `read\_inputs` ← EtherCAT + Drivers (encoders, sensores, IO)

- `update\_state` ← Core (estados, alarmas)

- `planner\_step` ← Core (planner/interpolador)

- `write\_outputs` ← EtherCAT + Drivers (servos, actuadores)

- `send\_events` ← Motion API → UI LINCAT / PLC

- `wait` ← sincronización determinista

## 4. Relación PLC integrado

text

```
`\[ PLC integrado \]`

`   ├─ Editor ST`

`   ├─ Compilador`

`   ├─ Runtime determinista`

`   ├─ Debugger`

`   └─ IO Mapping (EtherCAT / Drivers / CNC)`
```

El PLC se ejecuta en paralelo al ciclo de control y ve:

- IO EtherCAT

- estados CNC‑CAT

- variables de sistema

## 5. Objetivo del diagrama

Este diagrama resume:

- quién habla con quién,

- qué capa hace qué,

- cómo fluye la información,

- dónde se separan lógica, UI y hardware.

Es la **foto global** del ecosistema LINCAT / CNC‑CAT.

Código


`---`


`Cuando quieras, pasamos \*\*a la siguiente en la lista descendente\*\*:  `

`README para GitHub, roadmap técnico, portada visual, índice maestro final.`
```


# **CORE — Documentación Técnica Oficial**

**Modelos · G‑code · Estados · Estructuras internas · Filosofía**

# **1. Propósito del CORE**

El CORE es la base lógica del motor CNC‑CAT. Es el módulo más estable, más importante y más duradero del proyecto.

> “El CORE es la base lógica del motor CNC… no toca hardware, no toca simulación, no depende de drivers, no depende de la UI.”

Su misión:

- definir la lógica CNC universal,

- ser independiente del hardware,

- ser independiente de la UI,

- ser estable durante décadas,

- servir tanto al motor simulado como al motor real.

# **2. Estructura del CORE**

Según tus documentos, el CORE contiene cinco grandes áreas:

Código

```
`core/`

`    models/`

`    gcode/`

`    planner/`

`    states/`

`    utils/`
```

> “El CORE contiene: models, gcode, motion\_api, states, utils.”

# **3. Módulos del CORE**

## **3.1 models/**

Modelos puros, sin lógica de hardware.

Incluye:

- **Axis**

- **MachineState**

- **Tool**

- **Offset**

- **Program**

- **TrajectoryPoint**

> “Representaciones internas: Axis, MachineState, Tool, Offset, Program, TrajectoryPoint.”

### UML (según tus documentos)

> “class Axis \{ name, position\_machine, position\_work, min\_limit, max\_limit \}”

> “class Tool \{ id, length, radius, comment \}”

> “class Offset \{ system, x, y, z \}”

## **3.2 gcode/**

Parser y estructuras internas del lenguaje CNC.

Incluye:

- **GcodeParser**

- **GcodeCommand**

- **GcodeProgram**

> “Incluye: GcodeParser, GcodeCommand, GcodeProgram. El parser convierte texto en estructuras internas.”

### UML del parser

> “GcodeParser, Tokenizer, Token, ModalGroupManager, GcodeErrorHandler.”

## **3.3 planner/**

Planificador abstracto de trayectorias.

Responsable de:

- convertir comandos en trayectorias,

- generar puntos interpolados,

- respetar límites,

- preparar datos para el ciclo de control.

> “Planner → Interpolator → TrajectoryPoint (1 kHz).”

El CORE no implementa el planner real ni el simulado: solo define la **interfaz y estructuras base**.

## **3.4 states/**

Define:

- estados de máquina,

- transiciones válidas,

- alarmas,

- condiciones de seguridad.

> “Define: estados de máquina, transiciones válidas, errores, alarmas, condiciones de seguridad.”

Estados oficiales:

> “READY, RUNNING, PAUSED, HOMING, ERROR, ESTOP.”

## **3.5 utils/**

Funciones comunes:

- matemáticas,

- validación,

- conversión de unidades,

- logs internos.

> “Funciones comunes: matemáticas, interpolación básica, validación, conversión de unidades, logs internos.”

# **4. Qué NO pertenece al CORE**

Esto es crítico:

> “❌ No drivers ❌ No hardware ❌ No tiempo real ❌ No simulación ❌ No UI ❌ No dependencias externas complejas ❌ No lógica específica de una máquina.”

El CORE debe ser:

- puro,

- limpio,

- estable,

- universal.

# **5. Relación del CORE con el resto del sistema**

Diagrama oficial:

> “UI → Motion API → Motor sim/real → CORE → Drivers → Hardware.”

El CORE es el puente entre:

- la lógica universal,

- y las implementaciones concretas (sim/real).

# **6. Filosofía del CORE**

> “Estabilidad, claridad, universalidad, documentación, extensibilidad.”

El CORE debe:

- durar décadas,

- ser fácil de mantener,

- ser fácil de extender,

- no romper compatibilidad,

- ser independiente del hardware.

# **7. Integración con Motion API**

Aunque la Motion API no está dentro del CORE, el CORE define las estructuras que la API utiliza:

- estados,

- DRO,

- offsets,

- herramientas,

- programas,

- alarmas.

> “La UI solo habla con la Motion API. El CORE es la lógica universal.”

# **8. Integración con el ciclo de control**

El CORE provee:

- modelos,

- planner base,

- estados,

- alarmas.

El ciclo usa estos elementos para ejecutar:

> “read\_inputs → update\_state → planner\_step → write\_outputs → send\_events → wait.”

# **9. Objetivo final del CORE**

Crear una base:

- sólida,

- universal,

- independiente,

- documentada,

- modular,

- profesional.

El CORE es el corazón lógico del ecosistema CNC‑CAT.


# **PLC Integrado — Documentación Técnica Oficial**

**Editor ST · Compilador · Runtime determinista · Debugger · IO Mapping**

# **1. Propósito del PLC integrado**

El PLC integrado es un componente nativo del ecosistema CNC‑CAT. Su misión es:

> “proporcionar lógica de máquina, automatización secuencial, control de periféricos, supervisión de estados e interacción directa con EtherCAT.”

El PLC no es externo: **forma parte del ecosistema**, sincronizado con CNC‑CAT y EtherCAT.

# **2. Arquitectura general del PLC**

Según tu documentación:

Código

```
`plc/`

`    editor/`

`    compiler/`

`    runtime/`

`    debugger/`

`    io\_mapping/`

`    system/`
```

> “El PLC se divide en editor ST, compilador, runtime, debugger, IO mapping y sistema.”

# **3. Componentes principales**

## **3.1 Editor ST (Structured Text)**

El editor ST es la interfaz donde el usuario escribe lógica PLC.

Incluye:

- resaltado de sintaxis

- autocompletado

- plegado de código

- navegación por funciones

- plantillas IEC

- verificación de sintaxis

- integración con debugger

> “El editor debe incluir resaltado, autocompletado, plegado, navegación y verificación.”

## **3.2 Compilador ST → Bytecode**

El compilador convierte el código ST en bytecode optimizado.

Debe soportar:

- variables globales y locales

- funciones

- Function Blocks (FB)

- estructuras

- arrays

- temporizadores

- operadores lógicos y aritméticos

- acceso a IO EtherCAT

- acceso a estados del CNC

> “El compilador convierte ST en bytecode optimizado.”

## **3.3 Runtime determinista**

El runtime ejecuta el bytecode en ciclos deterministas.

Responsabilidades:

- ejecutar tareas cíclicas

- respetar tiempos de ciclo

- sincronizar con EtherCAT

- sincronizar con CNC‑CAT

- manejar errores

- watchdog interno

> “El runtime ejecuta el bytecode en ciclos deterministas con sincronización EtherCAT.”

## **3.4 Debugger en tiempo real**

El debugger permite:

- inspección de variables

- modificación en vivo

- breakpoints

- watchlists

- seguimiento de ejecución

- gráficas de señales

- logging avanzado

> “El debugger debe permitir inspección, modificación, breakpoints, watchlists y gráficas.”

## **3.5 IO Mapping**

El PLC tiene acceso directo a:

- entradas digitales

- salidas digitales

- entradas analógicas

- salidas analógicas

- estados de servos

- sensores

- actuadores

- variables del CNC

> “El PLC puede leer cualquier variable EtherCAT y controlar periféricos.”

El mapeo debe ser:

- claro

- estable

- documentado

- accesible desde UI, CNC y PLC

## **3.6 Sistema de tareas**

El PLC soporta:

- tareas cíclicas

- tareas periódicas

- tareas event‑driven

- prioridades

- tiempos de ciclo configurables

> “El runtime ejecuta tareas deterministas con tiempos configurables.”

# **4. Integración con EtherCAT**

El PLC accede directamente al IO EtherCAT:

- lectura de sensores

- escritura de actuadores

- lectura de estados de servos

- lectura de módulos IO

- escritura de salidas digitales/analógicas

> “El PLC integrado tiene acceso directo al IO EtherCAT.”

# **5. Integración con CNC‑CAT**

El PLC puede:

- leer estados del CNC

- activar secuencias

- controlar periféricos

- gestionar ciclos automáticos

- interactuar con alarmas

- coordinar movimientos

El CNC expone:

- estados

- eventos

- señales

- variables

- overrides

> “El PLC puede coordinar movimientos y gestionar ciclos automáticos.”

# **6. Integración con la UI LINCAT**

La UI ofrece:

- editor ST

- panel de variables

- panel de IO

- debugger visual

- gráficas

- consola de compilación

- carga/descarga de programas

- gestión de tareas

> “La UI debe incluir editor ST, debugger, IO mapping y gráficas.”

# **7. Seguridad**

El PLC incluye:

- watchdog interno

- límites de ejecución

- protección contra loops infinitos

- aislamiento de memoria

- validación de tipos

- manejo seguro de errores

> “El PLC debe incluir watchdog, límites de ejecución y protección contra loops.”

# **8. Relación con el ciclo de control**

El PLC se ejecuta **en paralelo** al ciclo CNC:

> “read\_inputs → update\_state → planner\_step → write\_outputs → send\_events → wait”

El PLC puede:

- leer entradas

- escribir salidas

- reaccionar a estados

- activar secuencias

# **9. Objetivo final del PLC integrado**

Crear un PLC:

- profesional

- moderno

- robusto

- determinista

- integrado con EtherCAT

- integrado con CNC‑CAT

- accesible desde LINCAT

- digno de un estándar mundial

El PLC es el **cerebro lógico** del ecosistema.


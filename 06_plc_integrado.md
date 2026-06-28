# **06 — PLC Integrado (Editor ST, Runtime y Debugger)**

## **6.1 Propósito del PLC integrado**

El PLC integrado es un componente fundamental del ecosistema CNC‑CAT. Su misión es proporcionar:

- **lógica de máquina**,

- **automatización secuencial**,

- **control de periféricos**,

- **supervisión de estados**,

- **interacción directa con EtherCAT**,

- **comunicación con el motor CNC‑CAT**,

- **diagnóstico en tiempo real**.

El PLC no es un módulo externo: **es parte nativa del ecosistema**, diseñado para trabajar en sincronía con CNC‑CAT y EtherCAT.

## **6.2 Objetivos principales del PLC**

- Proveer un entorno de programación profesional basado en **Structured Text (ST)**.

- Permitir lógica compleja de máquina.

- Integrarse con el mapeo de IO EtherCAT.

- Ejecutar en tiempo real junto al motor CNC.

- Ofrecer herramientas de depuración avanzadas.

- Ser accesible desde la UI LINCAT.

- Ser seguro, determinista y confiable.

## **6.3 Arquitectura interna del PLC**

El PLC se divide en módulos:

Código

```
`plc/`

`    editor/       → editor ST con resaltado y herramientas`

`    compiler/     → compilador ST → bytecode`

`    runtime/      → ejecución determinista`

`    debugger/     → inspección en vivo`

`    io\_mapping/   → integración con EtherCAT`

`    system/       → tareas, ciclos, estados`
```

## **6.4 Componentes principales**

### **6.4.1 Editor ST (Structured Text)**

El editor debe incluir:

- resaltado de sintaxis,

- autocompletado,

- plegado de código,

- navegación por funciones,

- plantillas de bloques,

- verificación de sintaxis,

- integración con el debugger.

El lenguaje ST debe seguir IEC 61131‑3.

### **6.4.2 Compilador ST → Bytecode**

El compilador convierte el código ST en bytecode optimizado.

Debe soportar:

- variables globales y locales,

- funciones,

- FBs (Function Blocks),

- estructuras,

- arrays,

- temporizadores,

- operadores lógicos y aritméticos,

- acceso a IO EtherCAT,

- acceso a estados del CNC.

### **6.4.3 Runtime (Ejecución determinista)**

El runtime ejecuta el bytecode en ciclos deterministas.

Debe garantizar:

- ejecución estable,

- tiempos de ciclo configurables,

- acceso seguro a IO,

- sincronización con EtherCAT,

- sincronización con el motor CNC,

- manejo de errores,

- watchdog interno.

### **6.4.4 Debugger en tiempo real**

El debugger debe permitir:

- inspección de variables,

- modificación en vivo,

- breakpoints,

- watchlists,

- seguimiento de ejecución,

- gráficas de señales,

- logging avanzado.

Todo visible desde la UI LINCAT.

### **6.4.5 Mapeo de IO (IO Mapping)**

El PLC debe tener acceso directo a:

- entradas digitales,

- salidas digitales,

- entradas analógicas,

- salidas analógicas,

- estados de servos,

- sensores,

- actuadores,

- variables del CNC.

El mapeo debe ser:

- claro,

- estable,

- documentado,

- accesible desde la UI.

### **6.4.6 Integración con CNC‑CAT**

El PLC puede:

- leer estados del CNC,

- activar secuencias,

- controlar periféricos,

- gestionar ciclos automáticos,

- interactuar con alarmas,

- coordinar movimientos.

El motor CNC expone:

- estados,

- eventos,

- señales,

- variables,

- overrides.

## **6.5 Integración con la UI LINCAT**

La UI debe ofrecer:

- editor ST completo,

- panel de variables,

- panel de IO,

- debugger visual,

- gráficas de señales,

- consola de compilación,

- carga y descarga de programas,

- gestión de tareas PLC.

## **6.6 Seguridad y confiabilidad**

El PLC debe incluir:

- watchdog interno,

- límites de ejecución,

- protección contra loops infinitos,

- aislamiento de memoria,

- validación de tipos,

- manejo seguro de errores.

## **6.7 Objetivo final del PLC integrado**

Crear un PLC:

- profesional,

- moderno,

- robusto,

- determinista,

- integrado con EtherCAT,

- integrado con CNC‑CAT,

- accesible desde LINCAT,

- digno de un estándar mundial.

El PLC es el cerebro lógico del ecosistema. CNC‑CAT es el movimiento. EtherCAT es el sistema nervioso. LINCAT es la cara humana.


# **UI LINCAT — Documentación Técnica Oficial**

**Arquitectura · Eventos · Señales · Paneles · Controladores · Integración**

# **1. Propósito de la UI LINCAT**

La UI LINCAT es la **interfaz humana** del ecosistema CNC‑CAT. Su misión es:

> “ser clara, profesional, rápida, modular, internacional y apta para operación remota.”

La UI **no contiene lógica CNC**, ni lógica de hardware. Toda la lógica se delega a:

- Motion API

- CNC‑CAT

- EtherCAT Layer

- PLC

La UI es un **cliente visual**.

# **2. Arquitectura general de la UI**

Según tus documentos UML:

Código

```
`\[LincatApp\]`

`      ↓`

`\[LincatController\]`

`      ↓`

`\[LincatEvents\]`

`      ↓`

`\[Paneles / Widgets\]`
```

> “La UI LINCAT se organiza en cuatro capas: App → Controller → Events → Paneles.”

# **3. Capas internas**

## **3.1 LincatApp**

Es la aplicación principal.

Responsabilidades:

- inicializar la UI

- cargar configuración

- crear controladores

- gestionar temas visuales

- gestionar idiomas

- gestionar ventanas principales

> “LincatApp es el punto de entrada de la UI.”

## **3.2 LincatController**

Es el **cerebro de la UI**, pero sin lógica CNC.

Responsabilidades:

- comunicarse con Motion API

- recibir estados

- recibir alarmas

- enviar comandos

- distribuir eventos a los paneles

- gestionar modos de operación

> “LincatController es el puente entre la UI y la Motion API.”

## **3.3 LincatEvents**

Sistema interno de eventos.

Responsabilidades:

- notificar cambios de estado

- notificar alarmas

- notificar actualizaciones de posición

- notificar overrides

- notificar cambios de panel

- notificar cambios de idioma

> “LincatEvents distribuye eventos a todos los paneles.”

## **3.4 Paneles / Widgets**

Cada panel es independiente.

Paneles principales:

- CNC — Programa

- CNC — Ejecución

- CNC — Overrides

- CNC — Estado de máquina

- CNC — Movimiento (Jog + DRO + Home)

- CNC — Offsets

- CNC — Herramientas

- CNC — MDI

- CNC — Alarmas

- PLC — Editor ST

- PLC — Debugger

- EtherCAT — Topología

- EtherCAT — Diagnóstico

- Sistema — Logs

- Configuración de máquina

- Operación remota

> “Cada módulo es independiente, pero todos comparten la misma base visual.”

# **4. Comunicación con Motion API**

La UI **solo** se comunica con el motor a través de la Motion API.

La UI envía:

- comandos de movimiento

- jog

- homing

- start / pause / resume / stop

- reset

- overrides

- carga de G‑code

- selección de herramienta

- cambios de offset

La UI recibe:

- estados

- alarmas

- posiciones

- overrides

- eventos

- progreso

- topología EtherCAT

- variables PLC

- IO mapeado

> “La UI nunca toca el motor directamente.”

# **5. Eventos internos de la UI**

### **5.1 Eventos de estado**

- `on\_state\_changed(state)`

- `on\_execution\_started()`

- `on\_execution\_finished()`

- `on\_execution\_paused()`

- `on\_execution\_resumed()`

### **5.2 Eventos de posición**

- `on\_position\_update(machine\_pos, work\_pos)`

### **5.3 Eventos de alarmas**

- `on\_alarm\_raised(alarm)`

- `on\_alarm\_cleared(alarm)`

### **5.4 Eventos de overrides**

- `on\_feed\_override\_changed(value)`

- `on\_spindle\_override\_changed(value)`

### **5.5 Eventos de panel**

- `on\_panel\_changed(panel\_id)`

> “LincatEvents distribuye eventos a todos los paneles.”

# **6. Paneles principales (detalle técnico)**

## **6.1 Panel CNC — Ejecución**

Muestra:

- estado

- progreso

- línea actual

- tiempo estimado

- overrides

- botones de control

## **6.2 Panel CNC — Movimiento**

Incluye:

- jog

- home

- DRO

- límites

- velocidades

## **6.3 Panel CNC — Offsets**

Muestra:

- G54–G59

- offsets dinámicos

- offsets de herramienta

## **6.4 Panel CNC — Herramientas**

Incluye:

- tabla de herramientas

- longitudes

- radios

- comentarios

## **6.5 Panel CNC — Alarmas**

Muestra:

- alarmas activas

- historial

- severidad

- acciones recomendadas

## **6.6 Panel PLC**

Incluye:

- editor ST

- compilador

- debugger

- variables

- IO mapping

## **6.7 Panel EtherCAT**

Incluye:

- topología

- estados

- PDO/SDO

- diagnóstico

# **7. Estándares visuales aplicados**

La UI LINCAT usa:

- colores IEC 60204‑1

- iconografía ISO 7000

- tipografía industrial

- layout modular

- diseño táctil

- diseño multilingüe

> “La UI debe ser clara, profesional, rápida, modular, internacional.”

# **8. Integración con el ciclo de control**

La UI no ejecuta el ciclo, pero lo visualiza:

> “read\_inputs → update\_state → planner\_step → write\_outputs → send\_events → wait”

La UI muestra:

- posiciones

- estados

- alarmas

- overrides

- tiempos

- interpolación

# **9. Objetivo final de la UI LINCAT**

Crear una UI:

- profesional

- moderna

- clara

- robusta

- internacional

- accesible

- segura

- digna de un estándar mundial

La UI es la **cara humana** del ecosistema CNC‑CAT.


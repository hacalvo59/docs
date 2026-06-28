# **Motion API — Documentación Técnica Oficial**

**Interfaz universal entre UI LINCAT y CNC‑CAT**

# **1. Propósito de la Motion API**

La Motion API es la **interfaz universal** que conecta:

- la UI LINCAT

- con el motor CNC‑CAT (simulado o real)

Su objetivo es:

> “unificar comunicación, evitar dependencias, permitir intercambiar motores sin tocar la UI, garantizar estabilidad y claridad.”

Es el **contrato estable** del ecosistema.

# **2. Filosofía de diseño**

La Motion API debe ser:

- estable a largo plazo

- independiente de la UI

- independiente del motor real/simulado

- clara y documentada

- segura

- extensible

- determinista

> “La UI solo habla con la Motion API. Nunca directamente con el motor.”

# **3. Arquitectura general**

Según tus documentos:

Código

```
`UI LINCAT`

`    ↓`

`Motion API`

`    ↓`

`Motor CNC (sim/real)`
```

> “La Motion API es la frontera entre la UI y el motor CNC.”

# **4. Responsabilidades de la Motion API**

### **4.1 Comandos de movimiento**

- Jog

- Homing

- Start

- Pause

- Resume

- Stop

- Reset

- Overrides

- Movimientos manuales

- Movimientos programados

> “La API expone comandos de movimiento, ejecución y control.”

### **4.2 Gestión de programas**

- cargar G‑code

- validar

- iniciar ejecución

- detener

- obtener progreso

> “La API permite cargar y ejecutar programas G‑code sin tocar el motor.”

### **4.3 Estados y señales**

- estado de máquina

- estado de ejecución

- posiciones

- velocidades

- overrides

- alarmas

- eventos

> “La API expone estados, alarmas, posiciones y eventos del motor.”

### **4.4 Interacción con el ciclo de control**

La Motion API recibe datos del ciclo:

> “read\_inputs → update\_state → planner\_step → write\_outputs → send\_events → wait”

Y los expone a la UI de forma segura.

# **5. Estructura interna de la Motion API**

Según tus documentos UML:

Código

```
`class MotionAPI \{`

`    + connect()`

`    + disconnect()`

`    + get\_state()`

`    + get\_position()`

`    + get\_overrides()`

`    + send\_command()`

`    + load\_program()`

`    + start()`

`    + pause()`

`    + resume()`

`    + stop()`

`    + reset()`

`\}`
```

> “La API define métodos claros para control, estado, ejecución y eventos.”

# **6. Tipos de datos expuestos**

### **6.1 Estado de máquina**

- INIT

- IDLE

- READY

- RUNNING

- PAUSED

- STOPPING

- ERROR

- ESTOP

> “Estados oficiales del sistema CNC‑CAT.”

### **6.2 DRO (Digital Read Out)**

- posición máquina

- posición trabajo

- velocidad actual

- velocidad objetivo

- estado de interpolación

### **6.3 Overrides**

- feed override

- spindle override

- rapid override

### **6.4 Alarmas**

Cada alarma incluye:

- código

- severidad

- descripción

- acción recomendada

> “Cada alarma tiene código, severidad, descripción traducible y acción recomendada.”

### **6.5 Eventos**

- inicio de ejecución

- fin de ejecución

- cambio de estado

- alarma nueva

- alarma resuelta

- actualización de posición

- actualización de overrides

# **7. Seguridad y validación**

La Motion API debe:

- validar parámetros

- evitar comandos ilegales

- evitar transiciones inválidas

- proteger estados críticos

- impedir ejecución en ERROR o ESTOP

> “La API debe garantizar seguridad y estabilidad.”

# **8. Integración con motores sim/real**

La Motion API **no sabe** si el motor es:

- simulado

- real

Ambos implementan la misma interfaz:

Código

```
`SimMotionController implements MotionAPI`

`RealMotionController implements MotionAPI`
```

> “Permite intercambiar motores sin tocar la UI.”

# **9. Integración con la UI LINCAT**

La UI obtiene todo desde la Motion API:

- estados

- alarmas

- posiciones

- overrides

- eventos

- progreso

- herramientas

- offsets

Y envía:

- comandos

- ejecución

- homing

- jog

- overrides

- carga de programas

> “La UI nunca toca el motor directamente.”

# **10. Objetivo final de la Motion API**

Crear una interfaz:

- clara

- estable

- universal

- segura

- documentada

- independiente

- profesional

La Motion API es el **contrato oficial** del ecosistema CNC‑CAT.


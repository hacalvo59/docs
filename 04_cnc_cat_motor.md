# **04 — CNC‑CAT: Motor CNC Industrial**

## **4.1 Propósito del motor CNC‑CAT**

CNC‑CAT es el **motor CNC industrial** del ecosistema. Su misión es ejecutar movimientos precisos, seguros y deterministas en máquinas CNC modernas, integrándose de forma nativa con EtherCAT, PLC y la UI LINCAT.

CNC‑CAT no depende de LinuxCNC ni de ningún motor externo. Es un motor **nuevo**, diseñado desde cero para:

- rendimiento industrial,

- modularidad,

- claridad arquitectónica,

- escalabilidad,

- operación en tiempo real,

- integración total con EtherCAT.

## **4.2 Estructura general del motor**

El motor se divide en tres módulos principales:

Código

```
`core/`

`    common/   → lógica pura, independiente de hardware`

`    sim/      → implementación simulada`

`    real/     → implementación física`
```

### **common/**

Contiene:

- modelos,

- parser de G‑code,

- planner,

- interpolador,

- estados,

- alarmas,

- ciclo de control abstracto,

- utilidades.

### **sim/**

Contiene:

- motor simulado,

- cinemática virtual,

- simulación de sensores,

- simulación de IO,

- simulación de movimiento,

- ejecución de G‑code sin hardware.

### **real/**

Contiene:

- integración con EtherCAT,

- drivers reales,

- lectura de sensores,

- control de motores,

- homing físico,

- límites reales,

- control de husillo,

- seguridad industrial.

## **4.3 Componentes principales del motor**

### **4.3.1 Parser de G‑code**

Responsable de:

- tokenizar,

- interpretar,

- validar,

- convertir texto → comandos estructurados.

Compatible con:

- G‑codes estándar ISO,

- extensiones modernas,

- macros,

- parámetros.

### **4.3.2 Planner (Planificador de trayectorias)**

Convierte:

Código

```
`G‑code → trayectorias → segmentos → puntos interpolados`
```

Debe soportar:

- movimientos lineales,

- movimientos circulares,

- movimientos helicoidales,

- blending,

- look‑ahead,

- control de velocidad,

- aceleración y jerk.

### **4.3.3 Interpolador**

Genera puntos a **1 kHz** (o más) para el ciclo de control.

Debe garantizar:

- suavidad,

- precisión,

- sincronización con EtherCAT,

- cumplimiento de límites físicos.

### **4.3.4 Ciclo de control (Control Loop)**

El corazón del motor.

Estructura:

Código

```
`read\_inputs`

`update\_state`

`planner\_step`

`write\_outputs`

`send\_events`

`wait`
```

Debe ser:

- determinista,

- seguro,

- estable,

- sincronizado con EtherCAT.

### **4.3.5 Sistema de estados**

Estados principales:

- INIT

- IDLE

- READY

- RUNNING

- PAUSED

- STOPPING

- ERROR

- ESTOP

Cada estado tiene:

- reglas de transición,

- alarmas asociadas,

- eventos.

### **4.3.6 Sistema de alarmas**

Cada alarma tiene:

- código,

- severidad,

- descripción traducible,

- acción recomendada,

- estado del sistema asociado.

## **4.4 Integración con EtherCAT**

El motor real utiliza EtherCAT para:

- leer entradas,

- escribir salidas,

- controlar servos,

- leer encoders,

- sincronizar ejes,

- detectar fallos,

- gestionar topología.

La integración es nativa, no adaptada.

## **4.5 Integración con PLC**

El motor CNC‑CAT expone:

- estados,

- señales,

- eventos,

- variables,

- IO mapeado.

El PLC puede:

- leer estados,

- activar secuencias,

- controlar periféricos,

- interactuar con el ciclo de control.

## **4.6 Integración con LINCAT (UI)**

La UI recibe:

- estados,

- alarmas,

- posiciones,

- overrides,

- eventos,

- progreso de ejecución.

Y envía:

- comandos de movimiento,

- overrides,

- ejecución de G‑code,

- homing,

- jog,

- reset,

- stop.

Todo mediante la **Motion API**.

## **4.7 Objetivo final del motor CNC‑CAT**

Crear un motor CNC:

- moderno,

- modular,

- profesional,

- libre,

- industrial,

- seguro,

- escalable,

- preparado para EtherCAT,

- digno de ser el estándar mundial en Linux.


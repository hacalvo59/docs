# 📘 **GLOSSARY.md**

**Glosario oficial de términos del ecosistema LINCAT / CNC‑CAT**

# ⭐ **1. Propósito**

Este glosario define todos los términos técnicos utilizados en:

- CNC‑CAT Core

- Motion API

- UI LINCAT

- EtherCAT

- PLC integrado

- Drivers

- Documentación

- Arquitectura

- Ciclo de control

Es la referencia rápida para cualquier desarrollador u operador.

# ⭐ **2. Términos generales**

### **CNC**

Control Numérico Computarizado. Sistema que controla máquinas mediante coordenadas.

### **CNC‑CAT**

Motor CNC modular, moderno e industrial diseñado desde cero.

### **LINCAT**

UI oficial del ecosistema CNC‑CAT.

### **Motion API**

Interfaz universal entre UI y motores (sim/real).

### **Core**

Núcleo lógico del motor CNC‑CAT.

# ⭐ **3. Términos del ciclo de control**

### **Control Cycle**

Bucle periódico que ejecuta:

Código

```
`read\_inputs → update\_state → planner\_step → write\_outputs → send\_events`
```

### **Planner**

Convierte G‑code en trayectorias.

### **Interpolator**

Genera puntos a 1 kHz para los servos.

### **Trajectory**

Trayectoria completa generada por el planner.

### **TrajectoryPoint**

Punto interpolado enviado al servo.

# ⭐ **4. Términos de estados y alarmas**

### **INIT**

Sistema arrancando.

### **IDLE**

Sistema encendido pero sin homing.

### **READY**

Sistema homing completado.

### **RUNNING**

Programa en ejecución.

### **PAUSED**

Ejecución detenida temporalmente.

### **STOPPING**

Detención controlada.

### **ERROR**

Fallo recuperable.

### **ESTOP**

Fallo crítico. Requiere intervención humana.

### **Alarm**

Condición anómala detectada por el sistema.

# ⭐ **5. Términos de G‑code**

### **G‑code**

Lenguaje estándar para controlar máquinas CNC.

### **G0**

Movimiento rápido.

### **G1**

Movimiento lineal.

### **G2/G3**

Movimiento circular.

### **M‑codes**

Comandos auxiliares (husillo, refrigerante, etc.).

### **Offsets**

Desplazamientos de referencia (G54–G59).

# ⭐ **6. Términos de EtherCAT**

### **EtherCAT**

Protocolo industrial de comunicación en tiempo real.

### **PDO**

Process Data Object. Datos cíclicos.

### **SDO**

Service Data Object. Configuración.

### **DC Sync**

Distributed Clocks. Sincronización precisa.

### **Slave**

Dispositivo EtherCAT (servo, IO, etc.).

### **Master**

Controlador EtherCAT (PC).

# ⭐ **7. Términos del PLC integrado**

### **ST**

Structured Text. Lenguaje IEC 61131‑3.

### **AST**

Árbol sintáctico del código ST.

### **Bytecode**

Código intermedio ejecutado por el runtime del PLC.

### **Task**

Tarea cíclica del PLC.

# ⭐ **8. Términos de UI LINCAT**

### **Panel**

Sección visual de la UI (jog, offsets, herramientas, etc.).

### **Widget**

Elemento visual (botón, slider, etc.).

### **Event**

Evento generado por la UI o el motor.

### **Signal/Slot**

Mecanismo Qt para comunicación interna.

# ⭐ **9. Términos de drivers**

### **Driver**

Interfaz entre CNC‑CAT y hardware real.

### **RealIO**

Capa que abstrae entradas y salidas reales.

### **RealMotionController**

Controlador de movimiento real conectado a EtherCAT.

# ⭐ **10. Términos de documentación**

### **MkDocs**

Sistema para generar documentación web.

### **Pandoc**

Herramienta para generar PDF.

### **Changelog**

Registro de cambios del proyecto.

# ⭐ **11. Objetivo final**

Este glosario garantiza:

- claridad

- coherencia

- comunicación precisa

- comprensión rápida

- profesionalidad

Es la referencia oficial del ecosistema.


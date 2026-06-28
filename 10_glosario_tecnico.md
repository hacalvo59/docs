# 📘 **10\_glosario\_tecnico.md**

**Glosario técnico oficial del ecosistema CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Este glosario define **todos los términos técnicos** utilizados en:

- CNC‑CAT Core

- Motion API

- UI LINCAT

- EtherCAT

- PLC integrado

- Drivers

- Arquitectura

- Ciclo de control

- Documentación técnica

Es la referencia rápida para desarrolladores, integradores y operadores.

# ⭐ 2. Términos de arquitectura

### **CNC‑CAT**

Motor CNC modular, moderno e industrial.

### **LINCAT**

Interfaz humana del sistema CNC‑CAT.

### **Motion API**

Interfaz universal entre UI y motores (sim/real).

### **CORE**

Núcleo lógico del motor CNC‑CAT.

### **Drivers**

Capa que conecta el motor real con el hardware físico.

### **Motor simulado**

Implementación virtual para pruebas sin hardware.

### **Motor real**

Implementación física conectada a EtherCAT.

# ⭐ 3. Términos del ciclo de control

### **Control Cycle**

Bucle periódico del motor CNC.

### **read\_inputs**

Lectura de sensores, estados y entradas.

### **update\_state**

Actualización del estado interno del sistema.

### **planner\_step**

Ejecución del planificador de trayectorias.

### **write\_outputs**

Envío de comandos a servos y actuadores.

### **send\_events**

Comunicación de eventos a la UI.

# ⭐ 4. Términos de planificación y movimiento

### **Planner**

Convierte G‑code en trayectorias.

### **Interpolator**

Genera puntos interpolados a 1 kHz.

### **Trajectory**

Trayectoria completa generada por el planner.

### **TrajectoryPoint**

Punto interpolado enviado al servo.

### **Feedrate**

Velocidad de avance.

### **Acceleration / Jerk**

Parámetros de suavidad del movimiento.

# ⭐ 5. Términos de estados y alarmas

### **INIT**

Sistema arrancando.

### **IDLE**

Sistema encendido sin homing.

### **READY**

Homing completado.

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

# ⭐ 6. Términos de G‑code

### **G‑code**

Lenguaje estándar para controlar máquinas CNC.

### **G0 / G1**

Movimientos rápidos y lineales.

### **G2 / G3**

Movimientos circulares.

### **M‑codes**

Comandos auxiliares (husillo, refrigerante, etc.).

### **Offsets (G54–G59)**

Sistemas de coordenadas de pieza.

# ⭐ 7. Términos de EtherCAT

### **EtherCAT**

Protocolo industrial de tiempo real.

### **Master**

Controlador EtherCAT (PC).

### **Slave**

Dispositivo EtherCAT (servo, IO, etc.).

### **PDO**

Process Data Object (datos cíclicos).

### **SDO**

Service Data Object (configuración).

### **DC Sync**

Distributed Clocks (sincronización precisa).

### **Watchdog**

Supervisión de tiempo real.

# ⭐ 8. Términos del PLC integrado

### **ST (Structured Text)**

Lenguaje IEC 61131‑3.

### **AST**

Árbol sintáctico del código ST.

### **Bytecode**

Código intermedio ejecutado por el runtime.

### **Task**

Tarea cíclica del PLC.

### **Runtime**

Máquina virtual que ejecuta el bytecode.

# ⭐ 9. Términos de UI LINCAT

### **Panel**

Sección visual de la UI.

### **Widget**

Elemento visual (botón, slider, etc.).

### **Signal / Slot**

Mecanismo Qt para comunicación interna.

### **Event**

Evento generado por UI o motor.

### **DRO**

Digital Read Out (posición en tiempo real).

# ⭐ 10. Términos de drivers y hardware

### **RealIO**

Capa que abstrae entradas y salidas reales.

### **RealMotionController**

Controlador de movimiento conectado a EtherCAT.

### **Servo**

Motor controlado electrónicamente.

### **Encoder**

Sensor de posición.

### **Homing switch**

Sensor de referencia.

### **Limit switch**

Sensor de límite físico.

# ⭐ 11. Términos de documentación

### **MkDocs**

Sistema para generar documentación web.

### **Pandoc**

Herramienta para generar PDF.

### **Changelog**

Registro de cambios del proyecto.

### **Estándares**

Normas de estilo, formato y estructura.

# ⭐ 12. Objetivo final

Este glosario garantiza:

- claridad

- coherencia

- comunicación precisa

- comprensión rápida

- profesionalidad

Es la referencia técnica oficial del ecosistema.


# **02 — Arquitectura del Ecosistema LINCAT / CNC‑CAT**

## **2.1 Visión general de la arquitectura**

El ecosistema LINCAT/CNC‑CAT está diseñado como una plataforma industrial modular, escalable y profesional para automatización basada en Linux y EtherCAT. Su arquitectura se compone de capas independientes, cada una con responsabilidades claras, que interactúan mediante interfaces estables y documentadas.

El objetivo es garantizar:

- robustez industrial,

- mantenibilidad a largo plazo,

- independencia tecnológica,

- interoperabilidad entre módulos,

- escalabilidad sin romper compatibilidad,

- claridad conceptual para integradores y fabricantes.

## **2.2 Capas principales del ecosistema**

### **Capa 1 — UI LINCAT (Interfaz Humana)**

Responsable de:

- operación CNC,

- configuración de máquina,

- diagnóstico,

- PLC,

- EtherCAT,

- CAM,

- operación remota.

No contiene lógica de control. Es la capa visual y de interacción.

### **Capa 2 — Motion API (Interfaz de Movimiento)**

Es la frontera entre la UI y el motor CNC‑CAT.

Garantiza:

- independencia entre UI y motor,

- estabilidad a largo plazo,

- intercambiabilidad de motores (sim/real),

- claridad en los comandos y estados.

### **Capa 3 — CNC‑CAT (Motor CNC Industrial)**

Incluye:

- planificación de trayectorias,

- interpolación,

- parsing de G‑code,

- estados del sistema,

- alarmas,

- ciclo de control,

- ejecución en tiempo real.

Se divide en:

- **common/** → lógica pura

- **sim/** → implementación simulada

- **real/** → implementación física

### **Capa 4 — EtherCAT Layer (Capa de Campo)**

Responsable de:

- comunicación con esclavos EtherCAT,

- topología,

- estados,

- diagnóstico,

- IO en tiempo real,

- sincronización distribuida.

### **Capa 5 — PLC Integrado**

Incluye:

- editor ST,

- compilador,

- runtime,

- debugger,

- mapeo de IO,

- integración con CNC‑CAT.

### **Capa 6 — Drivers y Hardware**

Incluye:

- drivers EtherCAT,

- drivers IO,

- drivers de dispositivos,

- sensores,

- actuadores,

- motores,

- husillos.

## **2.3 Interacción entre capas**

La interacción se realiza mediante:

- APIs estables,

- eventos,

- estados,

- mensajes estructurados,

- protocolos internos documentados.

Cada capa puede evolucionar sin romper a las demás.

## **2.4 Filosofía de diseño arquitectónico**

- **Separación estricta de responsabilidades**

- **Modularidad extrema**

- **Interfaces claras y documentadas**

- **Evolución sin ruptura**

- **Independencia de terceros**

- **Preparado para décadas de mantenimiento**

## **2.5 Objetivo final de la arquitectura**

Crear un ecosistema industrial completo, libre, profesional y global, capaz de competir con:

- Siemens TIA Portal

- Beckhoff TwinCAT

- Fanuc iHMI

- Mach4

- Haas NextGen Control

pero basado en Linux, abierto, moderno y accesible para todo el mundo.


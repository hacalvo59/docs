# **05 — Capa EtherCAT (EtherCAT Layer)**

**Comunicación Industrial en Tiempo Real**

## **5.1 Propósito de la capa EtherCAT**

La capa EtherCAT es la columna vertebral del ecosistema CNC‑CAT. Su misión es proporcionar comunicación industrial determinista, rápida y confiable entre:

- el motor CNC‑CAT,

- los esclavos EtherCAT,

- los dispositivos de campo,

- los sensores y actuadores,

- los servomotores,

- el PLC integrado.

EtherCAT es el estándar industrial más eficiente para control de movimiento moderno, y CNC‑CAT lo adopta como **tecnología nativa**, no como adaptación.

## **5.2 Objetivos principales de la capa EtherCAT**

- Comunicación determinista en tiempo real.

- Sincronización precisa entre ejes.

- Diagnóstico completo de la red.

- Detección de fallos en milisegundos.

- Topología dinámica y auto‑descubrible.

- Integración directa con el ciclo de control CNC.

- Mapeo claro de IO para PLC y CNC.

- Compatibilidad con dispositivos industriales estándar.

## **5.3 Arquitectura interna de la capa EtherCAT**

La capa EtherCAT se divide en módulos:

Código

```
`ethercat/`

`    master/         → comunicación con el maestro EtherCAT`

`    topology/       → detección y representación de la red`

`    diagnostics/    → estados, alarmas, errores`

`    io\_mapping/     → mapeo de entradas y salidas`

`    devices/        → perfiles de dispositivos`

`    sync/           → sincronización distribuida (DC)`
```

## **5.4 Componentes principales**

### **5.4.1 EtherCAT Master**

Responsable de:

- inicializar la red,

- escanear esclavos,

- configurar PDOs y SDOs,

- gestionar estados (INIT, PRE‑OP, SAFE‑OP, OP),

- enviar y recibir frames,

- mantener la comunicación determinista.

### **5.4.2 Topología EtherCAT**

Debe detectar automáticamente:

- número de esclavos,

- orden físico,

- tipo de dispositivo,

- direcciones,

- perfiles,

- capacidades,

- estados.

La UI LINCAT mostrará la topología en tiempo real.

### **5.4.3 Diagnóstico y estados**

Cada esclavo EtherCAT debe reportar:

- estado actual (INIT, PRE‑OP, SAFE‑OP, OP),

- errores,

- warnings,

- fallos de comunicación,

- fallos de sincronización,

- fallos de PDO/SDO,

- fallos de alimentación,

- fallos de hardware.

La UI debe mostrar:

- colores IEC,

- iconos ISO,

- mensajes traducibles,

- acciones recomendadas.

### **5.4.4 Mapeo de IO (IO Mapping)**

El mapeo debe ser:

- claro,

- estable,

- documentado,

- accesible desde la UI,

- accesible desde el PLC,

- accesible desde el motor CNC.

Cada variable debe tener:

- nombre lógico,

- tipo,

- dirección,

- esclavo asociado,

- PDO asociado.

### **5.4.5 Perfiles de dispositivos**

La capa EtherCAT debe soportar:

- servomotores,

- drivers de ejes,

- encoders,

- módulos de IO digital,

- módulos analógicos,

- sensores industriales,

- actuadores neumáticos,

- variadores de frecuencia,

- módulos de seguridad.

Cada dispositivo tendrá un perfil:

- parámetros,

- modos de operación,

- PDOs,

- SDOs,

- alarmas,

- capacidades.

### **5.4.6 Sincronización distribuida (Distributed Clocks)**

La sincronización DC es esencial para:

- interpolación precisa,

- control multi‑eje,

- homing sincronizado,

- movimientos coordinados,

- estabilidad del ciclo de control.

CNC‑CAT debe sincronizar su ciclo con el reloj EtherCAT.

## **5.5 Integración con el motor CNC‑CAT**

El motor CNC‑CAT utiliza EtherCAT para:

- leer encoders,

- controlar servos,

- activar salidas,

- leer sensores,

- ejecutar homing,

- detectar límites,

- sincronizar ejes,

- ejecutar movimientos en tiempo real.

La integración es directa y nativa.

## **5.6 Integración con el PLC**

El PLC integrado debe poder:

- leer cualquier variable EtherCAT,

- escribir salidas,

- activar secuencias,

- controlar periféricos,

- supervisar estados,

- reaccionar a alarmas.

El mapeo de IO debe ser accesible desde la UI.

## **5.7 Integración con la UI LINCAT**

La UI debe mostrar:

- topología completa,

- estados de cada esclavo,

- alarmas,

- PDOs y SDOs,

- variables en tiempo real,

- gráficas de diagnóstico,

- tiempos de ciclo,

- sincronización DC.

## **5.8 Objetivo final de la capa EtherCAT**

Crear una capa EtherCAT:

- profesional,

- robusta,

- clara,

- moderna,

- industrial,

- totalmente integrada,

- digna de un estándar mundial.

EtherCAT es el corazón del sistema. CNC‑CAT y LINCAT deben latir al ritmo de EtherCAT.


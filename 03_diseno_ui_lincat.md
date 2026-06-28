# **03 — Diseño de la UI LINCAT**

## **3.1 Propósito del diseño UI**

La interfaz gráfica de LINCAT es el punto de contacto entre el ser humano y el ecosistema industrial CNC‑CAT. Su diseño debe cumplir simultáneamente con:

- **claridad operativa**,

- **profesionalismo industrial**,

- **ergonomía**,

- **consistencia visual**,

- **multilingüismo**,

- **robustez**,

- **estética moderna**,

- **accesibilidad**,

- **operación remota**.

La UI no es un accesorio: **es el centro de operación del sistema industrial completo.**

## **3.2 Principios de diseño visual**

### **Claridad industrial**

Toda la información debe ser legible, directa y sin ambigüedades.

### **Consistencia absoluta**

Todos los módulos deben compartir:

- tipografías,

- colores,

- iconografía,

- espaciados,

- patrones de interacción.

### **Diseño modular**

Cada panel debe ser independiente, intercambiable y escalable.

### **Diseño multilingüe desde el origen**

La UI debe adaptarse a:

- textos largos (alemán),

- textos cortos (chino),

- alfabetos distintos.

### **Ergonomía para operadores**

Botones grandes, claros, accesibles. Información crítica siempre visible.

### **Profundidad para ingenieros**

Paneles avanzados, configuraciones detalladas, diagnósticos completos.

### **Estética moderna**

Inspirada en:

- Mach4,

- Siemens iHMI,

- Beckhoff TwinCAT HMI,

- Haas NextGen Control.

## **3.3 Estructura general de la UI**

La UI LINCAT se organiza en **módulos principales**, accesibles mediante pestañas o paneles laterales:

1. **CNC — Programa**

2. **CNC — Ejecución**

3. **CNC — Overrides**

4. **CNC — Estado de máquina**

5. **CNC — Movimiento (Jog + DRO + Home)**

6. **CNC — Offsets G54–G59**

7. **CNC — Herramientas**

8. **CNC — MDI**

9. **CNC — Alarmas**

10. **PLC — Editor ST + Debugger**

11. **EtherCAT — Topología + Diagnóstico**

12. **Sistema — Logs + Servicios**

13. **Configuración de máquina**

14. **Operación remota**

Cada módulo es independiente, pero todos comparten la misma base visual.

## **3.4 Reglas visuales y de interacción**

### **Tipografía**

- Fuente industrial clara (ej. Inter, Roboto, Noto Sans).

- Tamaños adaptados a paneles táctiles.

### **Colores (IEC 60204‑1)**

- **Verde** → Estado OK

- **Amarillo** → Advertencia

- **Rojo** → Error / Parada

- **Azul** → Información

- **Gris** → Elementos pasivos

### **Iconografía (ISO 7000 / IEC 60417)**

- Home, Jog, E‑STOP, Play, Pause, Stop, Tool, Alarm, EtherCAT, PLC, etc.

### **Controles**

- Botones grandes para operación.

- Sliders para overrides.

- Tablas para offsets y herramientas.

- Gráficos para estados y diagnósticos.

- Paneles plegables para configuraciones avanzadas.

### **Jerarquía visual**

- Información crítica siempre arriba.

- Controles de ejecución centrados.

- Configuración avanzada en paneles secundarios.

## **3.5 Diseño para operación remota**

La UI debe permitir:

- control remoto seguro,

- visualización en tiempo real,

- acceso desde escritorio, tablet o panel industrial,

- autenticación por roles,

- permisos granulares (operador, técnico, ingeniero, administrador).

## **3.6 Diseño para integradores y fabricantes**

La UI debe incluir:

- paneles de diagnóstico profundo,

- configuración de máquina,

- mapeo de IO,

- topología EtherCAT,

- estados de esclavos,

- alarmas detalladas,

- herramientas de calibración.

## **3.7 Objetivo final del diseño UI**

Crear una interfaz:

- profesional,

- moderna,

- clara,

- robusta,

- internacional,

- extensible,

- digna de un estándar mundial.


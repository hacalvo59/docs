# ⭐ **Roadmap Técnico — Ecosistema LINCAT / CNC‑CAT**

**v1.0 → v2.0 → v3.0**

# **1. Objetivo del Roadmap**

Este roadmap define:

- fases de desarrollo,

- prioridades técnicas,

- dependencias entre módulos,

- entregables por versión,

- visión industrial a largo plazo.

Es la guía estratégica del ecosistema.

# **2. v1.0 — Arquitectura completa (Estado: ✔ Completado)**

### **2.1 Documentación**

- ✔ Documento Maestro (00–10)

- ✔ Documentación técnica (technical/)

- ✔ Índice general

- ✔ README maestro

- ✔ README GitHub

- ✔ Diagrama general

### **2.2 Arquitectura de software**

- ✔ UI LINCAT v1 (estructura, paneles, eventos)

- ✔ Motion API (contrato universal)

- ✔ CNC‑CAT Core (models, gcode, planner base, states)

- ✔ Motor simulado completo

- ✔ EtherCAT Layer (diseño)

- ✔ PLC integrado (diseño)

- ✔ Drivers (diseño)

### **2.3 Infraestructura**

- ✔ Estructura de carpetas

- ✔ Estándares visuales

- ✔ Estándares de documentación

**Resultado:** Una arquitectura industrial completa, documentada y lista para implementación.

# **3. v2.0 — Implementación del ecosistema (Estado: ⏳ Próximo)**

### **3.1 CNC‑CAT (motor real)**

- Implementación del planner real

- Interpolador 1 kHz

- Control multi‑eje

- Homing real

- Límites físicos

- Control de husillo

- Alarmas reales

- Estados completos

### **3.2 EtherCAT Layer**

- EtherCAT master operativo

- PDO/SDO mapping

- Topología dinámica

- Diagnóstico en tiempo real

- Sincronización DC

- Drivers EtherCAT (servos, encoders, IO)

### **3.3 PLC integrado**

- Compilador ST → bytecode

- Runtime determinista

- Debugger en tiempo real

- IO mapping EtherCAT

- Tareas cíclicas y event‑driven

### **3.4 UI LINCAT v2**

- Paneles finales

- Editor ST completo

- Debugger PLC

- Topología EtherCAT

- Simulación 3D

- MDI avanzado

- Panel de alarmas industrial

- Panel de offsets y herramientas profesional

### **3.5 Simulación**

- Simulación 3D

- Simulación de IO

- Simulación de servos

- Simulación de alarmas

### **3.6 CAM**

- Postprocesador CNC‑CAT

- Integración con BlenderCAM

- Vista previa de trayectorias

**Resultado esperado:** Un ecosistema **funcional**, capaz de mover máquinas reales y simular máquinas virtuales.

# **4. v3.0 — Industrialización (Estado: 🔜 Futuro)**

### **4.1 Hardware industrial**

- Panel táctil industrial

- Control remoto seguro

- Integración con armarios eléctricos reales

- Integración con servos industriales

### **4.2 Seguridad**

- Safety IO

- Safety relays

- Safety door

- Safety PLC (opcional)

- Certificación CE/ISO

### **4.3 Ecosistema**

- Marketplace de módulos

- Plugins de terceros

- Integración con robots

- Integración con SCADA

- Integración con MES

### **4.4 Distribución**

- Imagen ISO industrial

- Instalador Debian

- Actualizaciones OTA

- Documentación web (MkDocs / GitHub Pages)

**Resultado esperado:** Un producto industrial completo, competitivo y libre.

# **5. Dependencias entre versiones**

Código

```
`v1.0 → define arquitectura`

`v2.0 → implementa arquitectura`

`v3.0 → industrializa arquitectura`
```

# **6. Prioridades estratégicas**

1. **Estabilidad del CORE**

2. **Determinismo del ciclo de control**

3. **Sincronización EtherCAT**

4. **UI profesional y clara**

5. **PLC integrado robusto**

6. **Simulación completa**

7. **Documentación impecable**

# **7. Objetivo final**

Convertir LINCAT / CNC‑CAT en:

- un estándar industrial libre,

- modular,

- profesional,

- escalable,

- documentado,

- seguro,

- global.


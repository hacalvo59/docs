# 📘 **TESTING\_GUIDE.md**

**Guía oficial de pruebas del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Esta guía define **cómo se prueban todos los módulos** del ecosistema:

- CNC‑CAT Core

- Motion API

- UI LINCAT

- EtherCAT Layer

- PLC integrado

- Drivers

- Motores (sim/real)

- Documentación

El objetivo es garantizar un sistema **estable, determinista y apto para uso industrial**.

# ⭐ 2. Tipos de pruebas

El ecosistema utiliza cuatro niveles de pruebas:

Código

```
`Unit tests`

`Integration tests`

`Hardware-in-the-loop (HIL)`

`End-to-end (E2E)`
```

# ⭐ 3. Pruebas unitarias (Unit Tests)

### **3.1 Objetivo**

Validar funciones y clases individuales.

### **3.2 Módulos cubiertos**

- Core (models, math, planner base)

- Parser G‑code

- Motion API (validación de comandos)

- PLC (parser ST, AST, bytecode)

### **3.3 Herramientas**

- pytest

- mocks para IO y EtherCAT

### **3.4 Reglas**

- Cada función crítica debe tener test

- Cada bug corregido debe tener test

- Cobertura mínima recomendada: **70%**

# ⭐ 4. Pruebas de integración (Integration Tests)

### **4.1 Objetivo**

Validar que los módulos funcionan juntos.

### **4.2 Casos típicos**

- Motion API ↔ Core

- Core ↔ Planner ↔ Interpolador

- PLC ↔ IO virtual

- UI LINCAT ↔ Motion API (mock)

### **4.3 Reglas**

- No usar hardware real

- Simulación obligatoria

- Validar estados, alarmas y transiciones

# ⭐ 5. Pruebas Hardware-in-the-loop (HIL)

### **5.1 Objetivo**

Validar el comportamiento del sistema con hardware real:

- servos

- encoders

- IO

- EtherCAT

### **5.2 Requisitos**

- banco de pruebas seguro

- E‑STOP físico

- límites mecánicos

- supervisión humana

### **5.3 Casos típicos**

- Homing real

- Movimiento lineal

- Movimiento circular

- Pérdida de sincronía EtherCAT

- Fallo de servo

- Alarmas reales

# ⭐ 6. Pruebas end-to-end (E2E)

### **6.1 Objetivo**

Validar el flujo completo:

Código

```
`UI → Motion API → Core → Motor → EtherCAT → Drivers → Hardware`
```

### **6.2 Casos típicos**

- Cargar programa

- Ejecutar G‑code

- Pausar / Reanudar

- Parada segura

- Parada de emergencia

- Alarmas

- Offsets y herramientas

# ⭐ 7. Pruebas de UI LINCAT

### **7.1 Objetivo**

Validar:

- paneles

- eventos

- señales/slots

- estados

- errores

- rendimiento

### **7.2 Herramientas**

- pytest-qt

- simulación de eventos

# ⭐ 8. Pruebas del PLC integrado

### **8.1 Objetivo**

Validar:

- parser ST

- AST

- bytecode

- runtime determinista

- debugger

### **8.2 Casos típicos**

- variables

- temporizadores

- tareas cíclicas

- acceso a IO

- errores de compilación

# ⭐ 9. Pruebas de EtherCAT

### **9.1 Objetivo**

Validar:

- estados del master

- PDO/SDO

- sincronización DC

- watchdog

- topología

### **9.2 Casos típicos**

- INIT → PREOP → SAFEOP → OP

- pérdida de esclavo

- error de PDO

- error de sincronía

# ⭐ 10. Pruebas de documentación

### **10.1 Objetivo**

Garantizar:

- enlaces correctos

- estructura coherente

- ausencia de duplicados

- consistencia visual

### **10.2 Herramientas**

- mkdocs build

- validadores de enlaces

# ⭐ 11. Automatización de pruebas

### **11.1 CI recomendado**

- GitHub Actions

- GitLab CI

- Jenkins

### **11.2 Pasos**

1. Instalar dependencias

2. Ejecutar unit tests

3. Ejecutar integration tests

4. Validar documentación

5. Generar artefactos

# ⭐ 12. Objetivo final

Garantizar que el ecosistema LINCAT / CNC‑CAT sea:

- estable

- determinista

- seguro

- industrial

- confiable

- apto para producción


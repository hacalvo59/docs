# 📘 **README\_GITHUB.md**

*(Versión pública para repositorio GitHub)*

# **LINCAT / CNC‑CAT — Plataforma Industrial Libre**

**CNC · PLC · EtherCAT · CAM · UI · Simulación · Linux**


## ⭐ **Descripción del proyecto**

LINCAT y CNC‑CAT forman un ecosistema industrial moderno, modular y completamente libre, diseñado para:

- control CNC profesional,

- automatización mediante PLC integrado,

- comunicación en tiempo real con EtherCAT,

- flujo CAM → CNC completo,

- operación remota,

- UI moderna y multilingüe,

- arquitectura escalable y mantenible sobre Linux.

El objetivo es crear **la plataforma industrial libre más completa del mundo**, sin firmware propietario, sin licencias por eje y con una arquitectura clara y profesional.

## ⭐ **Características principales**

- UI industrial moderna (Qt6)

- Motor CNC modular (planner, interpolador, parser G‑code)

- PLC integrado (ST, runtime determinista, debugger)

- EtherCAT master nativo

- Drivers industriales (servos, encoders, IO)

- Motor simulado completo

- Motor real con sincronización DC

- Documentación profesional

- Arquitectura limpia y extensible

## ⭐ **Arquitectura general**

text

```
`\[ UI LINCAT \]`

`      ↓`

`\[ Motion API \]`

`      ↓`

`\[ CNC‑CAT Core \]`

`      ↓`

`\[ Motores \]`

`   ├─ Simulado`

`   └─ Real (EtherCAT)`

`      ↓`

`\[ Drivers \]`

`      ↓`

`\[ Hardware \]`
```

## ⭐ **Instalación (Linux)**

bash

```
`sudo apt install python3 python3-pip qt6-base-dev`

`git clone https://github.com/tuusuario/lincat.git`

`cd lincat`

`pip install -r requirements.txt`

`python3 lincat.py`
```

## ⭐ **Estructura del repositorio**

text

```
`lincat/`

` ├─ ui/`

` ├─ motion\_api/`

` ├─ cnc\_cat/`

` │    ├─ core/`

` │    ├─ simulation/`

` │    └─ real/`

` ├─ ethercat/`

` ├─ plc/`

` ├─ drivers/`

` └─ docs/`
```

## ⭐ **Capturas (placeholders)**

> *(Sustituir cuando tengas capturas reales)*

- UI principal

- Panel CNC

- Panel PLC

- Topología EtherCAT

- Simulación 3D

## ⭐ **Roadmap**

### **v1.0 — Arquitectura**

- Documento Maestro

- UI LINCAT v1

- CNC‑CAT Core

- EtherCAT Layer

- PLC integrado

- Motor simulado

### **v2.0 — Implementación**

- Motor real completo

- Planner avanzado

- Interpolador 1 kHz

- Postprocesador CAM

- Paneles UI finales

### **v3.0 — Industrialización**

- Panel táctil industrial

- Seguridad avanzada

- Integración con máquinas reales

- Certificación CE/ISO

## ⭐ **Documentación**

Toda la documentación oficial está en:

Código

```
`C\_Pilot\_Docs/`
```

Incluye:

- Documento Maestro (00–10)

- Documentación técnica (technical/)

- Índice general

- Diagramas

## ⭐ **Licencia**

Proyecto **100% libre**, orientado a uso industrial profesional.

## ⭐ **Contribuciones**

Pull requests bienvenidas. Se aceptan mejoras en:

- UI

- drivers

- EtherCAT

- planner

- documentación

## ⭐ **Objetivo final**

Construir un ecosistema industrial libre, modular y profesional que unifique:

- CNC

- PLC

- EtherCAT

- CAM

- UI

- Simulación

- Documentación

Todo sobre Linux. Todo modular. Todo profesional.


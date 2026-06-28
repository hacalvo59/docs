# 📘 **CONFIGURATION\_GUIDE.md**

**Guía oficial de configuración del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Esta guía define **cómo configurar** todos los componentes del ecosistema:

- UI LINCAT

- Motion API

- CNC‑CAT Core

- Motores (sim/real)

- EtherCAT Layer

- PLC integrado

- Drivers

- Parámetros de máquina

- Offsets y herramientas

El objetivo es garantizar una configuración **coherente, segura y profesional**.

# ⭐ 2. Estructura general de configuración

El ecosistema utiliza archivos de configuración en formato **YAML**:

Código

```
`config/`

`    system.yaml`

`    machine.yaml`

`    ethercat.yaml`

`    ui.yaml`

`    plc.yaml`
```

Cada archivo tiene una responsabilidad clara.

# ⭐ 3. system.yaml

Define parámetros globales del ecosistema.

### **Ejemplo:**

yaml

```
`system:`

`  mode: simulation   \# simulation | real`

`  cycle\_time\_ms: 1`

`  logging: true`

`  log\_level: INFO`
```

### **Parámetros clave**

- `mode`: modo de operación

- `cycle\_time\_ms`: ciclo del interpolador

- `logging`: activar logs

- `log\_level`: nivel de detalle

# ⭐ 4. machine.yaml

Define la configuración física de la máquina.

### **Ejemplo:**

yaml

```
`machine:`

`  axes:`

`    X:`

`      steps\_per\_mm: 160`

`      max\_velocity: 5000`

`      max\_acceleration: 2000`

`      limits:`

`        min: -10`

`        max: 510`

`    Y:`

`      steps\_per\_mm: 160`

`      max\_velocity: 5000`

`      max\_acceleration: 2000`

`      limits:`

`        min: -10`

`        max: 510`
```

### **Parámetros clave**

- `steps\_per\_mm`

- `max\_velocity`

- `max\_acceleration`

- `limits`

- `homing`

- `soft\_limits`

# ⭐ 5. ethercat.yaml

Define la configuración del bus EtherCAT.

### **Ejemplo:**

yaml

```
`ethercat:`

`  master: eth0`

`  slaves:`

`    - name: AXIS\_X`

`      vendor\_id: 0x00000002`

`      product\_id: 0x12345678`

`      pdo:`

`        position: 0x6004`

`        velocity: 0x600C`

`        status: 0x6041`

`        control: 0x6040`
```

### **Parámetros clave**

- interfaz de red

- lista de esclavos

- PDO/SDO

- sincronización DC

- watchdog

# ⭐ 6. ui.yaml

Define la configuración de la UI LINCAT.

### **Ejemplo:**

yaml

```
`ui:`

`  theme: dark`

`  language: es`

`  panels:`

`    jog: true`

`    offsets: true`

`    tools: true`

`    diagnostics: true`
```

### **Parámetros clave**

- idioma

- tema

- paneles visibles

- refresco de datos

- límites visuales

# ⭐ 7. plc.yaml

Define la configuración del PLC integrado.

### **Ejemplo:**

yaml

```
`plc:`

`  cycle\_time\_ms: 10`

`  tasks:`

`    - name: main`

`      file: main.st`

`      priority: 1`
```

### **Parámetros clave**

- tiempo de ciclo

- tareas

- prioridades

- archivos ST

# ⭐ 8. Configuración del motor simulado

### **Ejemplo:**

yaml

```
`simulation:`

`  noise: false`

`  max\_velocity: 3000`

`  max\_acceleration: 1500`
```

### **Parámetros clave**

- ruido

- límites virtuales

- velocidad

- aceleración

# ⭐ 9. Configuración del motor real

### **Ejemplo:**

yaml

```
`real:`

`  servo\_timeout\_ms: 50`

`  enable\_watchdog: true`

`  emergency\_stop\_gpio: 17`
```

### **Parámetros clave**

- watchdog

- E‑STOP

- GPIO

- tiempos críticos

# ⭐ 10. Configuración de herramientas

### **Ejemplo:**

yaml

```
`tools:`

`  - id: 1`

`    length: 120.5`

`    diameter: 6.0`

`  - id: 2`

`    length: 98.2`

`    diameter: 3.0`
```

### **Parámetros clave**

- longitud

- diámetro

- offsets

- número de herramienta

# ⭐ 11. Configuración de offsets

### **Ejemplo:**

yaml

```
`offsets:`

`  g54:`

`    x: 0`

`    y: 0`

`    z: 0`

`  g55:`

`    x: 10`

`    y: 20`

`    z: -5`
```

### **Parámetros clave**

- G54–G59

- offsets de pieza

- offsets de máquina

# ⭐ 12. Validación de configuración

### **Comando:**

bash

```
`python3 validate\_config.py`
```

### **Validaciones:**

- límites coherentes

- EtherCAT correcto

- herramientas válidas

- offsets válidos

- parámetros de máquina correctos

# ⭐ 13. Objetivo final

Garantizar que el ecosistema LINCAT / CNC‑CAT esté configurado:

- correctamente

- de forma segura

- de forma coherente

- de forma industrial

- de forma profesional


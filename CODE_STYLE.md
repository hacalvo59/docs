# 📘 **CODE\_STYLE.md**

*(Guía oficial de estilo de código del ecosistema LINCAT / CNC‑CAT)*

# **Estilo de código oficial**

Este proyecto sigue un estilo industrial, claro y mantenible.

# ⭐ 1. Lenguaje

- Python 3.10+

- Qt6 para UI

- Estructura modular estricta

# ⭐ 2. Reglas generales

- Código limpio

- Funciones cortas

- Clases pequeñas

- Nombres descriptivos

- Nada de “magia”

- Nada de lógica oculta

- Nada de dependencias circulares

# ⭐ 3. Nombres

### **Clases**

`CamelCase`

### **Funciones**

`snake\_case`

### **Variables**

`snake\_case`

### **Constantes**

`UPPER\_CASE`

# ⭐ 4. Documentación interna

Cada módulo debe incluir:

- descripción

- responsabilidades

- dependencias

- ejemplos

Cada función debe incluir:

- docstring

- parámetros

- retorno

- errores posibles

# ⭐ 5. Estructura de carpetas

Código

```
`ui/`

`motion\_api/`

`cnc\_cat/`

`    core/`

`    simulation/`

`    real/`

`ethercat/`

`plc/`

`drivers/`

`docs/`
```

# ⭐ 6. Estilo Python

- PEP8

- 4 espacios

- imports ordenados

- evitar side-effects

- evitar funciones de más de 40 líneas

- evitar clases de más de 300 líneas

# ⭐ 7. Estilo Qt6

- Widgets en clases separadas

- Nada de lógica en el .ui

- Controladores limpios

- Señales y slots documentados

# ⭐ 8. Estilo CNC‑CAT Core

- Planner determinista

- Interpolador limpio

- Modelos inmutables cuando sea posible

- Estados claros

- Alarmas explícitas

# ⭐ 9. Estilo EtherCAT

- Drivers minimalistas

- Nada de lógica CNC

- Nada de lógica UI

- Solo IO + sincronización

# ⭐ 10. Estilo PLC

- Runtime determinista

- Bytecode claro

- Debugger seguro

- IO mapping explícito

# ⭐ 11. Estilo de pruebas

- Unit tests por módulo

- Tests de integración para Motion API

- Tests de simulación

- Tests de drivers virtuales

# ⭐ 12. Objetivo final

Código:

- claro

- mantenible

- industrial

- profesional

- escalable


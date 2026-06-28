# 📘 **DEPENDENCIES.md**

**Guía oficial de dependencias y librerías del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Este documento define:

- las dependencias oficiales del ecosistema,

- las librerías permitidas,

- las librerías prohibidas,

- las reglas de actualización,

- los criterios industriales para seleccionar dependencias.

El objetivo es garantizar un sistema **estable, mantenible y profesional**.

# ⭐ 2. Principios de selección de dependencias

### **2.1 Estabilidad**

Solo se aceptan librerías:

- mantenidas activamente,

- con comunidad sólida,

- con releases estables.

### **2.2 Longevidad**

Preferencia por librerías:

- con más de 5 años de desarrollo,

- con roadmap claro,

- con soporte a largo plazo.

### **2.3 Licencia**

Solo se aceptan:

- MIT

- BSD

- Apache 2.0

- LGPL

- GPL (solo si no afecta distribución)

### **2.4 Rendimiento**

Las dependencias deben ser:

- rápidas,

- eficientes,

- aptas para uso industrial.

### **2.5 Seguridad**

No se aceptan librerías:

- sin mantenimiento,

- con CVEs abiertos,

- con dependencias inseguras.

# ⭐ 3. Dependencias oficiales del ecosistema

## **3.1 Python**

- Python 3.10+

- pip para instalación

- venv recomendado

## **3.2 UI LINCAT**

- **PySide6 (Qt6)**

  - UI industrial

  - Widgets modernos

  - Señales/slots

  - Multiplataforma

## **3.3 CNC‑CAT Core**

- **numpy**

  - matemáticas

  - interpolación

  - vectores

- **scipy** *(opcional)*

  - cálculos avanzados

  - filtros

  - cinemática

## **3.4 EtherCAT Layer**

*(Dependencias opcionales según implementación)*

- **pysoem**

  - acceso a EtherCAT Master

  - PDO/SDO

  - estados del bus

## **3.5 PLC integrado**

- **lark-parser**

  - parsing del lenguaje ST

  - generación de AST

- **bytecode** *(opcional)*

  - generación de bytecode

  - ejecución segura

## **3.6 Drivers**

- Sin dependencias externas

- Solo acceso a EtherCAT Layer

- Código limpio y directo

## **3.7 Simulación**

- **matplotlib** *(opcional)*

  - visualización

  - gráficas

- **pyqtgraph** *(opcional)*

  - visualización rápida

  - paneles de diagnóstico

## **3.8 Documentación**

- **mkdocs**

- **mkdocs-material**

- **pandoc**

- **xelatex**

# ⭐ 4. Dependencias prohibidas

- Librerías sin mantenimiento

- Librerías con CVEs abiertos

- Librerías con licencia no compatible

- Librerías que introduzcan:

  - telemetría

  - tracking

  - dependencias ocultas

  - binarios no auditables

# ⭐ 5. Reglas de actualización

### **5.1 Actualizaciones menores**

Permitidas si:

- no rompen compatibilidad

- no cambian APIs críticas

- no afectan rendimiento

### **5.2 Actualizaciones mayores**

Requieren:

- revisión completa

- pruebas en simulación

- pruebas en hardware real

- actualización de documentación

### **5.3 Congelación**

En versiones estables (`main`):

- las dependencias quedan congeladas

- solo se permiten parches de seguridad

# ⭐ 6. Auditoría de dependencias

Cada release debe incluir:

- lista de dependencias

- versiones exactas

- hashes (si aplica)

- notas de seguridad

# ⭐ 7. Objetivo final

Garantizar que el ecosistema LINCAT / CNC‑CAT sea:

- estable

- seguro

- profesional

- mantenible

- industrial


# 📘 **VERSIONING.md**

**Guía oficial de versionado del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Definir cómo se versiona el ecosistema completo:

- UI LINCAT

- CNC‑CAT Core

- Motores

- EtherCAT Layer

- PLC integrado

- Drivers

- Documentación

# ⭐ 2. Esquema de versionado

Se usa **Semantic Versioning (SemVer)**:

Código

```
`MAJOR.MINOR.PATCH`
```

Ejemplos:

- `1.0.0`

- `1.2.3`

- `2.0.1`

# ⭐ 3. Significado de cada número

### **MAJOR**

Se incrementa cuando:

- hay cambios incompatibles

- se rompe la API

- se rediseña un módulo crítico

- se cambia la arquitectura

Ejemplo: `1.x.x → 2.0.0`

### **MINOR**

Se incrementa cuando:

- se añade funcionalidad nueva

- se amplía la API sin romperla

- se añaden módulos nuevos

- se mejora la UI

Ejemplo: `1.3.x → 1.4.0`

### **PATCH**

Se incrementa cuando:

- se corrigen bugs

- se mejora rendimiento

- se ajusta documentación

- se hacen cambios menores

Ejemplo: `1.4.2 → 1.4.3`

# ⭐ 4. Versionado del ecosistema completo

El ecosistema se versiona como **un todo**, no por módulos.

Ejemplo:

Código

```
`LINCAT / CNC‑CAT v1.0.0`
```

Incluye:

- UI

- Core

- Motores

- EtherCAT

- PLC

- Drivers

- Documentación

# ⭐ 5. Versionado de documentación

La documentación sigue la misma versión que el software.

Ejemplo:

Código

```
`Documentación v1.0.0`
```

# ⭐ 6. Versionado de diagramas

Los diagramas se actualizan cuando:

- cambia la arquitectura

- cambia un módulo

- cambia la API

# ⭐ 7. Versionado de la Motion API

La Motion API tiene versión propia **y** sigue SemVer.

Ejemplo:

Código

```
`Motion API v1.2.0`
```

# ⭐ 8. Versionado de la UI LINCAT

La UI sigue la versión global del ecosistema.

# ⭐ 9. Objetivo final

Un versionado:

- claro

- profesional

- coherente

- industrial

- fácil de seguir


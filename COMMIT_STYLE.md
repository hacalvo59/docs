# 📘 **COMMIT\_STYLE.md**

**Guía oficial de estilo de commits del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Definir un estándar claro, industrial y consistente para todos los commits del proyecto.

Los commits deben ser:

- legibles

- estructurados

- consistentes

- útiles para el historial

- fáciles de buscar

# ⭐ 2. Formato obligatorio

Cada commit debe seguir este formato:

Código

```
`tipo: descripción corta`


`Descripción larga opcional.`
```

Ejemplos:

Código

```
`feat: añadir soporte para homing incremental`

`fix: corregir error en interpolador 1 kHz`

`docs: actualizar documentación del PLC`

`refactor: simplificar MotionController`
```

# ⭐ 3. Tipos permitidos

- **feat:** nueva funcionalidad

- **fix:** corrección de bug

- **docs:** documentación

- **style:** formato, espacios, comas

- **refactor:** cambio interno sin alterar comportamiento

- **perf:** mejora de rendimiento

- **test:** pruebas

- **build:** cambios en build system

- **ci:** cambios en pipelines

- **chore:** tareas menores

# ⭐ 4. Reglas de estilo

- Descripción corta ≤ 72 caracteres

- Usar infinitivo (“añadir”, “corregir”, “actualizar”)

- No usar punto final

- No usar mayúscula inicial

- No mezclar varios cambios en un commit

- Un commit = un propósito

# ⭐ 5. Descripción larga (opcional)

Debe incluir:

- contexto

- motivación

- impacto

- referencias a issues

Ejemplo:

Código

```
`feat: añadir soporte para homing incremental`


`Se añade un nuevo modo de homing incremental para máquinas sin sensor absoluto.`

`Incluye validación de límites y actualización de offsets.`

`Relacionado con \#42.`
```

# ⭐ 6. Commits prohibidos

- “arreglos varios”

- “cambios”

- “update”

- “cosas”

- “pruebas”

- “fix” sin contexto

# ⭐ 7. Objetivo final

Un historial:

- limpio

- profesional

- navegable

- mantenible

- industrial


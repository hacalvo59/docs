# 📘 **12\_estandar\_commits.md**

**Estándar oficial de mensajes de commit — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir un estándar **claro, profesional y consistente** para todos los mensajes de commit del ecosistema CNC‑CAT.

Un buen commit:

- explica **qué** cambió,

- explica **por qué** cambió,

- permite rastrear errores,

- facilita revisiones,

- mejora la calidad del proyecto.

# ⭐ 2. Formato obligatorio del commit

Cada commit debe seguir esta estructura:

Código

```
`\<tipo\>: \<descripción breve\>`


`\<descripción extendida opcional\>`


`Refs: \<issue/PR\>`
```

Ejemplo:

Código

```
`fix: corregido cálculo de aceleración en interpolador`


`El interpolador no respetaba el jerk configurado.`

`Se añadió validación y test unitario.`


`Refs: \#142`
```

# ⭐ 3. Tipos oficiales de commit

| **Tipo** | **Uso** |
| :-: | :-: |
| **feat** | Nueva funcionalidad |
| **fix** | Corrección de errores |
| **docs** | Documentación |
| **style** | Formato, espacios, comas, sin cambiar lógica |
| **refactor** | Reestructuración sin cambiar comportamiento |
| **perf** | Mejoras de rendimiento |
| **test** | Añadir o corregir tests |
| **build** | Cambios en build, dependencias, entorno |
| **ci** | Cambios en pipelines CI/CD |
| **chore** | Tareas menores, limpieza |
| **revert** | Revertir un commit |

# ⭐ 4. Reglas estrictas

### ✔️ 4.1 La descripción breve debe ser:

- en **minúsculas**,

- sin punto final,

- clara y directa,

- máximo 72 caracteres.

### ✔️ 4.2 Un commit = un propósito

Nunca mezclar:

❌ código + documentación ❌ refactor + fix ❌ feature + limpieza

### ✔️ 4.3 Commits pequeños

Commits grandes → revisiones difíciles → errores ocultos.

### ✔️ 4.4 Siempre incluir tests en:

- feat

- fix

- refactor crítico

### ✔️ 4.5 Commits en inglés o español

Pero **consistentes dentro del mismo módulo**.

# ⭐ 5. Ejemplos correctos

### ✔️ Nueva funcionalidad

Código

```
`feat: añadir soporte para G38.x en parser`
```

### ✔️ Corrección de bug

Código

```
`fix: corregido límite suave en eje Y`
```

### ✔️ Documentación

Código

```
`docs: actualizar guía de configuración de EtherCAT`
```

### ✔️ Refactor

Código

```
`refactor: separar planner en módulos internos`
```

### ✔️ Test

Código

```
`test: añadir pruebas para homing simulado`
```

# ⭐ 6. Ejemplos incorrectos

### ❌ Demasiado genérico

Código

```
`update stuff`
```

### ❌ Mezcla de cambios

Código

```
`fix: corregido bug y reescrita la UI`
```

### ❌ Sin contexto

Código

```
`arreglado`
```

### ❌ Demasiado largo

Código

```
`fix: corregido un problema muy complejo relacionado con la interpolación...`
```

# ⭐ 7. Commits para releases

Los commits de release deben seguir este formato:

Código

```
`chore: release v1.2.0`
```

Y siempre acompañarse de:

- tag

- changelog actualizado

- rama release fusionada

# ⭐ 8. Commits para hotfix

Formato:

Código

```
`hotfix: corregido fallo crítico en EtherCAT`
```

Reglas:

- parte de `main`

- se fusiona también en `develop`

- prioridad absoluta

# ⭐ 9. Objetivo final

Este estándar garantiza:

- claridad

- trazabilidad

- profesionalismo

- revisiones rápidas

- historial limpio

- calidad industrial

Es el estándar oficial de commits del ecosistema CNC‑CAT.


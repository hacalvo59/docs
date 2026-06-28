# 📘 **BRANCHING\_MODEL.md**

**Modelo oficial de ramas del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Definir un modelo de ramas:

- claro

- profesional

- industrial

- escalable

- fácil de mantener

Este modelo garantiza que el desarrollo del ecosistema sea ordenado, seguro y predecible.

# ⭐ 2. Modelo base: “GitFlow Industrial Simplificado”

El ecosistema LINCAT / CNC‑CAT usa una variante simplificada de GitFlow, adaptada a proyectos industriales.

Las ramas principales son:

Código

```
`main`

`develop`

`feature/\*`

`fix/\*`

`hotfix/\*`

`release/\*`
```

# ⭐ 3. Ramas principales

## **3.1 main**

- Código **estable**

- Versiones **publicadas**

- Solo recibe merges desde `release/\*` o `hotfix/\*`

- Cada commit en `main` debe corresponder a una **versión SemVer**

Ejemplo:

Código

```
`v1.0.0`

`v1.1.0`

`v2.0.0`
```

## **3.2 develop**

- Código en desarrollo

- Recibe merges de `feature/\*` y `fix/\*`

- Debe estar siempre **compilable**

- No debe contener código experimental

# ⭐ 4. Ramas de trabajo

## **4.1 feature/**

Para nuevas funcionalidades.

Formato:

Código

```
`feature/nombre\_funcionalidad`
```

Ejemplos:

Código

```
`feature/planner\_1khz`

`feature/editor\_st`

`feature/ethercat\_master`
```

Reglas:

- Siempre desde `develop`

- Merge a `develop`

- Nunca a `main`

## **4.2 fix/**

Para correcciones de bugs.

Formato:

Código

```
`fix/nombre\_bug`
```

Ejemplos:

Código

```
`fix/overflow\_interpolador`

`fix/error\_ui\_offsets`
```

Reglas:

- Siempre desde `develop`

- Merge a `develop`

## **4.3 hotfix/**

Para correcciones urgentes en producción.

Formato:

Código

```
`hotfix/nombre\_critico`
```

Ejemplos:

Código

```
`hotfix/ethercat\_sync\_loss`

`hotfix/crash\_planner`
```

Reglas:

- Siempre desde `main`

- Merge a `main` **y** `develop`

## **4.4 release/**

Para preparar una versión estable.

Formato:

Código

```
`release/1.2.0`
```

Reglas:

- Siempre desde `develop`

- Se usa para:

  - pruebas finales

  - documentación

  - limpieza

- Merge a `main` (con tag)

- Merge a `develop`

# ⭐ 5. Flujo completo

Código

```
`feature/\* → develop → release/\* → main`

`                      ↑          ↓`

`                    hotfix/\* ←───`
```

# ⭐ 6. Reglas estrictas

- Nunca hacer commit directo en `main`

- Nunca mezclar varias funcionalidades en una rama

- Nunca mezclar fix + feature

- Cada PR debe ser pequeño y enfocado

- Cada merge debe seguir CODE\_STYLE.md

- Cada versión debe seguir VERSIONING.md

# ⭐ 7. Ejemplo real

### Crear una nueva funcionalidad:

Código

```
`git checkout develop`

`git checkout -b feature/planner\_1khz`
```

### Terminarla:

Código

```
`git checkout develop`

`git merge feature/planner\_1khz`

`git branch -d feature/planner\_1khz`
```

### Preparar versión:

Código

```
`git checkout -b release/1.1.0`
```

### Publicar:

Código

```
`git checkout main`

`git merge release/1.1.0`

`git tag v1.1.0`
```

# ⭐ 8. Objetivo final

Un flujo de trabajo:

- limpio

- profesional

- industrial

- escalable

- seguro

- mantenible

Perfecto para un ecosistema CNC real.


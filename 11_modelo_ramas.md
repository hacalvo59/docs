# 📘 **11\_modelo\_ramas.md**

**Modelo oficial de ramas (branching model) del ecosistema CNC‑CAT**

# ⭐ 1. Propósito

Definir un modelo de ramas:

- claro

- profesional

- escalable

- seguro

- compatible con CI/CD

- apto para desarrollo industrial

El objetivo es garantizar que **todo el código fluya de forma ordenada**, sin caos, sin conflictos innecesarios y sin romper la estabilidad del proyecto.

# ⭐ 2. Filosofía del modelo

El ecosistema CNC‑CAT utiliza un modelo híbrido inspirado en:

- Git Flow

- Trunk‑Based Development

- Versionado SemVer

La idea central:

👉 **main siempre debe ser estable** 👉 **develop concentra el trabajo activo** 👉 **las features viven en ramas cortas y limpias**

# ⭐ 3. Ramas principales

## **3.1 main**

- Código **estable**

- Solo recibe merges desde `release/\*`

- Cada commit en `main` debe corresponder a una **versión real**

- Protegida contra pushes directos

## **3.2 develop**

- Código en desarrollo

- Recibe merges de `feature/\*`

- Puede contener cambios no liberados

- No debe romper compilación

# ⭐ 4. Ramas secundarias

## **4.1 feature/**

Para nuevas funcionalidades.

**Reglas:**

- nombre: `feature/nombre\_claro`

- corta duración

- siempre parte de `develop`

- merge mediante PR

- incluir tests

Ejemplo:

Código

```
`feature/planner\_arc\_support`
```

## **4.2 hotfix/**

Para corregir errores críticos en producción.

**Reglas:**

- parte de `main`

- se fusiona en `main` y también en `develop`

- prioridad máxima

Ejemplo:

Código

```
`hotfix/ethercat\_sync\_loss`
```

## **4.3 release/**

Para preparar una versión estable.

**Reglas:**

- parte de `develop`

- solo fixes, documentación y ajustes menores

- se fusiona en `main` y `develop`

Ejemplo:

Código

```
`release/v1.0.0`
```

# ⭐ 5. Flujo completo de trabajo

Código

```
`feature → develop → release → main`
```

### **5.1 Desarrollo**

1. Crear rama feature

2. Implementar

3. Testear

4. PR hacia develop

### **5.2 Preparación de release**

1. Crear rama release

2. Congelar nuevas features

3. Solo fixes y documentación

4. PR hacia main

5. PR hacia develop

### **5.3 Hotfix**

1. Crear rama hotfix desde main

2. Corregir

3. PR hacia main

4. PR hacia develop

# ⭐ 6. Reglas estrictas

- **Nunca** hacer commit directo en `main`

- **Nunca** mezclar varias features en una sola rama

- **Siempre** usar PR

- **Siempre** incluir tests

- **Siempre** actualizar documentación

- **Siempre** usar nombres claros

# ⭐ 7. Convenciones de nombres

| **Tipo** | **Formato** | **Ejemplo** |
| :-: | :-: | :-: |
| **feature** | `feature/\<nombre\>` | `feature/ui\_offsets\_panel` |
| **hotfix** | `hotfix/\<nombre\>` | `hotfix/servo\_timeout` |
| **release** | `release/vX.Y.Z` | `release/v1.2.0` |
| **develop** | `develop` | — |
| **main** | `main` | — |

# ⭐ 8. Integración continua (CI)

El modelo de ramas está diseñado para CI:

- `main` → build + release

- `develop` → build + tests

- `feature/\*` → tests

- `hotfix/\*` → build + tests

- `release/\*` → build + tests

# ⭐ 9. Objetivo final

Este modelo garantiza:

- orden

- estabilidad

- velocidad

- claridad

- profesionalismo

- control de versiones

- escalabilidad a largo plazo

Es el modelo oficial del ecosistema CNC‑CAT.


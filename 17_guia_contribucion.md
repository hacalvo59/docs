# 📘 **17\_guia\_contribucion.md**

**Guía oficial de contribución — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir cómo contribuir correctamente al ecosistema CNC‑CAT, garantizando:

- calidad

- consistencia

- orden

- profesionalismo

- seguridad

- mantenibilidad

Esta guía es obligatoria para cualquier colaborador interno o externo.

# ⭐ 2. Requisitos previos

Antes de contribuir, el desarrollador debe:

- conocer la arquitectura CNC‑CAT

- leer la Motion API

- entender el ciclo de control

- conocer los estándares de código

- conocer el modelo de ramas

- conocer el estándar de commits

- conocer los estándares de documentación

# ⭐ 3. Flujo de contribución

Código

```
`1. Crear issue`

`2. Crear rama feature`

`3. Implementar`

`4. Añadir tests`

`5. Actualizar documentación`

`6. Crear Pull Request`

`7. Revisión`

`8. Merge a develop`
```

# ⭐ 4. Crear un issue

Todo cambio debe comenzar con un issue que incluya:

- descripción clara

- motivación

- impacto

- módulos afectados

- criterios de aceptación

Ejemplo:

Código

```
`\[Planner\] Añadir soporte para G38.x`
```

# ⭐ 5. Crear una rama feature

Formato:

Código

```
`feature/\<nombre\_claro\>`
```

Ejemplos:

- `feature/planner\_arc\_support`

- `feature/ui\_offsets\_panel`

- `feature/ethercat\_watchdog`

# ⭐ 6. Implementación

Reglas:

- seguir convenciones de código

- seguir estándares de documentación

- no romper compatibilidad

- no introducir dependencias innecesarias

- no mezclar varias features en una sola rama

# ⭐ 7. Tests obligatorios

Cada contribución debe incluir:

- tests unitarios

- tests de integración (si aplica)

- tests de regresión (si aplica)

Ejemplo:

bash

```
`pytest`
```

# ⭐ 8. Documentación obligatoria

Cada contribución debe actualizar:

- documentación técnica

- documentación de usuario (si aplica)

- changelog

- comentarios en código

- diagramas (si aplica)

# ⭐ 9. Pull Request

Un PR debe incluir:

- descripción clara

- motivación

- cambios realizados

- capturas (si aplica)

- pruebas realizadas

- checklist de estándares

Ejemplo de checklist:

Código

```
`\[ \] Código formateado`

`\[ \] Tests incluidos`

`\[ \] Documentación actualizada`

`\[ \] Changelog actualizado`

`\[ \] Cumple estándares CNC‑CAT`
```

# ⭐ 10. Revisión de código

Reglas:

- respetuosa

- técnica

- objetiva

- basada en estándares

- sin opiniones personales

El revisor puede solicitar:

- cambios

- mejoras

- aclaraciones

- reestructuración

# ⭐ 11. Merge

Reglas:

- nunca hacer merge directo a main

- siempre mediante PR

- siempre squash merge para features

- siempre actualizar develop

# ⭐ 12. Contribuciones no aceptadas

No se aceptan:

- código sin tests

- código sin documentación

- cambios masivos sin justificación

- código no tipado

- código que rompa el ciclo de control

- código que mezcle UI + hardware

- código que ignore estándares

# ⭐ 13. Código de conducta

Los colaboradores deben:

- ser respetuosos

- ser profesionales

- evitar discusiones personales

- centrarse en el proyecto

- colaborar de forma constructiva

# ⭐ 14. Objetivo final

Esta guía garantiza que CNC‑CAT crezca:

- ordenado

- estable

- profesional

- escalable

- mantenible

Es la guía oficial de contribución del ecosistema.


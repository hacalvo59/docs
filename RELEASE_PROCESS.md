# 📘 **RELEASE\_PROCESS.md**

**Proceso oficial de publicación de versiones del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Este documento define el proceso **industrial, seguro y reproducible** para publicar nuevas versiones del ecosistema:

- UI LINCAT

- CNC‑CAT Core

- Motion API

- Motores (sim/real)

- EtherCAT Layer

- PLC integrado

- Documentación

- Drivers

El objetivo es garantizar que cada release sea **estable, probada y profesional**.

# ⭐ 2. Tipos de versiones

El ecosistema sigue **Semantic Versioning (SemVer)**:

Código

```
`MAJOR.MINOR.PATCH`
```

## **2.1 MAJOR**

Cambios incompatibles, reestructuración profunda.

## **2.2 MINOR**

Nuevas funcionalidades sin romper compatibilidad.

## **2.3 PATCH**

Correcciones, mejoras menores, documentación.

# ⭐ 3. Flujo general de release

Código

```
`1. Preparación`

`2. Congelación`

`3. Pruebas`

`4. Validación`

`5. Generación`

`6. Publicación`

`7. Documentación`

`8. Anuncio`
```

# ⭐ 4. Fase 1 — Preparación

## **4.1 Revisar issues**

- bugs abiertos

- mejoras pendientes

- tareas críticas

## **4.2 Revisar PRs**

- PRs sin revisar

- PRs bloqueados

- PRs incompletos

## **4.3 Revisar dependencias**

bash

```
`pip list --outdated`
```

# ⭐ 5. Fase 2 — Congelación

## **5.1 Crear rama de release**

bash

```
`git checkout -b release/vX.Y.Z`
```

## **5.2 Bloquear nuevas funcionalidades**

Solo se permiten:

- fixes

- documentación

- ajustes menores

# ⭐ 6. Fase 3 — Pruebas

## **6.1 Unit tests**

bash

```
`pytest`
```

## **6.2 Integration tests**

- Motion API

- Planner

- Interpolador

- PLC

## **6.3 HIL tests**

- servos

- homing

- límites

- EtherCAT

## **6.4 E2E tests**

- UI → Motor → EtherCAT → Hardware

# ⭐ 7. Fase 4 — Validación

## **7.1 Validación técnica**

- rendimiento

- jitter

- estabilidad

- seguridad

## **7.2 Validación de documentación**

bash

```
`mkdocs build`
```

## **7.3 Validación de configuración**

bash

```
`python3 validate\_config.py`
```

# ⭐ 8. Fase 5 — Generación de artefactos

## **8.1 Generar paquete**

bash

```
`python3 setup.py sdist bdist\_wheel`
```

## **8.2 Generar documentación PDF**

bash

```
`pandoc pdf\_master.md -o lincat\_cnc-cat\_documentacion.pdf`
```

## **8.3 Generar binarios (si aplica)**

- UI empaquetada

- scripts de instalación

# ⭐ 9. Fase 6 — Publicación

## **9.1 Merge a main**

bash

```
`git checkout main`

`git merge --no-ff release/vX.Y.Z`
```

## **9.2 Crear tag**

bash

```
`git tag -a vX.Y.Z -m "Release vX.Y.Z"`

`git push origin vX.Y.Z`
```

## **9.3 Publicar artefactos**

- GitHub Releases

- documentación actualizada

- binarios (si aplica)

# ⭐ 10. Fase 7 — Documentación

## **10.1 Actualizar CHANGELOG.md**

- nuevas funciones

- fixes

- breaking changes

## **10.2 Actualizar versión en código**

- `\_\_version\_\_`

- documentación

- UI LINCAT

# ⭐ 11. Fase 8 — Anuncio

## **11.1 Canales**

- GitHub

- documentación

- notas de release

## **11.2 Contenido**

- resumen

- mejoras

- fixes

- instrucciones de actualización

# ⭐ 12. Objetivo final

Garantizar que cada release del ecosistema LINCAT / CNC‑CAT sea:

- estable

- segura

- probada

- documentada

- reproducible

- profesional

- industrial


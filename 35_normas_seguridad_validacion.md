# ⭐ **35\_normas\_seguridad\_validacion.md**

Aquí tienes el siguiente archivo, **completo**, **industrial**, **coherente**, listo para guardar en:

Código

```
`C\_Pilot\_Docs/35\_normas\_seguridad\_validacion.md`
```

# 📘 **35\_normas\_seguridad\_validacion.md**

**Normas oficiales de seguridad en validación — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad obligatorias** para realizar validaciones en máquinas controladas por CNC‑CAT, garantizando:

- precisión

- estabilidad

- seguridad del operador

- seguridad del hardware

- cumplimiento industrial

- trazabilidad

Estas normas son **críticas** y deben cumplirse SIEMPRE.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 Validar es confirmar que el sistema es seguro

No es una prueba superficial: es una certificación interna.

### ✔️ 2.2 La validación debe ser objetiva

Basada en datos, no en percepciones.

### ✔️ 2.3 La validación debe ser repetible

Dos técnicos distintos deben obtener el mismo resultado.

### ✔️ 2.4 La validación debe ser documentada

Sin registro → no existe.

# ⭐ 3. Tipos de validación cubiertos

### ✔️ 3.1 Validación mecánica

- backlash

- escuadra

- paralelismo

- precisión de posicionamiento

### ✔️ 3.2 Validación eléctrica

- drivers

- servos

- sensores

- alimentación

### ✔️ 3.3 Validación de seguridad

- E‑STOP

- límites

- watchdog

- alarmas

### ✔️ 3.4 Validación de software

- Motion API

- UI LINCAT

- CORE

- simulación

### ✔️ 3.5 Validación de integración

- EtherCAT

- PLC

- robots

- módulos externos

# ⭐ 4. Requisitos previos

Antes de validar, el técnico debe:

- ser usuario con rol **técnico** o **administrador**

- revisar estado de la máquina

- verificar ausencia de alarmas

- verificar integridad mecánica

- verificar integridad eléctrica

- preparar herramientas de medición certificadas

- preparar entorno seguro

# ⭐ 5. Equipo de protección personal (EPP)

Obligatorio:

- gafas de seguridad

- calzado de seguridad

- ropa ajustada

Opcional según validación:

- protección auditiva

- guantes

# ⭐ 6. Seguridad en validación mecánica

### ✔️ 6.1 Prohibido validar con la máquina activa

Excepto cuando el procedimiento lo requiera.

### ✔️ 6.2 Prohibido acercar manos a partes móviles

Incluso en jog lento.

### ✔️ 6.3 Prohibido validar con herramientas de medición dañadas

Debe usarse equipo certificado.

### ✔️ 6.4 Validación obligatoria

- backlash

- escuadra

- paralelismo

- precisión

# ⭐ 7. Seguridad en validación eléctrica

### ✔️ 7.1 Prohibido validar con tensión aplicada

Excepto cuando el fabricante lo permita.

### ✔️ 7.2 Prohibido validar drivers sin documentación

Nada de ajustes improvisados.

### ✔️ 7.3 Validación obligatoria

- servos

- encoders

- frenos

- watchdog

# ⭐ 8. Seguridad en validación de seguridad

### ✔️ 8.1 Validar E‑STOP

Debe detener la máquina inmediatamente.

### ✔️ 8.2 Validar límites

Nunca permitir límites defectuosos.

### ✔️ 8.3 Validar watchdog

Debe activarse ante fallos de comunicación.

### ✔️ 8.4 Validar alarmas

Todas deben dispararse correctamente.

# ⭐ 9. Seguridad en validación de software

### ✔️ 9.1 Prohibido validar software sin pruebas unitarias

Debe existir cobertura mínima.

### ✔️ 9.2 Prohibido validar software sin simulación previa

Primero en entorno seguro.

### ✔️ 9.3 Validación obligatoria

- homing

- jog

- límites

- alarmas

- trayectorias

# ⭐ 10. Seguridad en validación de integración

### ✔️ 10.1 Prohibido validar integración sin documentación

Debe existir esquema eléctrico y de comunicación.

### ✔️ 10.2 Prohibido validar integración sin sandbox

Primero en entorno aislado.

### ✔️ 10.3 Validación obligatoria

- comunicación

- latencia

- sincronización

- seguridad

# ⭐ 11. Procedimiento seguro de validación

### ✔️ 11.1 Preparación

- revisar máquina

- revisar entorno

- revisar sensores

- revisar servos

- revisar documentación

### ✔️ 11.2 Ejecución

- pasos claros

- movimientos lentos

- supervisión constante

### ✔️ 11.3 Validación

- homing

- jog

- límites

- precisión

### ✔️ 11.4 Registro

Debe incluir:

- técnico

- fecha

- valores validados

- herramientas usadas

- incidencias

# ⭐ 12. Prohibiciones absolutas

- validar sin permisos

- validar sin EPP

- validar sin documentación

- validar sin simulación previa

- validar sin registrar

- validar desactivando límites

- validar servos sin encoder

- validar con sensores defectuosos

- validar con herramientas no certificadas

# ⭐ 13. Objetivo final

Estas normas garantizan que la validación CNC‑CAT sea:

- segura

- precisa

- profesional

- industrial

- trazable

- confiable

Son las normas oficiales de seguridad en validación del ecosistema CNC‑CAT.


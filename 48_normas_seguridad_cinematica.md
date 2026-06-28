# 📘 **48\_normas\_seguridad\_cinematica.md**

**Normas oficiales de seguridad cinemática — CNC‑CAT / LINCAT**

## ⭐ 1. Propósito

Definir las **normas de seguridad cinemática** para todos los sistemas de movimiento del ecosistema CNC‑CAT, garantizando:

- integridad del operador

- integridad de la máquina

- precisión del movimiento

- estabilidad dinámica

- cumplimiento industrial

La cinemática es la ciencia del movimiento. Si falla, la máquina falla. Estas normas son **críticas** y deben cumplirse SIEMPRE.

## ⭐ 2. Principios fundamentales

- **La cinemática define el movimiento** — sin cinemática correcta, no hay precisión.

- **La sincronización es seguridad** — desincronización = colisiones.

- **La aceleración debe ser controlada** — jerk excesivo = vibración.

- **La calibración es obligatoria** — sin calibración, no hay repetibilidad.

## ⭐ 3. Sistemas cinemáticos cubiertos

- **Cinemática cartesiana** (X‑Y‑Z)

- **Cinemática rotativa** (A‑B‑C)

- **Cinemática híbrida**

- **Cinemática multieje**

- **Cinemática 5 ejes simultáneos**

## ⭐ 4. Requisitos previos

Antes de intervenir cinemáticamente:

- **Revisar parámetros de ejes**

- **Revisar aceleraciones**

- **Revisar jerk**

- **Revisar límites**

- **Revisar homing**

## ⭐ 5. Seguridad en cinemática cartesiana

- **Prohibido operar con ejes desalineados**

- **Prohibido operar con backlash excesivo**

- **Prohibido operar sin homing preciso**

- Validación obligatoria:

  - paralelismo

  - perpendicularidad

  - repetibilidad

## ⭐ 6. Seguridad en cinemática rotativa

- **Prohibido operar sin compensación angular**

- **Prohibido operar con holgura en platos o mesas**

- **Prohibido operar sin límites rotativos**

- Validación obligatoria:

  - precisión angular

  - repetibilidad

  - backlash rotativo

## ⭐ 7. Seguridad en cinemática híbrida

- **Prohibido mezclar sistemas sin calibración cruzada**

- **Prohibido operar sin compensación de transformaciones**

- Validación obligatoria:

  - matrices de transformación

  - offsets

  - sincronización

## ⭐ 8. Seguridad en cinemática multieje

- **Prohibido operar sin sincronización de ejes**

- **Prohibido operar sin límites activos**

- **Prohibido operar sin simulación previa**

- Validación obligatoria:

  - trayectoria

  - colisiones

  - interpolación

## ⭐ 9. Seguridad en cinemática 5 ejes simultáneos

- **Prohibido operar sin modelo cinemático completo**

- **Prohibido operar sin compensación TCP**

- **Prohibido operar sin simulación 3D**

- Validación obligatoria:

  - orientación

  - trayectoria

  - colisiones

  - sincronización

## ⭐ 10. Prohibiciones absolutas

- operar con ejes desalineados

- operar sin homing

- operar sin límites

- operar sin compensaciones

- operar sin simulación

- operar con backlash excesivo

- operar con vibración

- ignorar ruido

- ignorar temperatura

- ignorar alarmas

- operar sin validar

- operar sin registrar

## ⭐ 11. Objetivo final

Estas normas garantizan que la cinemática CNC‑CAT sea:

- segura

- precisa

- estable

- profesional

- industrial

- trazable

- confiable

Son las normas oficiales de seguridad cinemática del ecosistema CNC‑CAT.


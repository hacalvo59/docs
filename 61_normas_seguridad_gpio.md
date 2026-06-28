# 📘 **61\_normas\_seguridad\_gpio.md**

**Normas oficiales de seguridad para GPIO — CNC‑CAT / LINCAT**

## ⭐ 1. Propósito

Definir las **normas de seguridad para el uso de GPIO (General‑Purpose Input/Output)** dentro del ecosistema CNC‑CAT, garantizando:

- seguridad del operador

- integridad eléctrica

- integridad de sensores y actuadores

- estabilidad del sistema

- cumplimiento industrial

Los GPIO son la puerta de entrada al mundo físico. Si fallan, la máquina falla. Estas normas son **críticas** y deben cumplirse SIEMPRE.

## ⭐ 2. Principios fundamentales

- **Los GPIO no son juguetes** — pueden quemarse o causar fallos graves.

- **La tensión debe ser correcta** — 24V industriales ≠ 3.3V lógicos.

- **La protección es obligatoria** — optoacopladores, fusibles, TVS.

- **La tierra debe ser común** — evita ruido y fallos.

## ⭐ 3. Componentes GPIO cubiertos

- **Entradas digitales**

- **Salidas digitales**

- **Sensores**

- **Relés**

- **Botones y E‑STOP**

- **Optoacopladores**

- **Aislamiento galvánico**

## ⭐ 4. Requisitos previos

Antes de usar GPIO:

- **Revisar tensiones**

- **Revisar polaridad**

- **Revisar tierra**

- **Revisar aislamiento**

- **Revisar documentación del sensor**

## ⭐ 5. Seguridad en entradas digitales

- **Prohibido conectar sensores sin conocer su tipo**

- **Prohibido mezclar PNP y NPN sin adaptación**

- **Prohibido usar entradas sin protección**

- Validación obligatoria:

  - nivel lógico

  - ruido

  - estabilidad

## ⭐ 6. Seguridad en salidas digitales

- **Prohibido conectar cargas sin conocer su consumo**

- **Prohibido usar salidas sin protección de sobrecorriente**

- **Prohibido usar salidas sin diodos flyback**

- Validación obligatoria:

  - corriente

  - temperatura

  - ruido

## ⭐ 7. Seguridad en sensores

- **Prohibido usar sensores sin documentación**

- **Prohibido usar sensores sin blindaje**

- **Prohibido usar sensores sin tierra común**

- Validación obligatoria:

  - señal

  - estabilidad

  - repetibilidad

## ⭐ 8. Seguridad en relés

- **Prohibido usar relés sin diodo flyback**

- **Prohibido usar relés sin aislamiento**

- **Prohibido usar relés con cargas inductivas sin protección**

- Validación obligatoria:

  - continuidad

  - ruido

  - temperatura

## ⭐ 9. Seguridad en botones y E‑STOP

- **Prohibido usar E‑STOP sin doble canal**

- **Prohibido usar botones sin enclavamiento**

- **Prohibido usar cableado sin certificación**

- Validación obligatoria:

  - continuidad

  - redundancia

  - respuesta

## ⭐ 10. Seguridad en aislamiento y protección

- **Prohibido usar GPIO sin optoacopladores**

- **Prohibido usar GPIO sin fusibles**

- **Prohibido usar GPIO sin TVS**

- Validación obligatoria:

  - aislamiento

  - ruido

  - estabilidad

## ⭐ 11. Prohibiciones absolutas

- mezclar PNP y NPN sin adaptación

- usar sensores sin documentación

- usar salidas sin protección

- usar relés sin flyback

- usar GPIO sin aislamiento

- ignorar ruido eléctrico

- ignorar temperatura

- ignorar olor a quemado

- operar sin validar

- operar sin registrar

## ⭐ 12. Objetivo final

Estas normas garantizan que los GPIO en CNC‑CAT sean:

- seguros

- estables

- precisos

- profesionales

- industriales

- trazables

- confiables

Son las normas oficiales de seguridad GPIO del ecosistema CNC‑CAT.


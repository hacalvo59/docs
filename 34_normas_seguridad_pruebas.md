# 📘 **34\_normas\_seguridad\_pruebas.md**

**Normas oficiales de seguridad en pruebas — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad obligatorias** para realizar pruebas en máquinas controladas por CNC‑CAT, garantizando:

- protección del operador

- protección del hardware

- protección del entorno

- estabilidad del sistema

- cumplimiento industrial

- reducción de riesgos durante validaciones

Estas normas son **críticas** y deben cumplirse SIEMPRE.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 Toda prueba implica riesgo

Incluso las pruebas simples pueden causar daños si se ejecutan incorrectamente.

### ✔️ 2.2 La seguridad está por encima de la validación

Si una prueba compromete la seguridad → se detiene.

### ✔️ 2.3 Las pruebas deben ser controladas

Nada de improvisaciones.

### ✔️ 2.4 Las pruebas deben ser reproducibles

Debe existir un procedimiento claro.

# ⭐ 3. Tipos de pruebas cubiertas

### ✔️ 3.1 Pruebas de software

- UI

- Motion API

- CORE

- simulación

### ✔️ 3.2 Pruebas de hardware

- servos

- drivers

- sensores

- husillo

- sondas

### ✔️ 3.3 Pruebas de integración

- EtherCAT

- PLC

- robots

- módulos externos

### ✔️ 3.4 Pruebas de seguridad

- E‑STOP

- límites

- watchdog

- alarmas

### ✔️ 3.5 Pruebas de G‑code

- movimientos simples

- movimientos complejos

- trayectorias largas

# ⭐ 4. Requisitos previos

Antes de realizar cualquier prueba, el técnico debe:

- ser usuario con rol **técnico** o **administrador**

- revisar estado de la máquina

- verificar ausencia de alarmas

- verificar integridad mecánica

- verificar integridad eléctrica

- verificar integridad de sensores

- preparar entorno seguro

- activar EPP obligatorio

# ⭐ 5. Equipo de protección personal (EPP)

Obligatorio:

- gafas de seguridad

- calzado de seguridad

- ropa ajustada

- pelo recogido

Opcional según prueba:

- protección auditiva

- guantes

# ⭐ 6. Seguridad en pruebas de software

### ✔️ 6.1 Prohibido probar software en máquina real sin validación previa

Primero en simulación.

### ✔️ 6.2 Prohibido modificar Motion API sin pruebas unitarias

Debe existir cobertura mínima.

### ✔️ 6.3 Prohibido probar UI sin motor conectado

Evita estados inconsistentes.

### ✔️ 6.4 Validación obligatoria

Después de cada cambio:

- homing

- jog

- límites

- alarmas

# ⭐ 7. Seguridad en pruebas de hardware

### ✔️ 7.1 Prohibido probar hardware sin documentación

Nada de “a ver qué pasa”.

### ✔️ 7.2 Prohibido probar hardware sin apagar la máquina

Excepto módulos hot‑swap certificados.

### ✔️ 7.3 Prohibido probar servos sin fijación mecánica

Evita movimientos bruscos.

### ✔️ 7.4 Validación obligatoria

Después de cada prueba:

- encoder

- watchdog

- límites

- sensores

# ⭐ 8. Seguridad en pruebas de movimiento

### ✔️ 8.1 Velocidad reducida

Todas las pruebas deben comenzar a baja velocidad.

### ✔️ 8.2 Movimientos cortos

Nunca iniciar pruebas con desplazamientos largos.

### ✔️ 8.3 Prohibido acercar manos a partes móviles

Incluso en jog lento.

### ✔️ 8.4 Validación obligatoria

Después de cada prueba:

- DRO

- precisión

- repetibilidad

# ⭐ 9. Seguridad en pruebas de G‑code

### ✔️ 9.1 Simulación obligatoria

Antes de ejecutar en máquina real.

### ✔️ 9.2 Prohibido ejecutar G‑code desconocido

Debe ser revisado.

### ✔️ 9.3 Prohibido ejecutar G‑code sin herramienta adecuada

Evita colisiones.

### ✔️ 9.4 Validación obligatoria

Después de cada prueba:

- offsets

- herramienta

- trayectoria

- colisiones

# ⭐ 10. Seguridad en pruebas de integración

### ✔️ 10.1 Prohibido integrar sin pruebas unitarias

Cada módulo debe validarse por separado.

### ✔️ 10.2 Prohibido integrar sin sandbox

Primero en entorno aislado.

### ✔️ 10.3 Prohibido integrar sin documentación

Debe existir esquema eléctrico y de comunicación.

### ✔️ 10.4 Validación obligatoria

Después de integrar:

- comunicación

- latencia

- sincronización

- seguridad

# ⭐ 11. Procedimiento seguro de pruebas

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

- tipo de prueba

- resultados

- incidencias

# ⭐ 12. Prohibiciones absolutas

- probar sin permisos

- probar sin EPP

- probar sin documentación

- probar sin simulación previa

- probar con la máquina activa (si no corresponde)

- probar sin validar

- probar sin registrar

- probar desactivando límites

- probar servos sin encoder

- probar G‑code desconocido

# ⭐ 13. Objetivo final

Estas normas garantizan que las pruebas CNC‑CAT sean:

- seguras

- controladas

- profesionales

- industriales

- trazables

- confiables

Son las normas oficiales de seguridad en pruebas del ecosistema CNC‑CAT.


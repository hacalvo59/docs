# 📘 **31\_normas\_seguridad\_actualizaciones.md**

**Normas oficiales de seguridad en actualizaciones — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad obligatorias** para realizar actualizaciones de software, firmware, configuraciones y documentación dentro del ecosistema CNC‑CAT, garantizando:

- integridad del sistema

- continuidad operativa

- protección del hardware

- trazabilidad

- cumplimiento industrial

- prevención de fallos críticos

Estas normas son **estrictas** y deben cumplirse SIEMPRE.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 Nunca actualizar durante operación

La máquina debe estar completamente detenida.

### ✔️ 2.2 Nunca actualizar sin respaldo

Backup obligatorio antes de cualquier cambio.

### ✔️ 2.3 Nunca actualizar desde internet

Solo fuentes verificadas y controladas.

### ✔️ 2.4 Las actualizaciones deben ser reversibles

Debe existir un plan de rollback.

# ⭐ 3. Tipos de actualizaciones cubiertas

### ✔️ 3.1 Software CNC‑CAT

- motor simulado

- motor real

- Motion API

- UI LINCAT

- drivers

- ciclo de control

### ✔️ 3.2 Firmware

- servos

- drivers EtherCAT

- sensores inteligentes

- husillo

### ✔️ 3.3 Configuraciones

- offsets

- herramientas

- parámetros

- límites

- red

- EtherCAT

### ✔️ 3.4 Documentación

- técnica

- operativa

- de seguridad

# ⭐ 4. Requisitos previos

Antes de actualizar, el técnico debe:

- ser usuario con rol **administrador**

- verificar estado de la máquina

- verificar ausencia de alarmas

- verificar integridad del sistema

- realizar backup completo

- revisar notas de versión

- verificar compatibilidad

# ⭐ 5. Procedimiento seguro de actualización

### ✔️ 5.1 Detener la máquina

Incluye:

- husillo

- servos

- drivers

- ciclo de control

### ✔️ 5.2 Activar LOTO si aplica

Bloqueo y etiquetado en entornos industriales.

### ✔️ 5.3 Realizar backup

Debe incluir:

- configuraciones

- offsets

- herramientas

- parámetros

- logs

- firmware actual

### ✔️ 5.4 Verificar integridad del paquete

Checksum obligatorio.

### ✔️ 5.5 Instalar actualización

Sin interrupciones.

### ✔️ 5.6 Reiniciar sistema

Completo:

- UI

- motor

- drivers

- EtherCAT

### ✔️ 5.7 Validar funcionamiento

Incluye:

- homing

- límites

- sensores

- servos

- husillo

- ejecución de G‑code simple

# ⭐ 6. Seguridad en actualizaciones de firmware

### ✔️ 6.1 Prohibido actualizar firmware con la máquina energizada

Excepto cuando el fabricante lo permita explícitamente.

### ✔️ 6.2 Prohibido actualizar firmware sin UPS

Evita fallos por corte eléctrico.

### ✔️ 6.3 Prohibido mezclar versiones incompatibles

Drivers y servos deben ser compatibles.

### ✔️ 6.4 Verificación posterior

- encoder

- watchdog

- límites

- homing

# ⭐ 7. Seguridad en actualizaciones de configuraciones

### ✔️ 7.1 Solo administradores pueden modificar configuraciones críticas

Incluye:

- límites

- parámetros del planner

- parámetros de servos

- configuración EtherCAT

- configuración de red

### ✔️ 7.2 Validación obligatoria

Después de cualquier cambio:

- homing

- test de jog

- test de límites

- test de sensores

# ⭐ 8. Seguridad en actualizaciones de documentación

### ✔️ 8.1 Control de versiones obligatorio

Git.

### ✔️ 8.2 Prohibido eliminar historial

Debe mantenerse trazabilidad.

### ✔️ 8.3 Revisión técnica obligatoria

Antes de publicar.

### ✔️ 8.4 Documentación crítica debe permanecer privada

# ⭐ 9. Prohibiciones absolutas

- actualizar durante operación

- actualizar sin backup

- actualizar desde internet

- actualizar sin verificar integridad

- actualizar sin permisos

- actualizar firmware sin UPS

- ignorar incompatibilidades

- reiniciar sin validar

- mezclar versiones no certificadas

- modificar configuraciones sin autorización

# ⭐ 10. Objetivo final

Estas normas garantizan que las actualizaciones CNC‑CAT sean:

- seguras

- controladas

- trazables

- reversibles

- profesionales

- industriales

Son las normas oficiales de seguridad en actualizaciones del ecosistema CNC‑CAT.


# 📘 **23\_normas\_seguridad\_datos.md**

**Normas oficiales de seguridad de datos — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad de datos** que deben cumplirse en cualquier instalación de CNC‑CAT, garantizando:

- integridad de la información

- protección de datos sensibles

- prevención de pérdidas

- cumplimiento industrial

- trazabilidad

- auditoría

Estas normas son **obligatorias** en entornos profesionales.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 Los datos son parte crítica del sistema

Sin datos fiables → no hay operación segura.

### ✔️ 2.2 La integridad es prioritaria

Los datos nunca deben corromperse.

### ✔️ 2.3 La trazabilidad es obligatoria

Cada acción debe poder auditarse.

### ✔️ 2.4 Los datos deben estar protegidos

Nada de accesos abiertos o sin control.

# ⭐ 3. Tipos de datos protegidos

### ✔️ 3.1 Datos de máquina

- offsets

- herramientas

- parámetros

- límites

- configuraciones

### ✔️ 3.2 Datos de operación

- G‑code

- historial de alarmas

- historial de estados

- logs de operación

### ✔️ 3.3 Datos de usuario

- perfiles

- permisos

- acciones realizadas

### ✔️ 3.4 Datos de hardware

- calibraciones

- diagnósticos

- estados de servos

# ⭐ 4. Seguridad en almacenamiento

### ✔️ 4.1 Archivos críticos deben ser inmutables

Ejemplo:

- offsets

- herramientas

- parámetros

### ✔️ 4.2 Copias de seguridad automáticas

Frecuencia recomendada:

- diaria para datos de operación

- semanal para datos de máquina

### ✔️ 4.3 Verificación de integridad

Checksum obligatorio.

### ✔️ 4.4 Prohibido almacenar datos en ubicaciones no controladas

Nada de:

- carpetas temporales

- unidades externas sin control

- ubicaciones compartidas inseguras

# ⭐ 5. Seguridad en acceso

### ✔️ 5.1 Control de permisos

Tres niveles recomendados:

- operador

- técnico

- administrador

### ✔️ 5.2 Acceso restringido a datos críticos

Solo administradores pueden modificar:

- offsets

- herramientas

- parámetros

- configuraciones

### ✔️ 5.3 Autenticación obligatoria

Nada de acceso sin usuario.

### ✔️ 5.4 Sesiones con tiempo de expiración

Evita accesos no supervisados.

# ⭐ 6. Seguridad en transmisión

### ✔️ 6.1 Prohibido enviar datos por red sin cifrado

Especialmente:

- G‑code

- configuraciones

- logs

### ✔️ 6.2 Prohibido compartir carpetas por red

Nada de Samba, FTP o similares.

### ✔️ 6.3 Prohibido exponer datos a internet

Nunca.

# ⭐ 7. Seguridad en logs

### ✔️ 7.1 Logs deben ser inmutables

No se editan.

### ✔️ 7.2 Logs deben tener sello de tiempo

Formato ISO‑8601.

### ✔️ 7.3 Logs no deben contener datos sensibles

Ejemplo:

❌ contraseñas ❌ tokens ❌ claves

### ✔️ 7.4 Logs deben rotarse

Evita saturación del disco.

# ⭐ 8. Seguridad en backups

### ✔️ 8.1 Backups cifrados

Nunca en texto plano.

### ✔️ 8.2 Backups verificados

Comprobar integridad.

### ✔️ 8.3 Backups fuera de la máquina

Pero en entorno seguro.

### ✔️ 8.4 Backups automáticos

Sin intervención humana.

# ⭐ 9. Seguridad en restauración

### ✔️ 9.1 Restaurar solo desde fuentes confiables

Nunca desde archivos desconocidos.

### ✔️ 9.2 Validar integridad antes de restaurar

Checksum obligatorio.

### ✔️ 9.3 Registrar toda restauración

Auditoría completa.

# ⭐ 10. Auditoría

### ✔️ 10.1 Registrar acciones críticas

- cambios de parámetros

- cambios de offsets

- cambios de herramientas

- cambios de configuraciones

### ✔️ 10.2 Registrar accesos

- usuario

- hora

- acción

- resultado

### ✔️ 10.3 Registrar fallos

Todo error debe quedar registrado.

# ⭐ 11. Prohibiciones absolutas

- almacenar datos sin cifrado

- exponer datos a internet

- compartir carpetas por red

- usar USB desconocidos

- modificar logs

- eliminar logs críticos

- ignorar fallos de integridad

- permitir acceso sin autenticación

# ⭐ 12. Objetivo final

Estas normas garantizan que los datos CNC‑CAT sean:

- seguros

- íntegros

- auditables

- confiables

- industriales

- profesionales

Son las normas oficiales de seguridad de datos del ecosistema CNC‑CAT.


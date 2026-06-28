# 📘 **24\_normas\_seguridad\_usuarios.md**

**Normas oficiales de seguridad para usuarios — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad relacionadas con usuarios, permisos y roles** dentro del ecosistema CNC‑CAT, garantizando:

- control de acceso

- trazabilidad

- protección del sistema

- prevención de acciones no autorizadas

- cumplimiento industrial

Estas normas son **obligatorias** en cualquier instalación profesional.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 No todos los usuarios son iguales

Cada rol tiene permisos específicos.

### ✔️ 2.2 El sistema debe saber quién hace qué

Trazabilidad completa.

### ✔️ 2.3 Ningún usuario debe tener más permisos de los necesarios

Principio de **mínimo privilegio**.

### ✔️ 2.4 Las acciones críticas requieren permisos elevados

Nada de operadores cambiando parámetros peligrosos.

# ⭐ 3. Roles oficiales del sistema

El ecosistema CNC‑CAT define **tres niveles de usuario**:

## **3.1 Operador**

Permisos:

- ejecutar G‑code

- usar jog

- hacer homing

- cargar programas

- ver alarmas

- detener la máquina

Prohibido:

- cambiar offsets

- cambiar herramientas

- modificar parámetros

- acceder a configuraciones internas

- modificar límites

## **3.2 Técnico**

Permisos:

- todo lo del operador

- modificar offsets

- modificar herramientas

- calibrar ejes

- configurar drivers

- revisar logs

- ejecutar diagnósticos

Prohibido:

- modificar parámetros críticos del sistema

- cambiar configuraciones de red

- modificar Motion API

- deshabilitar límites

## **3.3 Administrador**

Permisos:

- todo lo del técnico

- modificar parámetros críticos

- configurar red

- gestionar usuarios

- gestionar backups

- restaurar configuraciones

- actualizar el sistema

Prohibido:

- operar la máquina sin EPP

- ignorar normas de seguridad

# ⭐ 4. Autenticación

### ✔️ 4.1 Inicio de sesión obligatorio

Nadie puede usar la máquina sin identificarse.

### ✔️ 4.2 Contraseñas seguras

Requisitos:

- mínimo 10 caracteres

- mezcla de letras, números y símbolos

- sin palabras comunes

### ✔️ 4.3 Expiración de sesión

Si el usuario se ausenta → cierre automático.

### ✔️ 4.4 Prohibido compartir cuentas

Cada persona debe tener su propio usuario.

# ⭐ 5. Autorización

### ✔️ 5.1 Acciones críticas requieren permisos elevados

Ejemplos:

- cambiar offsets

- cambiar herramientas

- modificar parámetros

- desactivar límites

- ejecutar diagnósticos avanzados

### ✔️ 5.2 Confirmación obligatoria

Acciones peligrosas requieren:

- confirmación en UI

- registro en logs

# ⭐ 6. Auditoría

### ✔️ 6.1 Registrar todas las acciones críticas

Incluyendo:

- cambios de offsets

- cambios de herramientas

- cambios de parámetros

- ejecución de diagnósticos

- restauración de backups

### ✔️ 6.2 Registrar accesos

- usuario

- hora

- acción

- resultado

### ✔️ 6.3 Logs inmutables

No se editan ni eliminan.

# ⭐ 7. Seguridad en la UI LINCAT

### ✔️ 7.1 Paneles restringidos

Los paneles avanzados solo deben mostrarse a técnicos o administradores.

### ✔️ 7.2 Botones críticos protegidos

- RESET

- CLEAR ALARMS

- TOOL CHANGE

- PARAMS

### ✔️ 7.3 Indicadores siempre visibles

- usuario actual

- rol

- permisos activos

# ⭐ 8. Seguridad en la Motion API

### ✔️ 8.1 Validar permisos antes de ejecutar comandos

La UI no puede saltarse la seguridad.

### ✔️ 8.2 Prohibido ejecutar comandos sin usuario activo

### ✔️ 8.3 Registrar comandos críticos

# ⭐ 9. Seguridad en configuraciones

### ✔️ 9.1 Configuraciones críticas solo para administradores

Incluye:

- límites

- parámetros de servo

- parámetros de planner

- configuraciones de red

- configuraciones de EtherCAT

### ✔️ 9.2 Prohibido modificar configuraciones sin autenticación

# ⭐ 10. Prohibiciones absolutas

- operar sin usuario autenticado

- compartir cuentas

- usar contraseñas débiles

- permitir acceso a operadores a configuraciones críticas

- ignorar auditorías

- eliminar logs

- deshabilitar límites sin permisos

- ejecutar G‑code sin rol adecuado

# ⭐ 11. Objetivo final

Estas normas garantizan que el sistema CNC‑CAT sea:

- seguro

- controlado

- trazable

- profesional

- industrial

- confiable

Son las normas oficiales de seguridad para usuarios del ecosistema CNC‑CAT.


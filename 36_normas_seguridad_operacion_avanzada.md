# 📘 **36\_normas\_seguridad\_operacion\_avanzada.md**

**Normas oficiales de seguridad en operación avanzada — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad obligatorias** para realizar operaciones avanzadas en máquinas controladas por CNC‑CAT, garantizando:

- seguridad del operador

- seguridad del hardware

- estabilidad del sistema

- precisión en operaciones complejas

- cumplimiento industrial

Estas normas aplican a operaciones que exceden el uso básico del CNC.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 La operación avanzada aumenta el riesgo

Más complejidad → más posibilidades de fallo.

### ✔️ 2.2 La seguridad debe ser absoluta

Si una operación avanzada compromete la seguridad → se detiene.

### ✔️ 2.3 Solo personal cualificado puede ejecutar estas operaciones

Operadores sin formación → prohibido.

### ✔️ 2.4 Toda operación avanzada debe estar documentada

Sin procedimiento → no se ejecuta.

# ⭐ 3. Operaciones avanzadas cubiertas

### ✔️ 3.1 Probing (sonda)

- medición automática

- detección de superficies

- búsqueda de bordes

- calibración de herramientas

### ✔️ 3.2 Cambios automáticos de herramienta (ATC)

- carrusel

- brazo

- torreta

### ✔️ 3.3 Operaciones multieje

- 4 ejes

- 5 ejes

- rotativos

- simultáneos

### ✔️ 3.4 Operaciones de alta velocidad

- husillo \> 18.000 rpm

- feedrates elevados

- aceleraciones agresivas

### ✔️ 3.5 Operaciones con robot

- carga/descarga

- sincronización

- handshakes

### ✔️ 3.6 Operaciones con PLC externo

- automatización avanzada

- secuencias personalizadas

# ⭐ 4. Requisitos previos

Antes de ejecutar cualquier operación avanzada, el técnico debe:

- ser usuario con rol **técnico** o **administrador**

- revisar estado de la máquina

- verificar ausencia de alarmas

- verificar integridad mecánica

- verificar integridad eléctrica

- verificar integridad de sensores

- revisar documentación del procedimiento

- preparar entorno seguro

# ⭐ 5. Equipo de protección personal (EPP)

Obligatorio:

- gafas de seguridad

- calzado de seguridad

- ropa ajustada

Opcional según operación:

- protección auditiva

- guantes

- pantalla facial

# ⭐ 6. Seguridad en probing (sonda)

### ✔️ 6.1 Prohibido usar sonda dañada

Debe estar calibrada y certificada.

### ✔️ 6.2 Prohibido ejecutar probing sin simulación previa

Evita colisiones.

### ✔️ 6.3 Prohibido usar probing con offsets incorrectos

Riesgo de impacto.

### ✔️ 6.4 Validación obligatoria

Después de probing:

- Z0

- X0

- Y0

- perpendicularidad

- repetibilidad

# ⭐ 7. Seguridad en cambios automáticos de herramienta (ATC)

### ✔️ 7.1 Prohibido usar ATC sin calibración previa

El carrusel debe estar alineado.

### ✔️ 7.2 Prohibido usar ATC con herramientas sueltas

Riesgo de expulsión.

### ✔️ 7.3 Prohibido usar ATC con sensores defectuosos

Incluye:

- sensor de herramienta presente

- sensor de posición

- sensor de carrusel

### ✔️ 7.4 Validación obligatoria

Después de cada cambio:

- herramienta correcta

- longitud correcta

- diámetro correcto

# ⭐ 8. Seguridad en operaciones multieje

### ✔️ 8.1 Prohibido operar multieje sin simulación

Especialmente 5 ejes simultáneos.

### ✔️ 8.2 Prohibido operar multieje sin límites activos

Nunca desactivar límites.

### ✔️ 8.3 Prohibido operar multieje sin herramienta adecuada

Evita colisiones.

### ✔️ 8.4 Validación obligatoria

- cinemática

- offsets

- trayectoria

- colisiones

# ⭐ 9. Seguridad en operaciones de alta velocidad

### ✔️ 9.1 Prohibido operar con herramienta dañada

A alta velocidad → riesgo extremo.

### ✔️ 9.2 Prohibido operar sin balanceo

Herramientas desbalanceadas → vibración.

### ✔️ 9.3 Prohibido operar sin protección auditiva

Ruido elevado.

### ✔️ 9.4 Validación obligatoria

- vibración

- temperatura

- estabilidad

# ⭐ 10. Seguridad en operaciones con robot

### ✔️ 10.1 Zona de seguridad compartida

Debe estar definida y señalizada.

### ✔️ 10.2 Handshake obligatorio

Antes de:

- mover robot

- mover CNC

- intercambiar piezas

### ✔️ 10.3 Parada coordinada

Si uno entra en emergencia → ambos se detienen.

# ⭐ 11. Seguridad en operaciones con PLC externo

### ✔️ 11.1 Comunicación segura

El PLC nunca debe poder:

- mover ejes

- modificar parámetros

- desactivar límites

### ✔️ 11.2 Validación de señales

Cada señal debe:

- documentarse

- etiquetarse

- probarse

### ✔️ 11.3 Prohibido acceso directo al hardware

El PLC solo usa APIs seguras.

# ⭐ 12. Prohibiciones absolutas

- operar sin permisos

- operar sin EPP

- operar sin documentación

- operar sin simulación previa

- operar con sensores defectuosos

- operar con herramienta dañada

- operar desactivando límites

- operar sin validar

- operar sin registrar

- operar con ATC desalineado

- operar multieje sin cinemática correcta

# ⭐ 13. Objetivo final

Estas normas garantizan que la operación avanzada CNC‑CAT sea:

- segura

- precisa

- profesional

- industrial

- trazable

- confiable

Son las normas oficiales de seguridad en operación avanzada del ecosistema CNC‑CAT.


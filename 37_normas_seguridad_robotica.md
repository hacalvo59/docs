# 📘 **37\_normas\_seguridad\_robotica.md**

**Normas oficiales de seguridad en integración robótica — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad obligatorias** para integrar y operar robots industriales junto a máquinas controladas por CNC‑CAT, garantizando:

- seguridad del operador

- seguridad del robot

- seguridad del CNC

- sincronización correcta

- cumplimiento industrial

- prevención de colisiones y atrapamientos

Estas normas son **críticas** y deben cumplirse SIEMPRE.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 Un robot + un CNC = riesgo multiplicado

Ambos son máquinas autónomas capaces de causar daño.

### ✔️ 2.2 La coordinación debe ser absoluta

Si uno se mueve sin que el otro lo sepa → accidente.

### ✔️ 2.3 La seguridad debe ser redundante

Ambos sistemas deben poder detenerse mutuamente.

### ✔️ 2.4 Solo personal cualificado puede operar robots

Operadores sin formación → prohibido.

# ⭐ 3. Tipos de integración robótica cubiertos

### ✔️ 3.1 Robots cartesianos

- carga/descarga

- manipulación de piezas

### ✔️ 3.2 Robots antropomórficos (6 ejes)

- alimentación de CNC

- extracción de piezas

- operaciones colaborativas

### ✔️ 3.3 Robots SCARA

- pick & place

- manipulación ligera

### ✔️ 3.4 Robots colaborativos (cobots)

- asistencia al operador

- tareas compartidas

### ✔️ 3.5 Robots móviles (AMR/AGV)

- transporte automático

- logística interna

# ⭐ 4. Requisitos previos

Antes de integrar un robot con CNC‑CAT, el técnico debe:

- ser usuario con rol **administrador**

- revisar documentación del robot

- revisar documentación del CNC

- verificar compatibilidad eléctrica

- verificar compatibilidad mecánica

- verificar compatibilidad de comunicación

- definir zonas de seguridad

- definir handshakes

- realizar backup completo

# ⭐ 5. Zonas de seguridad

### ✔️ 5.1 Zona del CNC

Debe estar delimitada y señalizada.

### ✔️ 5.2 Zona del robot

Debe estar delimitada y señalizada.

### ✔️ 5.3 Zona compartida

Debe tener:

- sensores

- barreras

- límites

- lógica de seguridad

### ✔️ 5.4 Prohibido que el operador entre en zona compartida

Excepto con robot detenido y CNC detenido.

# ⭐ 6. Handshake obligatorio CNC ↔ Robot

Toda integración debe incluir un **protocolo de sincronización**:

### ✔️ 6.1 Señales mínimas

- CNC listo

- Robot listo

- CNC en movimiento

- Robot en movimiento

- CNC detenido

- Robot detenido

- Error CNC

- Error robot

### ✔️ 6.2 Señales de permiso

- permiso para entrar

- permiso para salir

- permiso para cargar

- permiso para descargar

### ✔️ 6.3 Señales de seguridad

- E‑STOP compartido

- parada coordinada

- watchdog de comunicación

# ⭐ 7. Seguridad en carga y descarga automática

### ✔️ 7.1 Prohibido que el robot entre al CNC sin permiso

Debe esperar señal de “CNC seguro”.

### ✔️ 7.2 Prohibido que el CNC se mueva con el robot dentro

Excepto en sistemas certificados.

### ✔️ 7.3 Prohibido usar herramientas sueltas

Riesgo de expulsión.

### ✔️ 7.4 Validación obligatoria

- posición del robot

- posición del CNC

- herramienta

- pieza

- sensores

# ⭐ 8. Seguridad en operaciones colaborativas

### ✔️ 8.1 Prohibido operar sin sensores de presencia

Incluye:

- cámaras

- láser

- barreras

- sensores de fuerza

### ✔️ 8.2 Prohibido operar sin límites de velocidad

Los cobots deben reducir velocidad cerca del operador.

### ✔️ 8.3 Prohibido operar sin parada segura

El robot debe detenerse si detecta contacto.

# ⭐ 9. Seguridad en comunicación CNC ↔ Robot

### ✔️ 9.1 Prohibido usar Wi‑Fi

Solo cableado industrial.

### ✔️ 9.2 Prohibido usar protocolos no seguros

Debe usarse:

- EtherCAT

- Profinet

- Modbus TCP

- señales digitales seguras

### ✔️ 9.3 Prohibido exponer comunicación a internet

Aislamiento total.

# ⭐ 10. Validación de integración robótica

Toda integración debe pasar:

### ✔️ 10.1 Validación funcional

¿Hace lo que debe?

### ✔️ 10.2 Validación de seguridad

¿Puede causar daño?

### ✔️ 10.3 Validación de sincronización

¿Se coordinan correctamente?

### ✔️ 10.4 Validación de estrés

¿Se comporta bien bajo carga?

# ⭐ 11. Documentación obligatoria

Debe incluir:

- esquema eléctrico

- esquema de comunicación

- zonas de seguridad

- handshakes

- parámetros

- firmware

- pruebas realizadas

- resultados

# ⭐ 12. Prohibiciones absolutas

- integrar robots sin documentación

- operar sin EPP

- operar sin sensores

- operar sin handshakes

- operar sin simulación previa

- operar sin validar

- operar sin registrar

- mezclar redes

- usar Wi‑Fi

- permitir acceso directo al hardware

- permitir que el robot mueva ejes del CNC

- permitir que el CNC mueva el robot

# ⭐ 13. Objetivo final

Estas normas garantizan que la integración robótica CNC‑CAT sea:

- segura

- sincronizada

- profesional

- industrial

- trazable

- confiable

Son las normas oficiales de seguridad en robótica del ecosistema CNC‑CAT.


# 📘 **38\_normas\_seguridad\_plc.md**

**Normas oficiales de seguridad en integración con PLC — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad obligatorias** para integrar, comunicar y operar PLCs (Programmable Logic Controllers) junto a máquinas controladas por CNC‑CAT, garantizando:

- seguridad del operador

- seguridad del CNC

- seguridad del PLC

- integridad de señales

- sincronización correcta

- cumplimiento industrial

Estas normas son **críticas** y deben cumplirse SIEMPRE.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 Un PLC nunca debe poder mover ejes directamente

El control de movimiento pertenece exclusivamente al CNC.

### ✔️ 2.2 La comunicación debe ser segura y limitada

El PLC solo puede enviar señales autorizadas.

### ✔️ 2.3 La integración debe ser documentada

Sin documentación → no se integra.

### ✔️ 2.4 La seguridad debe ser redundante

Ambos sistemas deben poder detenerse mutuamente.

# ⭐ 3. Tipos de integración PLC cubiertos

### ✔️ 3.1 PLC como supervisor

- arranque

- parada

- secuencias externas

### ✔️ 3.2 PLC como automatizador

- carga/descarga

- actuadores externos

- sensores auxiliares

### ✔️ 3.3 PLC como sistema de seguridad

- puertas

- barreras

- E‑STOP externos

### ✔️ 3.4 PLC como coordinador

- robots

- cintas

- sistemas auxiliares

# ⭐ 4. Requisitos previos

Antes de integrar un PLC con CNC‑CAT, el técnico debe:

- ser usuario con rol **administrador**

- revisar documentación del PLC

- revisar documentación del CNC

- verificar compatibilidad eléctrica

- verificar compatibilidad de comunicación

- definir señales

- definir permisos

- realizar backup completo

# ⭐ 5. Señales permitidas PLC → CNC

El PLC **solo puede enviar**:

- señales de presencia de pieza

- señales de puerta cerrada

- señales de ciclo externo

- señales de error externo

- señales de fin de secuencia

- señales de actuadores auxiliares

# ⭐ 6. Señales permitidas CNC → PLC

El CNC **solo puede enviar**:

- estado de máquina

- estado de programa

- estado de herramienta

- estado de husillo

- estado de alarmas

- confirmaciones de secuencia

# ⭐ 7. Señales prohibidas

### ❌ Prohibido que el PLC envíe:

- comandos de jog

- comandos de movimiento

- comandos de homing

- comandos de offsets

- comandos de herramienta

- comandos de spindle

### ❌ Prohibido que el CNC envíe:

- señales de control directo de actuadores peligrosos

- señales de bypass de seguridad

# ⭐ 8. Seguridad eléctrica

### ✔️ 8.1 Prohibido mezclar tensiones

Cada sistema debe tener su propia alimentación.

### ✔️ 8.2 Prohibido compartir tierras sin certificación

Evita bucles de masa.

### ✔️ 8.3 Prohibido cableado sin etiquetar

Cada señal debe estar identificada.

### ✔️ 8.4 Prohibido cableado sin blindaje

Especialmente señales analógicas o de alta frecuencia.

# ⭐ 9. Seguridad en comunicación

### ✔️ 9.1 Prohibido usar Wi‑Fi

Solo cableado industrial.

### ✔️ 9.2 Prohibido exponer comunicación a internet

Aislamiento total.

### ✔️ 9.3 Protocolos permitidos

- Modbus TCP

- Profinet

- EtherCAT (solo esclavos)

- señales digitales seguras

### ✔️ 9.4 Validación obligatoria

- latencia

- sincronización

- watchdog

# ⭐ 10. Seguridad en secuencias automáticas

### ✔️ 10.1 Handshake obligatorio

Antes de:

- mover actuadores

- cargar piezas

- descargar piezas

### ✔️ 10.2 Parada coordinada

Si uno entra en emergencia → ambos se detienen.

### ✔️ 10.3 Prohibido ejecutar secuencias sin simulación previa

### ✔️ 10.4 Prohibido ejecutar secuencias sin sensores

Nada de movimientos “a ciegas”.

# ⭐ 11. Validación de integración PLC

Toda integración debe pasar:

### ✔️ 11.1 Validación funcional

¿Hace lo que debe?

### ✔️ 11.2 Validación de seguridad

¿Puede causar daño?

### ✔️ 11.3 Validación de sincronización

¿Se coordinan correctamente?

### ✔️ 11.4 Validación de estrés

¿Se comporta bien bajo carga?

# ⭐ 12. Documentación obligatoria

Debe incluir:

- esquema eléctrico

- esquema de comunicación

- señales definidas

- permisos

- handshakes

- pruebas realizadas

- resultados

# ⭐ 13. Prohibiciones absolutas

- integrar PLC sin documentación

- operar sin EPP

- operar sin sensores

- operar sin handshakes

- operar sin simulación previa

- operar sin validar

- operar sin registrar

- mezclar redes

- usar Wi‑Fi

- permitir que el PLC mueva ejes

- permitir que el PLC modifique parámetros

- permitir que el PLC desactive límites

# ⭐ 14. Objetivo final

Estas normas garantizan que la integración PLC ↔ CNC‑CAT sea:

- segura

- sincronizada

- profesional

- industrial

- trazable

- confiable

Son las normas oficiales de seguridad en integración con PLC del ecosistema CNC‑CAT.


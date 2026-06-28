# 📘 **39\_normas\_seguridad\_ethercat.md**

**Normas oficiales de seguridad en EtherCAT — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad obligatorias** para integrar, configurar y operar EtherCAT dentro del ecosistema CNC‑CAT, garantizando:

- integridad del bus

- seguridad del operador

- seguridad del hardware

- sincronización determinista

- cumplimiento industrial

- prevención de fallos críticos

EtherCAT es el **sistema nervioso** del CNC real. Estas normas son **críticas** y deben cumplirse SIEMPRE.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 EtherCAT es tiempo real duro

Cualquier error → impacto inmediato en la máquina.

### ✔️ 2.2 La seguridad depende de la topología

Un solo cable mal conectado puede detener todo el sistema.

### ✔️ 2.3 La configuración debe ser exacta

Offsets, PDOs, SDOs, modos de operación.

### ✔️ 2.4 Solo personal cualificado puede operar EtherCAT

No es un bus plug‑and‑play.

# ⭐ 3. Requisitos previos

Antes de trabajar con EtherCAT, el técnico debe:

- ser usuario con rol **administrador**

- conocer la topología

- conocer los esclavos

- conocer los PDOs

- conocer los modos de operación

- revisar documentación del fabricante

- realizar backup completo

# ⭐ 4. Seguridad en cableado EtherCAT

### ✔️ 4.1 Prohibido usar cables no industriales

Solo cables:

- CAT5e industriales

- CAT6 industriales

- blindados

- con conectores certificados

### ✔️ 4.2 Prohibido mezclar cables de distinta categoría

Riesgo de jitter.

### ✔️ 4.3 Prohibido usar cables dañados

Ni doblados, ni aplastados, ni pelados.

### ✔️ 4.4 Prohibido usar Wi‑Fi o enlaces inalámbricos

EtherCAT es **solo cable**.

# ⭐ 5. Seguridad en topología

### ✔️ 5.1 Topología recomendada

Línea o anillo.

### ✔️ 5.2 Prohibido conectar esclavos en estrella

No es compatible con EtherCAT.

### ✔️ 5.3 Prohibido mezclar esclavos críticos con no críticos

Separar:

- servos

- IO

- sensores

- actuadores

### ✔️ 5.4 Prohibido cambiar el orden de los esclavos sin actualizar configuración

El orden define la asignación de PDOs.

# ⭐ 6. Seguridad en configuración de esclavos

### ✔️ 6.1 Prohibido usar configuraciones genéricas

Cada esclavo debe tener:

- vendor ID

- product ID

- revision

- PDOs correctos

- modos correctos

### ✔️ 6.2 Prohibido usar PDOs no documentados

Nada de “probar a ver qué pasa”.

### ✔️ 6.3 Prohibido usar modos de operación incorrectos

Ejemplo:

- servos → CSP/CSV

- IO → PDO digital

- sensores → PDO analógico

### ✔️ 6.4 Validación obligatoria

Después de configurar:

- watchdog

- estados

- PDOs

- sincronización

# ⭐ 7. Seguridad en sincronización (DC Sync)

### ✔️ 7.1 Prohibido desactivar Distributed Clocks

El CNC depende de sincronización precisa.

### ✔️ 7.2 Prohibido usar esclavos sin soporte DC

Excepto IO simples.

### ✔️ 7.3 Validación obligatoria

- jitter

- offset

- drift

# ⭐ 8. Seguridad en servos EtherCAT

### ✔️ 8.1 Prohibido usar servos sin encoder funcional

Sin encoder → sin movimiento.

### ✔️ 8.2 Prohibido usar servos sin límites activos

Soft + hard limits.

### ✔️ 8.3 Prohibido usar servos sin watchdog

Debe detenerse ante pérdida de comunicación.

### ✔️ 8.4 Validación obligatoria

- homing

- jog

- límites

- precisión

# ⭐ 9. Seguridad en IO EtherCAT

### ✔️ 9.1 Prohibido mezclar señales de seguridad con señales normales

Separación física y lógica.

### ✔️ 9.2 Prohibido usar IO sin etiquetar

Cada pin debe estar identificado.

### ✔️ 9.3 Prohibido usar IO sin documentación

Nada de señales desconocidas.

# ⭐ 10. Seguridad en diagnóstico

### ✔️ 10.1 Supervisión continua

Debe monitorearse:

- estado del maestro

- estado de esclavos

- watchdog

- errores de PDO

- errores de sincronización

### ✔️ 10.2 Alarmas obligatorias

Cualquier error EtherCAT → STOP inmediato.

### ✔️ 10.3 Logs obligatorios

Registrar:

- fallos

- reconexiones

- cambios de estado

# ⭐ 11. Prohibiciones absolutas

- usar cables no industriales

- usar Wi‑Fi

- mezclar topologías

- cambiar orden de esclavos sin actualizar configuración

- usar PDOs no documentados

- desactivar Distributed Clocks

- operar servos sin encoder

- operar sin watchdog

- ignorar alarmas EtherCAT

- mezclar señales de seguridad con señales normales

- operar sin validación

# ⭐ 12. Objetivo final

Estas normas garantizan que EtherCAT en CNC‑CAT sea:

- seguro

- determinista

- profesional

- industrial

- trazable

- confiable

Son las normas oficiales de seguridad EtherCAT del ecosistema CNC‑CAT.


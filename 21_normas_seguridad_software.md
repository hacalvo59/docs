# 📘 **21\_normas\_seguridad\_software.md**

**Normas oficiales de seguridad del software — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad obligatorias** que deben cumplirse en todo el software del ecosistema CNC‑CAT, garantizando:

- integridad del sistema

- protección del operador

- protección del hardware

- estabilidad del ciclo de control

- prevención de fallos críticos

- cumplimiento industrial

Estas normas son **estrictas** y deben cumplirse SIEMPRE.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 El software debe ser seguro por diseño

No se parchea la seguridad: se diseña desde el inicio.

### ✔️ 2.2 El sistema debe fallar en modo seguro

Si algo falla → detener, no continuar.

### ✔️ 2.3 El software nunca debe confiar en datos externos

Todo debe validarse.

### ✔️ 2.4 El software debe ser determinista

Especialmente en el ciclo de control.

# ⭐ 3. Seguridad en la arquitectura

### ✔️ 3.1 Separación estricta de capas

- UI

- Motion API

- CORE

- Drivers

- EtherCAT

Nunca mezclar responsabilidades.

### ✔️ 3.2 Sin acceso directo al hardware desde la UI

Todo pasa por Motion API.

### ✔️ 3.3 Sin lógica CNC en drivers

Drivers = hardware, nada más.

# ⭐ 4. Seguridad en la Motion API

### ✔️ 4.1 Validación de comandos

La UI nunca debe poder enviar comandos peligrosos.

### ✔️ 4.2 Validación de tipos y rangos

Ejemplo:

python

```
`if cmd\["feedrate"\] \> MAX\_FEEDRATE:`

`    raise MotionAPIError("Feedrate fuera de rango")`
```

### ✔️ 4.3 Validación de estado

No permitir:

- jog durante RUNNING

- homing durante RUNNING

- ejecutar G‑code sin READY

# ⭐ 5. Seguridad en el CORE

### ✔️ 5.1 Planner seguro

- validar trayectorias

- validar aceleraciones

- validar jerk

- validar límites

### ✔️ 5.2 Interpolador determinista

Nada de:

- aleatoriedad

- dependencias externas

- estructuras dinámicas

### ✔️ 5.3 Ciclo de control protegido

- sin logs

- sin asignaciones pesadas

- sin acceso a disco

- sin acceso a red

# ⭐ 6. Seguridad en drivers

### ✔️ 6.1 Validar feedback del servo

Nunca confiar en valores sin verificar.

### ✔️ 6.2 Watchdog obligatorio

Si un servo no responde → detener máquina.

### ✔️ 6.3 Validar coherencia

Ejemplo:

python

```
`if abs(feedback - command) \> MAX\_ERROR:`

`    raise ServoError("Desviación excesiva")`
```

# ⭐ 7. Seguridad en la UI LINCAT

### ✔️ 7.1 Botones críticos requieren confirmación

- STOP

- RESET

- CLEAR ALARMS

- TOOL CHANGE

### ✔️ 7.2 Indicadores siempre visibles

- estado máquina

- alarmas

- límites

- E‑STOP

### ✔️ 7.3 Prohibido ocultar errores

La UI debe mostrar todo.

# ⭐ 8. Seguridad en el PLC integrado

### ✔️ 8.1 Validar bytecode

Nunca ejecutar bytecode corrupto.

### ✔️ 8.2 Tiempo máximo por ciclo

El PLC nunca puede bloquear el ciclo CNC.

### ✔️ 8.3 Sin acceso directo a hardware

El PLC solo usa APIs seguras.

# ⭐ 9. Seguridad en G‑code

### ✔️ 9.1 Validar comandos

Nada de G‑code inválido.

### ✔️ 9.2 Validar trayectorias

Nada de movimientos imposibles.

### ✔️ 9.3 Validar offsets

Nunca permitir offsets corruptos.

### ✔️ 9.4 Validar herramientas

No permitir:

- herramienta inexistente

- herramienta sin longitud

- herramienta sin diámetro

# ⭐ 10. Seguridad en la comunicación

### ✔️ 10.1 Motion API debe ser robusta

Nunca confiar en datos sin validar.

### ✔️ 10.2 Prohibido ejecutar comandos remotos sin autenticación

Especialmente en entornos industriales.

### ✔️ 10.3 Prohibido exponer puertos innecesarios

# ⭐ 11. Seguridad en logs y diagnósticos

### ✔️ 11.1 Sin logs en el ciclo de control

Solo en modo debug controlado.

### ✔️ 11.2 Logs deben ser claros

Nada de mensajes ambiguos.

### ✔️ 11.3 Logs no deben contener datos sensibles

# ⭐ 12. Prohibiciones absolutas

- ignorar alarmas

- ignorar límites

- ignorar estados

- ejecutar G‑code sin validación

- mezclar UI + hardware

- mezclar drivers + lógica CNC

- usar `Exception` genérica

- silenciar errores

- usar hilos sin control

- usar acceso a disco en 1 kHz

- usar acceso a red en 1 kHz

# ⭐ 13. Objetivo final

Estas normas garantizan que el software CNC‑CAT sea:

- seguro

- robusto

- industrial

- confiable

- profesional

- apto para producción real

Son las normas oficiales de seguridad del software.


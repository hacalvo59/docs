# 📘 **18\_normas\_seguridad\_codigo.md**

**Normas oficiales de seguridad en el código — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad obligatorias** que deben cumplirse en todo el código del ecosistema CNC‑CAT, garantizando:

- integridad del sistema

- protección del hardware

- protección del operador

- estabilidad del ciclo de control

- prevención de fallos críticos

- cumplimiento industrial

Estas normas son **estrictas** y **no negociables**.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 La seguridad está por encima del rendimiento

Si hay conflicto entre velocidad y seguridad → gana seguridad.

### ✔️ 2.2 Nunca confiar en hardware externo

Todo dato debe validarse.

### ✔️ 2.3 El sistema debe fallar en modo seguro

Si algo va mal → detener, no continuar.

### ✔️ 2.4 El código debe ser explícito

Nada de comportamientos implícitos o mágicos.

# ⭐ 3. Validación de parámetros

### ✔️ 3.1 Validar todo input

Ejemplo:

python

```
`if speed \< 0 or speed \> MAX\_FEEDRATE:`

`    raise InvalidParameterError("Feedrate fuera de rango")`
```

### ✔️ 3.2 Validar tipos

Nunca asumir que un valor es correcto.

### ✔️ 3.3 Validar límites físicos

Antes de mover un eje:

python

```
`if target \> axis.max\_limit:`

`    raise LimitError("Movimiento fuera de límites")`
```

# ⭐ 4. Validación de estados

### ✔️ 4.1 Cada acción debe verificar el estado de la máquina

Ejemplo:

python

```
`if self.state != MachineState.READY:`

`    raise InvalidStateError("No se puede ejecutar G-code sin homing")`
```

### ✔️ 4.2 Estados prohibidos para movimiento

- INIT

- ERROR

- ESTOP

- STOPPING

### ✔️ 4.3 El sistema debe impedir acciones peligrosas

Ejemplo:

- Jog durante RUNNING

- Homing durante RUNNING

- Cambiar herramienta sin STOP

# ⭐ 5. Manejo de errores

### ✔️ 5.1 Excepciones específicas

Nunca usar `Exception` genérica.

### ✔️ 5.2 Mensajes claros

Siempre indicar:

- qué falló

- por qué falló

- cómo evitarlo

### ✔️ 5.3 Nunca silenciar errores

Prohibido:

python

```
`try:`

`    ...`

`except:`

`    pass`
```

# ⭐ 6. Seguridad en el ciclo de control (1 kHz)

### ✔️ 6.1 Prohibido asignar objetos pesados

Nada de:

- listas nuevas

- diccionarios nuevos

- objetos temporales

### ✔️ 6.2 Prohibido logs dentro del ciclo

Solo en modo debug controlado.

### ✔️ 6.3 Prohibido acceso a disco

Nunca.

### ✔️ 6.4 Prohibido acceso a red

Excepto EtherCAT.

# ⭐ 7. Seguridad en drivers y hardware

### ✔️ 7.1 Nunca confiar en valores del servo

Validar:

- posición

- velocidad

- estado

- watchdog

### ✔️ 7.2 Comprobar coherencia

Ejemplo:

python

```
`if abs(feedback - command) \> MAX\_ERROR:`

`    raise ServoError("Desviación excesiva")`
```

### ✔️ 7.3 Watchdog obligatorio

Si un servo no responde → detener máquina.


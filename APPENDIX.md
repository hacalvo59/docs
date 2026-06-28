# 📘 **APPENDIX.md**

**Apéndices técnicos y notas adicionales del ecosistema LINCAT / CNC‑CAT**

# ⭐ **1. Propósito**

Este documento reúne:

- notas técnicas

- tablas de referencia

- valores por defecto

- ejemplos extendidos

- diagramas auxiliares

- aclaraciones conceptuales

- material complementario

Es el “cajón técnico” del ecosistema.

# ⭐ **2. Tabla de estados del sistema**

| **Estado** | **Descripción** | **Transiciones permitidas** |
| :-: | :-: | :-: |
| **INIT** | Sistema arrancando | → IDLE |
| **IDLE** | Encendido sin homing | → READY |
| **READY** | Homing completado | → RUNNING, → IDLE |
| **RUNNING** | Programa ejecutándose | → PAUSED, → STOPPING |
| **PAUSED** | Ejecución detenida | → RUNNING, → STOPPING |
| **STOPPING** | Detención controlada | → IDLE |
| **ERROR** | Fallo recuperable | → IDLE |
| **ESTOP** | Fallo crítico | → INIT |

# ⭐ **3. Tabla de alarmas comunes**

| **Código** | **Tipo** | **Descripción** |
| :-: | :-: | :-: |
| **A001** | Límite | Eje fuera de límites |
| **A010** | Servo | Fallo de habilitación |
| **A020** | EtherCAT | Esclavo no responde |
| **A030** | Planner | Movimiento inválido |
| **A040** | Interpolador | Ciclo excedido |
| **A050** | PLC | Error de bytecode |

# ⭐ **4. Códigos G más usados**

| **Código** | **Acción** |
| :-: | :-: |
| **G0** | Movimiento rápido |
| **G1** | Movimiento lineal |
| **G2** | Circular CW |
| **G3** | Circular CCW |
| **G17/G18/G19** | Selección de plano |
| **G20/G21** | Pulgadas / mm |
| **G28** | Volver a home |
| **G90/G91** | Absoluto / relativo |

# ⭐ **5. Códigos M más usados**

| **Código** | **Acción** |
| :-: | :-: |
| **M3** | Husillo CW |
| **M4** | Husillo CCW |
| **M5** | Parar husillo |
| **M6** | Cambio de herramienta |
| **M7/M8** | Refrigerante |
| **M9** | Apagar refrigerante |

# ⭐ **6. Ejemplo completo de G‑code**

Código

```
`G21`

`G90`

`G0 X0 Y0 Z5`

`G1 Z-2 F200`

`G1 X50 Y50 F800`

`G2 X100 Y0 I25 J-25`

`G0 Z5`

`M5`

`M30`
```

# ⭐ **7. Ejemplo completo de configuración YAML**

yaml

```
`machine:`

`  axes:`

`    X:`

`      steps\_per\_mm: 160`

`      max\_velocity: 5000`

`      max\_acceleration: 2000`

`      limits:`

`        min: -10`

`        max: 510`

`    Y:`

`      steps\_per\_mm: 160`

`      max\_velocity: 5000`

`      max\_acceleration: 2000`

`      limits:`

`        min: -10`

`        max: 510`
```

# ⭐ **8. Ejemplo de tarea PLC**

st

```
`PROGRAM main`

`VAR`

`    counter : INT := 0;`

`END\_VAR`


`counter := counter + 1;`


`IF counter \> 1000 THEN`

`    counter := 0;`

`END\_IF;`
```

# ⭐ **9. Ejemplo de comunicación UI → Motion API**

json

```
`\{`

`  "cmd": "jog",`

`  "axis": "X",`

`  "velocity": 1200`

`\}`
```

# ⭐ **10. Ejemplo de respuesta Motion API → UI**

json

```
`\{`

`  "status": "ok",`

`  "position": \{`

`    "X": 12.554,`

`    "Y": 0.000,`

`    "Z": 5.000`

`  \}`

`\}`
```

# ⭐ **11. Valores por defecto del sistema**

| **Parámetro** | **Valor** |
| :-: | :-: |
| **cycle\_time\_ms** | 1 |
| **ui\_port** | 5555 |
| **diag\_port** | 7777 |
| **plc\_cycle\_ms** | 10 |
| **max\_axes** | 6 |

# ⭐ **12. Diagramas auxiliares**

## **12.1 Flujo de homing**

Código

```
`START`

` ↓`

`SEARCH SWITCH`

` ↓`

`LATCH`

` ↓`

`OFFSET`

` ↓`

`DONE`
```

## **12.2 Flujo de ejecución**

Código

```
`LOAD → PLAN → INTERPOLATE → EXECUTE → MONITOR → END`
```

# ⭐ **13. Notas sobre rendimiento**

- EtherCAT estable requiere NIC Intel.

- El interpolador debe ejecutarse a 1 kHz.

- El PLC no debe bloquear el ciclo.

- La UI debe mantenerse en hilo separado.

# ⭐ **14. Notas sobre seguridad**

- E‑STOP siempre físico.

- Límites siempre activos.

- Nunca ejecutar sin homing.

- Nunca ignorar alarmas.

# ⭐ **15. Objetivo final**

Este apéndice sirve como:

- referencia rápida

- material de apoyo

- ejemplos prácticos

- tablas técnicas

- notas de ingeniería

Es el complemento perfecto para toda la documentación.


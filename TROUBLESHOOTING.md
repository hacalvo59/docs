# 📘 **TROUBLESHOOTING.md**

**Guía oficial de resolución de problemas del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Esta guía proporciona soluciones rápidas y claras a los problemas más comunes del ecosistema:

- UI LINCAT

- Motion API

- CNC‑CAT Core

- Motores (sim/real)

- EtherCAT

- PLC integrado

- Drivers

- Documentación

- Despliegue

- Operación

Es la guía que un técnico industrial consulta cuando algo **no funciona**.

# ⭐ 2. Problemas de inicio

## **2.1 La UI no arranca**

**Síntomas:**

- ventana no aparece

- error de PySide6

**Solución:**

- reinstalar dependencias

bash

```
`pip install -r requirements.txt`
```

- borrar caché

Código

```
`~/.local/share/lincat/cache/`
```

## **2.2 El motor simulado no arranca**

**Síntomas:**

- error al ejecutar `main\_simulation.py`

**Solución:**

- verificar Python 3.10+

- reinstalar dependencias

- revisar rutas relativas

## **2.3 El motor real no arranca**

**Síntomas:**

- error de permisos

- error de SOEM

- error de EtherCAT

**Solución:**

bash

```
`sudo python3 main\_real.py`
```

- verificar que SOEM esté instalado

- verificar que la NIC esté en modo real‑time

# ⭐ 3. Problemas de homing

## **3.1 Homing no avanza**

**Causas:**

- sensor no detectado

- límites mal configurados

- servo no habilitado

**Solución:**

- revisar wiring

- revisar PDO de sensores

- revisar configuración de límites

## **3.2 Homing se detiene en LATCH**

**Causas:**

- sensor ruidoso

- mala posición mecánica

**Solución:**

- ajustar sensor

- revisar distancia de activación

# ⭐ 4. Problemas de movimiento

## **4.1 Jog no funciona**

**Causas:**

- estado ≠ READY

- alarma activa

- E‑STOP activo

**Solución:**

- verificar estado

- limpiar alarmas

- revisar E‑STOP

## **4.2 Movimiento brusco o irregular**

**Causas:**

- interpolador mal configurado

- servo saturado

- EtherCAT con jitter

**Solución:**

- revisar parámetros del interpolador

- revisar ganancia del servo

- revisar sincronización DC

# ⭐ 5. Problemas de ejecución de G‑code

## **5.1 Error al cargar archivo**

**Causas:**

- sintaxis inválida

- caracteres no soportados

**Solución:**

- validar con parser

- limpiar caracteres especiales

## **5.2 Ejecución se detiene inesperadamente**

**Causas:**

- alarma

- límite

- error de interpolación

**Solución:**

- revisar panel de alarmas

- revisar límites

- revisar planner

# ⭐ 6. Problemas de EtherCAT

## **6.1 Esclavos no aparecen**

**Solución:**

bash

```
`ethercat slaves`
```

- revisar cableado

- revisar alimentación

- revisar NIC

## **6.2 Esclavos no pasan a OP**

**Causas:**

- PDO incorrectos

- firmware incompatible

- sincronización fallida

**Solución:**

- revisar PDO

- revisar SDO

- revisar DC

## **6.3 Pérdida de sincronía**

**Causas:**

- jitter

- cable defectuoso

- servo lento

**Solución:**

- cambiar cable

- revisar servo

- revisar topología

# ⭐ 7. Problemas del PLC integrado

## **7.1 Error de compilación**

**Causas:**

- sintaxis ST incorrecta

**Solución:**

- revisar logs del parser

## **7.2 Bytecode inválido**

**Causas:**

- AST corrupto

- error en optimización

**Solución:**

- regenerar bytecode

## **7.3 Runtime se congela**

**Causas:**

- loop infinito

- acceso ilegal a IO

**Solución:**

- usar debugger

- revisar tareas cíclicas

# ⭐ 8. Problemas de UI LINCAT

## **8.1 Paneles no actualizan**

**Causas:**

- señales desconectadas

- Motion API no responde

**Solución:**

- revisar logs

- reiniciar UI

## **8.2 Widgets congelados**

**Causas:**

- bloqueo en hilo principal

**Solución:**

- mover tareas pesadas a threads

# ⭐ 9. Problemas de documentación

## **9.1 MkDocs no compila**

**Causas:**

- enlaces rotos

- archivos faltantes

**Solución:**

bash

```
`mkdocs build`
```

## **9.2 PDF no genera**

**Causas:**

- falta LaTeX

- error en includes

**Solución:**

bash

```
`sudo apt install texlive-full`
```

# ⭐ 10. Problemas de despliegue

## **10.1 Servicios systemd no arrancan**

**Causas:**

- rutas incorrectas

- permisos insuficientes

**Solución:**

bash

```
`sudo systemctl status cnc-cat`
```

# ⭐ 11. Objetivo final

Garantizar que cualquier problema del ecosistema pueda:

- diagnosticarse

- reproducirse

- aislarse

- corregirse

- verificarse

de forma **industrial, segura y profesional**.


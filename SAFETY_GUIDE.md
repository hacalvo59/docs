# 📘 **SAFETY\_GUIDE.md**

**Guía oficial de seguridad operativa del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Esta guía define las normas de seguridad necesarias para operar el ecosistema:

- seguridad del operador

- seguridad de la máquina

- seguridad eléctrica

- seguridad mecánica

- seguridad del software

- seguridad del entorno

- seguridad en producción

El objetivo es garantizar un sistema **seguro, confiable y apto para uso industrial**.

# ⭐ 2. Principios fundamentales de seguridad

1. **La seguridad siempre tiene prioridad sobre la producción.**

2. **Ninguna operación debe realizarse sin E‑STOP funcional.**

3. **Nunca operar sin límites físicos y software activos.**

4. **Nunca operar sin homing válido.**

5. **Nunca ignorar alarmas.**

6. **Nunca modificar parámetros críticos sin autorización.**

# ⭐ 3. Seguridad del operador

## **3.1 Reglas obligatorias**

- Mantener distancia segura durante movimientos.

- No introducir manos en la zona de trabajo.

- No usar ropa suelta.

- Usar gafas de protección.

- Usar calzado de seguridad.

## **3.2 Supervisión**

- El operador debe estar presente durante toda la ejecución.

- No dejar la máquina funcionando sin vigilancia.

# ⭐ 4. Seguridad mecánica

## **4.1 Requisitos**

- guías limpias

- husillos lubricados

- protecciones instaladas

- puertas cerradas (si aplica)

## **4.2 Riesgos**

- atrapamiento

- colisión

- vibración excesiva

- rotura de herramienta

## **4.3 Prevención**

- límites configurados

- offsets correctos

- herramientas bien sujetas

- piezas bien fijadas

# ⭐ 5. Seguridad eléctrica

## **5.1 Requisitos**

- armario eléctrico cerrado

- cables ordenados

- tierra obligatoria

- fusibles adecuados

- relés de seguridad

## **5.2 Riesgos**

- cortocircuitos

- sobrecargas

- descargas eléctricas

## **5.3 Prevención**

- inspección mensual

- ventilación adecuada

- evitar humedad

# ⭐ 6. Seguridad del software

## **6.1 Reglas**

- no modificar código en producción

- no desactivar alarmas

- no desactivar límites

- no desactivar watchdog

- no ejecutar código no firmado

## **6.2 Validaciones**

- pruebas en simulación

- pruebas HIL

- pruebas en máquina real

- documentación actualizada

# ⭐ 7. Seguridad en EtherCAT

## **7.1 Requisitos**

- NIC dedicada

- cables industriales

- topología estable

- sincronización DC válida

## **7.2 Riesgos**

- pérdida de sincronía

- servo runaway

- PDO corruptos

## **7.3 Prevención**

- watchdog activo

- límites físicos

- E‑STOP funcional

# ⭐ 8. Seguridad en PLC integrado

## **8.1 Riesgos**

- loops infinitos

- acceso ilegal a IO

- tareas mal configuradas

## **8.2 Prevención**

- validación del bytecode

- límites de tiempo

- aislamiento de memoria

# ⭐ 9. Seguridad en operación

## **9.1 Antes de operar**

- homing

- límites

- offsets

- herramientas

- sondas

- E‑STOP

## **9.2 Durante la operación**

- supervisión constante

- monitoreo de alarmas

- monitoreo de carga del servo

- monitoreo de temperatura

## **9.3 Después de operar**

- detener programa

- volver a IDLE

- apagar motor

- apagar máquina

# ⭐ 10. Seguridad en producción industrial

## **10.1 Requisitos**

- doble canal de E‑STOP

- relés de seguridad

- enclavamientos

- protecciones físicas

- cortinas de luz (opcional)

- UPS

- watchdog hardware

## **10.2 Auditoría**

- mensual

- trimestral

- anual

# ⭐ 11. Procedimientos de emergencia

## **11.1 E‑STOP**

- detiene todo movimiento

- corta energía del servo

- requiere reinicio manual

## **11.2 Parada segura**

- detiene interpolador

- detiene planner

- mantiene control del servo

## **11.3 Fallo crítico**

- apagar máquina

- revisar armario

- revisar servos

- revisar EtherCAT

# ⭐ 12. Objetivo final

Garantizar que el ecosistema LINCAT / CNC‑CAT se opere:

- sin riesgos

- sin improvisación

- sin accidentes

- con profesionalidad

- con estándares industriales


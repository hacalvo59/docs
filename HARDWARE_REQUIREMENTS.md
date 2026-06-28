# 📘 **HARDWARE\_REQUIREMENTS.md**

**Requisitos oficiales de hardware del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Este documento define el hardware necesario para:

- desarrollo

- simulación

- pruebas HIL

- operación real

- producción industrial

El objetivo es garantizar que el ecosistema funcione con **estabilidad, precisión y seguridad industrial**.

# ⭐ 2. Requisitos para desarrollo

## **2.1 Hardware mínimo**

- CPU: 4 núcleos

- RAM: 8 GB

- GPU: no requerida

- Disco: 20 GB libres

- Red: 1 NIC

## **2.2 Hardware recomendado**

- CPU: 6–8 núcleos

- RAM: 16 GB

- SSD NVMe

- Monitor 1080p o superior

# ⭐ 3. Requisitos para simulación

## **3.1 Hardware mínimo**

- CPU: 4 núcleos

- RAM: 8 GB

- Sin hardware industrial

## **3.2 Hardware recomendado**

- CPU: 8 núcleos

- RAM: 16 GB

- SSD

- Monitor dual (UI + diagnósticos)

# ⭐ 4. Requisitos para pruebas HIL (Hardware‑in‑the‑Loop)

## **4.1 Hardware obligatorio**

- Servomotores reales

- Encoders reales

- Drivers industriales

- Sensores de homing

- Sensores de límites

- E‑STOP físico

- Armario eléctrico básico

- Fuente de alimentación industrial

## **4.2 Requisitos de seguridad**

- parada de emergencia

- fusibles

- relés de seguridad

- ventilación

- protecciones mecánicas

# ⭐ 5. Requisitos para operación real

## **5.1 Controlador**

- CPU: 4–8 núcleos

- RAM: 8–16 GB

- SSD

- NIC dedicada para EtherCAT

- Kernel RT (recomendado)

## **5.2 Servos**

- servos industriales con soporte EtherCAT

- drivers con PDO estándar

- encoders absolutos o incrementales

## **5.3 Sensores**

- homing

- límites

- sondas

- sensores de puerta (opcional)

## **5.4 Armario eléctrico**

- ventilación

- protección térmica

- relés

- contactores

- E‑STOP

- fuente 24V industrial

# ⭐ 6. Requisitos para producción industrial

## **6.1 Controlador industrial**

- CPU industrial fanless

- SSD industrial

- NIC Intel i210 o i225

- UPS

- watchdog hardware

## **6.2 Máquina CNC**

- estructura rígida

- guías lineales

- husillos de bolas

- servos sincronizados

- sensores redundantes

## **6.3 Seguridad**

- doble canal de E‑STOP

- relés de seguridad

- enclavamientos

- protecciones físicas

- cortinas de luz (opcional)

# ⭐ 7. Requisitos de red

## **7.1 NIC para EtherCAT**

- Intel i210 (recomendada)

- Intel i225

- Realtek NO recomendado

## **7.2 Topología**

Código

```
`PC → NIC dedicada → EtherCAT → Drivers → Servos`
```

# ⭐ 8. Requisitos de alimentación

## **8.1 Voltajes típicos**

- 24V DC (control)

- 48–72V DC (servos pequeños)

- 220–380V AC (servos grandes)

## **8.2 Reglas**

- fuentes industriales

- protecciones térmicas

- fusibles

- tierra obligatoria

# ⭐ 9. Requisitos de sensores y actuadores

## **9.1 Sensores**

- inductivos

- ópticos

- mecánicos (evitar si es posible)

## **9.2 Actuadores**

- servos

- husillo

- relés

- neumática (opcional)

# ⭐ 10. Objetivo final

Garantizar que el ecosistema LINCAT / CNC‑CAT funcione sobre hardware:

- seguro

- industrial

- confiable

- preciso

- estable

- escalable


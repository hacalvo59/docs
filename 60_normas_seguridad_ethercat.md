# 📘 **60\_normas\_seguridad\_ethercat.md**

**Normas oficiales de seguridad para EtherCAT — CNC‑CAT / LINCAT**

## ⭐ 1. Propósito

Definir las **normas de seguridad para el bus EtherCAT** dentro del ecosistema CNC‑CAT, garantizando:

- seguridad del operador

- integridad de la red

- integridad de los esclavos

- estabilidad del ciclo de control

- cumplimiento industrial

EtherCAT es el sistema nervioso del CNC. Si falla, la máquina falla. Estas normas son **críticas** y deben cumplirse SIEMPRE.

## ⭐ 2. Principios fundamentales

- **EtherCAT exige cables industriales** — no admite cables baratos.

- **La topología debe ser correcta** — errores → pérdida de sincronía.

- **La latencia debe ser mínima** — afecta al ciclo de control.

- **La tierra debe ser común** — evita ruido y fallos.

## ⭐ 3. Componentes EtherCAT cubiertos

- **Master EtherCAT**

- **Slaves**

- **PDOs**

- **SDOs**

- **Cables y conectores**

- **Topología**

## ⭐ 4. Requisitos previos

Antes de operar EtherCAT:

- **Revisar topología**

- **Revisar cables**

- **Revisar tierra**

- **Revisar configuración PDO**

- **Revisar sincronización**

## ⭐ 5. Seguridad en el Master EtherCAT

- **Prohibido operar sin reloj sincronizado**

- **Prohibido operar sin watchdog**

- **Prohibido operar sin latencia validada**

- Validación obligatoria:

  - jitter

  - latencia

  - errores de frame

## ⭐ 6. Seguridad en Slaves EtherCAT

- **Prohibido mezclar slaves sin certificación**

- **Prohibido operar con firmware incorrecto**

- **Prohibido operar sin PDOs correctos**

- Validación obligatoria:

  - estado AL

  - errores

  - sincronización

## ⭐ 7. Seguridad en PDOs

- **Prohibido mapear PDOs sin documentación**

- **Prohibido usar PDOs inconsistentes**

- **Prohibido usar PDOs sin tamaño fijo**

- Validación obligatoria:

  - tamaño

  - orden

  - frecuencia

## ⭐ 8. Seguridad en SDOs

- **Prohibido escribir SDOs durante operación**

- **Prohibido usar SDOs sin límites**

- **Prohibido usar SDOs sin documentación**

- Validación obligatoria:

  - valores

  - rangos

  - consistencia

## ⭐ 9. Seguridad en cables y conectores

- **Prohibido usar cables no industriales**

- **Prohibido usar conectores sin blindaje**

- **Prohibido usar cables dañados**

- Validación obligatoria:

  - continuidad

  - blindaje

  - ruido

## ⭐ 10. Seguridad en topología

- **Prohibido usar topologías incorrectas**

- **Prohibido mezclar anillos sin redundancia**

- **Prohibido usar longitudes excesivas**

- Validación obligatoria:

  - orden

  - distancia

  - sincronización

## ⭐ 11. Prohibiciones absolutas

- operar sin reloj sincronizado

- operar sin watchdog

- usar cables no industriales

- usar conectores sin blindaje

- mezclar slaves no certificados

- escribir SDOs durante operación

- ignorar jitter

- ignorar latencia

- ignorar errores de frame

- operar sin validar

- operar sin registrar

## ⭐ 12. Objetivo final

Estas normas garantizan que EtherCAT en CNC‑CAT sea:

- seguro

- estable

- preciso

- profesional

- industrial

- trazable

- confiable

Son las normas oficiales de seguridad EtherCAT del ecosistema CNC‑CAT.


# 📘 **32\_normas\_seguridad\_integracion.md**

**Normas oficiales de seguridad en integración — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad obligatorias** para integrar CNC‑CAT con:

- hardware externo

- software externo

- sistemas industriales

- PLCs

- robots

- sensores avanzados

- módulos personalizados

Garantizando:

- estabilidad

- compatibilidad

- seguridad

- trazabilidad

- cumplimiento industrial

Estas normas son **estrictas** y deben cumplirse SIEMPRE.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 La integración nunca debe comprometer la seguridad

Si una integración introduce riesgo → se rechaza.

### ✔️ 2.2 La integración debe ser modular

Nada de acoplamientos rígidos o dependencias ocultas.

### ✔️ 2.3 La integración debe ser reversible

Debe poder desinstalarse sin romper el sistema.

### ✔️ 2.4 La integración debe ser verificable

Debe existir un procedimiento de validación.

# ⭐ 3. Tipos de integración cubiertos

### ✔️ 3.1 Integración de hardware

- servos

- drivers

- sensores

- actuadores

- módulos EtherCAT

- PLCs externos

### ✔️ 3.2 Integración de software

- sistemas MES

- sistemas SCADA

- sistemas ERP

- módulos personalizados

- APIs externas

### ✔️ 3.3 Integración de comunicación

- protocolos industriales

- buses de campo

- redes dedicadas

# ⭐ 4. Requisitos previos

Antes de integrar cualquier elemento, el técnico debe:

- ser usuario con rol **administrador**

- revisar documentación del fabricante

- verificar compatibilidad eléctrica

- verificar compatibilidad mecánica

- verificar compatibilidad de comunicación

- verificar compatibilidad de software

- realizar backup completo

# ⭐ 5. Seguridad en integración de hardware

### ✔️ 5.1 Prohibido conectar hardware sin documentación

Nada de “probar a ver si funciona”.

### ✔️ 5.2 Prohibido conectar hardware sin apagar la máquina

Excepto módulos hot‑swap certificados.

### ✔️ 5.3 Prohibido mezclar tensiones

Ejemplo:

- 24V con 5V

- 48V con 24V

### ✔️ 5.4 Prohibido usar cables no certificados

Especialmente en:

- encoders

- EtherCAT

- señales de seguridad

### ✔️ 5.5 Validación obligatoria

Después de integrar hardware:

- homing

- límites

- sensores

- servos

- watchdog

# ⭐ 6. Seguridad en integración de software

### ✔️ 6.1 Prohibido integrar software sin sandbox

Primero se prueba en entorno aislado.

### ✔️ 6.2 Prohibido integrar software sin revisión de código

Debe ser auditado.

### ✔️ 6.3 Prohibido integrar software sin control de permisos

Nada de accesos abiertos.

### ✔️ 6.4 Prohibido integrar software que modifique el ciclo de control

El ciclo CNC es intocable.

# ⭐ 7. Seguridad en integración de comunicación

### ✔️ 7.1 Prohibido exponer Motion API a la red

Debe permanecer local.

### ✔️ 7.2 Prohibido usar Wi‑Fi

Solo cableado industrial.

### ✔️ 7.3 Prohibido mezclar red CNC con red corporativa

Aislamiento total.

### ✔️ 7.4 Validación de latencia

Toda integración debe cumplir:

Código

```
`latencia \< 1 ms (si afecta al ciclo)`
```

# ⭐ 8. Integración con PLCs externos

### ✔️ 8.1 Comunicación unidireccional controlada

El PLC nunca debe poder:

- mover ejes

- modificar parámetros

- desactivar límites

### ✔️ 8.2 Validación de señales

Cada señal debe:

- documentarse

- etiquetarse

- probarse

### ✔️ 8.3 Prohibido acceso directo al hardware

El PLC solo usa APIs seguras.

# ⭐ 9. Integración con robots

### ✔️ 9.1 Zona de seguridad compartida

Debe definirse:

- área de trabajo

- límites

- zonas prohibidas

### ✔️ 9.2 Handshake obligatorio

Antes de:

- mover robot

- mover CNC

- intercambiar piezas

### ✔️ 9.3 Parada coordinada

Si uno entra en emergencia → ambos se detienen.

# ⭐ 10. Validación de integración

Toda integración debe pasar:

### ✔️ 10.1 Validación funcional

¿Hace lo que debe?

### ✔️ 10.2 Validación de seguridad

¿Puede causar daño?

### ✔️ 10.3 Validación de estrés

¿Se comporta bien bajo carga?

### ✔️ 10.4 Validación de compatibilidad

¿Rompe algo existente?

# ⭐ 11. Documentación obligatoria

Toda integración debe documentarse:

- esquema eléctrico

- esquema de comunicación

- configuración

- parámetros

- firmware

- versión

- pruebas realizadas

- resultados

# ⭐ 12. Prohibiciones absolutas

- integrar hardware sin documentación

- integrar software sin sandbox

- integrar sin backup

- integrar sin permisos

- integrar sin validación

- exponer Motion API

- mezclar redes

- modificar ciclo de control

- ignorar incompatibilidades

- usar cables no certificados

# ⭐ 13. Objetivo final

Estas normas garantizan que las integraciones CNC‑CAT sean:

- seguras

- compatibles

- profesionales

- industriales

- trazables

- mantenibles

Son las normas oficiales de seguridad en integración del ecosistema CNC‑CAT.


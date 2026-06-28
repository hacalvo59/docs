# 📘 **43\_normas\_seguridad\_gpio.md**

**Normas oficiales de seguridad para GPIO — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad obligatorias** para instalar, cablear, integrar, operar y diagnosticar señales GPIO (General Purpose Input/Output) dentro del ecosistema CNC‑CAT, garantizando:

- seguridad del operador

- integridad del hardware

- integridad de señales

- estabilidad del sistema

- cumplimiento industrial

GPIO es la capa más simple… y la más peligrosa si se usa mal. Estas normas son **críticas** y deben cumplirse SIEMPRE.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 GPIO no es un juguete

Un pin mal cableado puede destruir hardware.

### ✔️ 2.2 GPIO debe ser documentado

Cada pin debe tener función clara y fija.

### ✔️ 2.3 GPIO debe ser seguro

Nunca debe controlar elementos peligrosos sin protección.

### ✔️ 2.4 Solo personal cualificado puede manipular GPIO

No es para operadores sin formación.

# ⭐ 3. Tipos de señales GPIO cubiertas

### ✔️ 3.1 Entradas digitales

- finales de carrera

- sensores

- botones

- señales externas

### ✔️ 3.2 Salidas digitales

- relés

- actuadores

- solenoides

- indicadores

### ✔️ 3.3 Entradas analógicas

- temperatura

- corriente

- presión

### ✔️ 3.4 Salidas PWM

- ventiladores

- drivers auxiliares

# ⭐ 4. Requisitos previos

Antes de trabajar con GPIO, el técnico debe:

- ser usuario con rol **técnico** o **administrador**

- revisar documentación del hardware

- revisar tensiones

- revisar corrientes máximas

- revisar polaridades

- revisar blindaje

- revisar conectores

- revisar topología

# ⭐ 5. Equipo de protección personal (EPP)

Obligatorio:

- gafas de seguridad

- calzado de seguridad

Opcional según operación:

- guantes aislantes

# ⭐ 6. Seguridad en cableado GPIO

### ✔️ 6.1 Prohibido cablear con la máquina energizada

Debe estar apagada y bloqueada (LOTO).

### ✔️ 6.2 Prohibido mezclar tensiones

Ejemplo:

- 24V con 5V

- 48V con 24V

### ✔️ 6.3 Prohibido usar cables sin blindaje

Evita ruido eléctrico.

### ✔️ 6.4 Prohibido usar cables dañados

Ni pelados, ni doblados, ni aplastados.

### ✔️ 6.5 Prohibido cablear sin etiquetar

Cada pin debe estar identificado.

### ✔️ 6.6 Validación obligatoria

Después de cablear:

- continuidad

- polaridad

- tensión

- ruido

- estabilidad

# ⭐ 7. Seguridad en entradas digitales

### ✔️ 7.1 Prohibido usar entradas sin resistencia adecuada

Evita falsos positivos.

### ✔️ 7.2 Prohibido usar sensores sin documentación

Cada sensor tiene su rango.

### ✔️ 7.3 Prohibido usar entradas sin filtrado

Evita rebotes.

### ✔️ 7.4 Validación obligatoria

- repetibilidad

- histéresis

- estabilidad

# ⭐ 8. Seguridad en salidas digitales

### ✔️ 8.1 Prohibido conectar cargas sin relé o driver

GPIO no puede alimentar cargas directamente.

### ✔️ 8.2 Prohibido usar salidas sin protección

Diodos flyback para cargas inductivas.

### ✔️ 8.3 Prohibido usar salidas sin documentación

Evita daños.

### ✔️ 8.4 Validación obligatoria

- corriente

- tensión

- temperatura

# ⭐ 9. Seguridad en entradas analógicas

### ✔️ 9.1 Prohibido usar sensores sin calibración

Especialmente temperatura y corriente.

### ✔️ 9.2 Prohibido usar sensores sin referencia

Debe existir un valor base.

### ✔️ 9.3 Prohibido usar sensores sin filtrado

Evita ruido.

### ✔️ 9.4 Validación obligatoria

- precisión

- estabilidad

- desviación

# ⭐ 10. Seguridad en salidas PWM

### ✔️ 10.1 Prohibido usar PWM sin documentación

Cada dispositivo tiene su frecuencia.

### ✔️ 10.2 Prohibido usar PWM sin protección

Evita sobrecalentamiento.

### ✔️ 10.3 Validación obligatoria

- frecuencia

- ciclo útil

- temperatura

# ⭐ 11. Seguridad en integración GPIO ↔ CNC‑CAT

### ✔️ 11.1 Prohibido conectar GPIO directamente al motor

Debe pasar por drivers.

### ✔️ 11.2 Prohibido usar GPIO para controlar elementos peligrosos

Ejemplo:

- husillo

- servos

- actuadores grandes

### ✔️ 11.3 Prohibido usar GPIO sin documentación

Cada pin debe tener función fija.

### ✔️ 11.4 Validación obligatoria

- señales

- ruido

- estabilidad

- sincronización

# ⭐ 12. Prohibiciones absolutas

- usar GPIO sin documentación

- usar GPIO sin etiquetar

- mezclar tensiones

- usar cables dañados

- usar sensores sin calibración

- usar salidas sin relé

- usar salidas sin protección

- ignorar ruido eléctrico

- ignorar alarmas

- operar sin validar

- operar sin registrar

# ⭐ 13. Objetivo final

Estas normas garantizan que GPIO en CNC‑CAT sea:

- seguro

- estable

- profesional

- industrial

- trazable

- confiable

Son las normas oficiales de seguridad GPIO del ecosistema CNC‑CAT.


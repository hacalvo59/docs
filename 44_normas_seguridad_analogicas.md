# 📘 **44\_normas\_seguridad\_analogicas.md**

**Normas oficiales de seguridad para señales analógicas — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad obligatorias** para instalar, cablear, integrar, calibrar y operar señales analógicas dentro del ecosistema CNC‑CAT, garantizando:

- seguridad del operador

- integridad del hardware

- precisión de lectura

- estabilidad del sistema

- cumplimiento industrial

Las señales analógicas son extremadamente sensibles. Un error puede provocar lecturas falsas, fallos de control o daños en hardware. Estas normas son **críticas** y deben cumplirse SIEMPRE.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 Las señales analógicas son vulnerables al ruido

Requieren blindaje, filtrado y distancias adecuadas.

### ✔️ 2.2 La calibración es obligatoria

Sin calibración → lecturas incorrectas → decisiones incorrectas.

### ✔️ 2.3 La alimentación debe ser estable

Variaciones → errores de medición.

### ✔️ 2.4 Solo personal cualificado puede manipular señales analógicas

No es un sistema plug‑and‑play.

# ⭐ 3. Tipos de señales analógicas cubiertas

### ✔️ 3.1 Entradas analógicas

- temperatura

- corriente

- presión

- vibración

- sensores lineales

- potenciómetros

### ✔️ 3.2 Salidas analógicas

- control de drivers

- control de actuadores

- control de velocidad externa

- señales de referencia

### ✔️ 3.3 Señales especiales

- 0–10V

- 4–20mA

- ±10V

- PWM filtrado

# ⭐ 4. Requisitos previos

Antes de trabajar con señales analógicas, el técnico debe:

- ser usuario con rol **técnico** o **administrador**

- revisar documentación del sensor o actuador

- revisar tensiones

- revisar corrientes

- revisar impedancias

- revisar blindaje

- revisar conectores

- revisar topología

# ⭐ 5. Equipo de protección personal (EPP)

Obligatorio:

- gafas de seguridad

- calzado de seguridad

Opcional según operación:

- guantes aislantes

# ⭐ 6. Seguridad en cableado analógico

### ✔️ 6.1 Prohibido cablear con la máquina energizada

Debe estar apagada y bloqueada (LOTO).

### ✔️ 6.2 Prohibido mezclar señales analógicas con digitales

Evita interferencias.

### ✔️ 6.3 Prohibido usar cables sin blindaje

El ruido eléctrico destruye la precisión.

### ✔️ 6.4 Prohibido usar cables largos sin compensación

Puede introducir caída de tensión.

### ✔️ 6.5 Prohibido usar cables dañados

Ni pelados, ni doblados, ni aplastados.

### ✔️ 6.6 Validación obligatoria

Después de cablear:

- continuidad

- polaridad

- tensión

- ruido

- estabilidad

# ⭐ 7. Seguridad en entradas analógicas

### ✔️ 7.1 Prohibido usar sensores sin calibración

Especialmente temperatura, corriente y presión.

### ✔️ 7.2 Prohibido usar sensores sin referencia

Debe existir un valor base.

### ✔️ 7.3 Prohibido usar sensores sin filtrado

Evita ruido eléctrico.

### ✔️ 7.4 Prohibido usar sensores fuera de rango

Evita saturación.

### ✔️ 7.5 Validación obligatoria

- precisión

- estabilidad

- desviación

- histéresis

# ⭐ 8. Seguridad en salidas analógicas

### ✔️ 8.1 Prohibido conectar cargas sin documentación

Cada actuador tiene su rango.

### ✔️ 8.2 Prohibido usar salidas sin protección

Evita sobrecorriente.

### ✔️ 8.3 Prohibido usar salidas sin filtrado

Evita oscilaciones.

### ✔️ 8.4 Prohibido usar salidas fuera de rango

Evita daños.

### ✔️ 8.5 Validación obligatoria

- corriente

- tensión

- temperatura

- estabilidad

# ⭐ 9. Seguridad en señales 4–20mA

### ✔️ 9.1 Prohibido abrir el circuito

Interrumpe la lectura.

### ✔️ 9.2 Prohibido mezclar sensores activos y pasivos

Cada uno requiere configuración distinta.

### ✔️ 9.3 Prohibido usar fuentes no certificadas

Evita ruido.

### ✔️ 9.4 Validación obligatoria

- 4mA (mínimo)

- 20mA (máximo)

- linealidad

# ⭐ 10. Seguridad en señales 0–10V y ±10V

### ✔️ 10.1 Prohibido usar señales sin referencia común

Debe existir GND compartido.

### ✔️ 10.2 Prohibido usar señales sin protección

Evita sobrevoltaje.

### ✔️ 10.3 Prohibido usar señales sin filtrado

Evita ruido.

### ✔️ 10.4 Validación obligatoria

- offset

- ganancia

- linealidad

# ⭐ 11. Seguridad en PWM filtrado

### ✔️ 11.1 Prohibido usar PWM sin filtro RC adecuado

Evita oscilaciones.

### ✔️ 11.2 Prohibido usar PWM sin frecuencia correcta

Cada dispositivo tiene su rango.

### ✔️ 11.3 Validación obligatoria

- frecuencia

- ciclo útil

- ripple

# ⭐ 12. Prohibiciones absolutas

- usar señales analógicas sin documentación

- usar sensores sin calibración

- mezclar señales analógicas con digitales

- mezclar tensiones

- usar cables sin blindaje

- ignorar ruido eléctrico

- ignorar desviaciones

- operar sin validar

- operar sin registrar

# ⭐ 13. Objetivo final

Estas normas garantizan que las señales analógicas en CNC‑CAT sean:

- seguras

- precisas

- profesionales

- industriales

- trazables

- confiables

Son las normas oficiales de seguridad para señales analógicas del ecosistema CNC‑CAT.


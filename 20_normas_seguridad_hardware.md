# 📘 **20\_normas\_seguridad\_hardware.md**

**Normas oficiales de seguridad para hardware — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad obligatorias** relacionadas con el hardware utilizado en máquinas controladas por CNC‑CAT, garantizando:

- integridad del equipo

- protección del operador

- prevención de fallos eléctricos

- prevención de daños mecánicos

- cumplimiento industrial

- operación segura y estable

Estas normas son **estrictas** y deben cumplirse SIEMPRE.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 El hardware debe ser seguro por diseño

Nada de improvisaciones, adaptadores inseguros o cableados temporales.

### ✔️ 2.2 La máquina debe poder detenerse en cualquier momento

E‑STOP físico obligatorio.

### ✔️ 2.3 Todo componente debe estar certificado

Servos, drivers, fuentes, sensores, cables, conectores.

### ✔️ 2.4 La instalación debe ser profesional

Nada de cables sueltos, empalmes, cinta aislante o terminales sin crimpar.

# ⭐ 3. Seguridad eléctrica

### ✔️ 3.1 Toma de tierra obligatoria

Toda la máquina debe estar correctamente conectada a tierra.

### ✔️ 3.2 Protección contra sobrecorriente

- magnetotérmicos

- fusibles

- relés de seguridad

### ✔️ 3.3 Separación de potencia y señal

Nunca mezclar:

- cables de servos

- cables de sensores

- cables de comunicación

### ✔️ 3.4 Evitar interferencias EMI

- cables apantallados

- ferritas

- rutas separadas

### ✔️ 3.5 Caja eléctrica cerrada

Nunca operar con el armario abierto.

# ⭐ 4. Seguridad mecánica

### ✔️ 4.1 Ejes libres de obstrucciones

Nada debe interferir con el movimiento.

### ✔️ 4.2 Tornillería apretada

Revisar periódicamente:

- guías

- husillos

- soportes

- acoples

### ✔️ 4.3 Herramientas correctamente fijadas

Nunca usar herramientas dañadas o mal sujetas.

### ✔️ 4.4 Puertas de seguridad

Si existen, deben estar cerradas durante la operación.

# ⭐ 5. Sensores y límites

### ✔️ 5.1 Homing switches obligatorios

Uno por eje.

### ✔️ 5.2 Limit switches obligatorios

En ambos extremos del recorrido.

### ✔️ 5.3 Sensores redundantes recomendados

Especialmente en máquinas grandes.

### ✔️ 5.4 Nunca deshabilitar límites

Ni por software ni por hardware.

# ⭐ 6. Servos y actuadores

### ✔️ 6.1 Servos industriales certificados

Nada de servos de hobby.

### ✔️ 6.2 Watchdog activo

Si un servo deja de responder → detener máquina.

### ✔️ 6.3 Encoder funcional

Sin encoder → sin movimiento.

### ✔️ 6.4 Refrigeración adecuada

Evitar sobrecalentamiento.

# ⭐ 7. Cableado

### ✔️ 7.1 Cables etiquetados

Cada cable debe tener su identificación.

### ✔️ 7.2 Cables ordenados

Uso obligatorio de:

- canaletas

- bridas

- pasacables

### ✔️ 7.3 Cables apantallados para señales

Especialmente:

- encoders

- EtherCAT

- sensores

### ✔️ 7.4 Evitar cables sueltos

Nada debe colgar o rozar partes móviles.

# ⭐ 8. EtherCAT

### ✔️ 8.1 NIC dedicada

Nunca compartir con internet.

### ✔️ 8.2 Cables industriales

Cat5e o Cat6 blindado.

### ✔️ 8.3 Topología lineal

Evitar bifurcaciones.

### ✔️ 8.4 Esclavos correctamente alimentados

Nunca alimentar desde USB o fuentes no certificadas.

# ⭐ 9. Refrigeración y ventilación

### ✔️ 9.1 Ventilación adecuada en el armario

Evitar acumulación de calor.

### ✔️ 9.2 Filtros limpios

Revisar mensualmente.

### ✔️ 9.3 Evitar polvo y virutas

Nunca permitir que entren en el armario eléctrico.

# ⭐ 10. Mantenimiento preventivo

### ✔️ 10.1 Revisiones periódicas

- tornillería

- cables

- sensores

- servos

- ventiladores

### ✔️ 10.2 Lubricación

Según especificaciones del fabricante.

### ✔️ 10.3 Sustitución de piezas desgastadas

Nunca operar con componentes dañados.

# ⭐ 11. Prohibiciones absolutas

- operar sin E‑STOP

- operar sin límites

- operar con cables sueltos

- operar con armario abierto

- operar con servos sin encoder

- operar con sensores desconectados

- operar con herramientas dañadas

- operar con vibraciones excesivas

- operar con fuentes no certificadas

# ⭐ 12. Objetivo final

Estas normas garantizan que el hardware utilizado con CNC‑CAT sea:

- seguro

- estable

- profesional

- industrial

- confiable

- duradero

Son las normas oficiales de seguridad para hardware en CNC‑CAT.


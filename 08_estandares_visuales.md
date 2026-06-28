# 📘 **08\_estandares\_visuales.md**

**Estándares visuales oficiales del ecosistema LINCAT / CNC‑CAT**

# ⭐ 1. Propósito

Definir un **estándar visual unificado** para:

- UI LINCAT

- documentación

- diagramas

- iconografía

- colores

- tipografías

- espaciados

- layouts

El objetivo es garantizar una **identidad visual industrial, moderna y coherente** en todo el ecosistema.

# ⭐ 2. Principios visuales

- **Claridad**: nada debe distraer al operador.

- **Jerarquía**: lo importante siempre visible.

- **Consistencia**: mismos colores, tamaños y patrones.

- **Ergonomía**: accesible para operadores reales.

- **Minimalismo industrial**: limpio, fuerte, sin ruido visual.

- **Internacionalización**: textos preparados para traducción.

# ⭐ 3. Paleta de colores oficial

### **Colores principales**

- **Azul industrial**: `\#1E88E5`

- **Gris oscuro**: `\#212121`

- **Gris medio**: `\#424242`

- **Gris claro**: `\#BDBDBD`

- **Blanco**: `\#FFFFFF`

### **Colores de estado**

- **OK / READY**: `\#4CAF50`

- **WARNING**: `\#FFC107`

- **ERROR**: `\#F44336`

- **ESTOP**: `\#B71C1C`

### **Colores de ejes**

- **X**: `\#E53935`

- **Y**: `\#43A047`

- **Z**: `\#1E88E5`

- **A/B/C**: tonos derivados

# ⭐ 4. Tipografía

### **Fuente principal**

- **Roboto** (UI y documentación)

### **Fuente monoespaciada**

- **Roboto Mono** (código, DRO, G‑code)

### **Tamaños recomendados**

- Títulos: 22–26 px

- Subtítulos: 18–20 px

- Texto normal: 14–16 px

- Código: 14 px

# ⭐ 5. Iconografía

### **Estilo**

- Líneas limpias

- Grosor uniforme

- Sin sombras

- Sin degradados

- Iconos simples y reconocibles

### **Iconos obligatorios**

- Jog

- Home

- Run / Pause / Stop

- Alarmas

- IO

- Herramientas

- Offsets

- Estado máquina

# ⭐ 6. Layout general de la UI LINCAT

### **Reglas**

- Paneles alineados

- Márgenes uniformes (16 px)

- Espaciado interno consistente

- Botones grandes y accesibles

- Indicadores siempre visibles

- DRO siempre en la parte superior

- Alarmas siempre visibles

### **Estructura recomendada**

Código

```
`┌──────────────────────────────┐`

`│            DRO               │`

`├───────────────┬──────────────┤`

`│   Movimiento   │   Programa   │`

`├───────────────┼──────────────┤`

`│   Offsets      │ Herramientas │`

`├───────────────┼──────────────┤`

`│   IO           │   Estado     │`

`└───────────────┴──────────────┘`
```

# ⭐ 7. Estándares para diagramas

### **Formato**

- ASCII limpio

- UML simple

- Sin colores

- Sin decoraciones

- Texto monoespaciado

### **Reglas**

- Flechas claras

- Jerarquía vertical

- Módulos bien separados

- Nombres oficiales

# ⭐ 8. Estándares para documentación visual

### **Capturas**

- Solo si aportan valor

- Resolución mínima 1080p

- Sin información personal

- Sin ruido visual

### **Diagramas**

- Siempre en bloques de código

- Siempre consistentes con la arquitectura oficial

# ⭐ 9. Estándares de interacción visual

### **Botones**

- Estados: normal, hover, disabled

- Colores según estado máquina

- Tamaño mínimo: 36 px

### **Indicadores**

- DRO actualizado en tiempo real

- Alarmas con color + texto

- Estado máquina con icono + texto

# ⭐ 10. Objetivo final

Garantizar que todo el ecosistema CNC‑CAT tenga una identidad visual:

- profesional

- industrial

- moderna

- clara

- consistente

- escalable


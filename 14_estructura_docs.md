# 📘 **14\_estructura\_docs.md**

**Estructura oficial de la documentación del ecosistema CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir la **estructura estándar** que deben seguir todos los documentos del ecosistema CNC‑CAT, garantizando:

- claridad

- consistencia

- profesionalismo

- mantenibilidad

- escalabilidad

- compatibilidad con MkDocs y PDF

Este archivo es la **columna vertebral** de toda la documentación.

# ⭐ 2. Estructura obligatoria de cada documento

Cada documento técnico debe seguir esta plantilla:

Código

```
`\# Título del documento`


`\#\# 1. Propósito`

`Explica por qué existe el documento.`


`\#\# 2. Contexto`

`Describe dónde encaja dentro del ecosistema.`


`\#\# 3. Contenido principal`

`Explicación detallada del tema.`


`\#\# 4. Diagramas`

`Diagramas ASCII o UML si aplica.`


`\#\# 5. Ejemplos`

`Casos prácticos, código, configuraciones.`


`\#\# 6. Reglas o estándares`

`Normas obligatorias relacionadas con el tema.`


`\#\# 7. Errores comunes`

`Lista de fallos típicos y cómo evitarlos.`


`\#\# 8. Relación con otros módulos`

`Documentos o módulos relacionados.`


`\#\# 9. Historial de cambios`

`Versión, fecha, autor.`
```

# ⭐ 3. Reglas generales de estructura

### ✔️ 3.1 Un documento = un tema

Nada de mezclar conceptos.

### ✔️ 3.2 Secciones numeradas

Siempre en formato:

Código

```
`1.`

`1.1`

`1.2`

`2.`

`2.1`
```

### ✔️ 3.3 Diagramas siempre en bloques de código

Nunca imágenes incrustadas.

### ✔️ 3.4 Ejemplos siempre funcionales

Nada de pseudocódigo ambiguo.

### ✔️ 3.5 Historial obligatorio

Cada documento debe indicar:

- versión

- fecha

- autor

# ⭐ 4. Estructura del repositorio de documentación

La documentación se organiza así:

Código

```
`C\_Pilot\_Docs/`

`│`

`├── 00\_portada/`

`├── 01\_introduccion/`

`├── 02\_arquitectura/`

`├── 03\_ui\_lincat/`

`├── 04\_motion\_api/`

`├── 05\_core/`

`├── 06\_drivers/`

`├── 07\_ethercat/`

`├── 08\_estandares\_visuales.md`

`├── 09\_estandares\_documentacion.md`

`├── 10\_glosario\_tecnico.md`

`├── 11\_modelo\_ramas.md`

`├── 12\_estandar\_commits.md`

`├── 13\_portada\_visual.md`

`└── 14\_estructura\_docs.md`
```

# ⭐ 5. Reglas para nombres de archivos

### ✔️ 5.1 Prefijo numérico obligatorio

Permite orden alfabético correcto.

### ✔️ 5.2 Snake case

Ejemplo:

Código

```
`14\_estructura\_docs.md`
```

### ✔️ 5.3 Nombres descriptivos

Nada de:

❌ `doc1.md` ❌ `misc.md` ❌ `varios.md`

# ⭐ 6. Reglas para títulos

### ✔️ Título en H1

Ejemplo:

Código

```
`\# Estructura de Documentación`
```

### ✔️ Sin emojis en títulos principales

Solo en secciones internas si aportan claridad.

# ⭐ 7. Reglas para diagramas

### ✔️ ASCII o UML

Ejemplo:

Código

```
`┌──────────────┐`

`│   UI LINCAT   │`

`└──────────────┘`
```

### ✔️ Sin colores

### ✔️ Sin imágenes externas

### ✔️ Sin dependencias gráficas

# ⭐ 8. Reglas para ejemplos

### ✔️ Código real

### ✔️ Configuraciones reales

### ✔️ Comandos reales

Ejemplo:

bash

```
`python3 main\_simulation.py`
```

# ⭐ 9. Historial de cambios

Cada documento debe terminar con:

Código

```
`\#\# Historial de cambios`

`- v1.0 — Junio 2026 — Creación del documento`
```

# ⭐ 10. Objetivo final

Garantizar que toda la documentación del ecosistema CNC‑CAT sea:

- clara

- profesional

- modular

- mantenible

- escalable

- industrial

Este archivo define **cómo debe escribirse todo lo demás**.


# ⭐ **15\_mkdocs\_estructura.md**

**Estructura completa para documentación web con MkDocs**

# **1. Objetivo**

Convertir toda la documentación del ecosistema LINCAT / CNC‑CAT en un sitio web profesional:

- navegación lateral,

- buscador,

- temas industriales,

- enlaces internos,

- estructura clara,

- publicación en GitHub Pages.

# **2. Estructura recomendada de MkDocs**

Código

```
`mkdocs.yml`

`docs/`

`    index.md`

`    portada.md`

`    roadmap.md`

`    arquitectura/`

`        diagrama\_general.md`

`        arquitectura\_ecosistema.md`

`        ciclo\_control.md`

`    maestro/`

`        00\_internacionalizacion.md`

`        01\_vision\_lincat.md`

`        02\_arquitectura\_ecosistema.md`

`        03\_diseno\_ui\_lincat.md`

`        04\_cnc\_cat\_motor.md`

`        05\_ethercat\_layer.md`

`        06\_plc\_integrado.md`

`        07\_cam\_blendercam.md`

`        08\_estandares\_visuales.md`

`        09\_estandares\_documentacion.md`

`        10\_glosario\_tecnico.md`

`    technical/`

`        core.md`

`        motion\_api.md`

`        ui\_lincat.md`

`        ethercat.md`

`        plc.md`

`        drivers.md`

`        simulation.md`

`        real\_engine.md`
```

# **3. Archivo mkdocs.yml (estructura)**

yaml

```
`site\_name: LINCAT / CNC‑CAT`

`theme:`

`  name: material`

`  language: es`

`  features:`

`    - navigation.sections`

`    - navigation.expand`

`    - navigation.top`

`    - search.suggest`

`    - search.highlight`


`nav:`

`  - Inicio: index.md`

`  - Portada: portada.md`

`  - Roadmap: roadmap.md`

`  - Arquitectura:`

`      - Diagrama general: arquitectura/diagrama\_general.md`

`      - Ecosistema: arquitectura/arquitectura\_ecosistema.md`

`      - Ciclo de control: arquitectura/ciclo\_control.md`

`  - Documento Maestro:`

`      - Internacionalización: maestro/00\_internacionalizacion.md`

`      - Visión LINCAT: maestro/01\_vision\_lincat.md`

`      - Arquitectura del ecosistema: maestro/02\_arquitectura\_ecosistema.md`

`      - Diseño UI LINCAT: maestro/03\_diseno\_ui\_lincat.md`

`      - Motor CNC‑CAT: maestro/04\_cnc\_cat\_motor.md`

`      - EtherCAT Layer: maestro/05\_ethercat\_layer.md`

`      - PLC integrado: maestro/06\_plc\_integrado.md`

`      - CAM / BlenderCAM: maestro/07\_cam\_blendercam.md`

`      - Estándares visuales: maestro/08\_estandares\_visuales.md`

`      - Estándares de documentación: maestro/09\_estandares\_documentacion.md`

`      - Glosario técnico: maestro/10\_glosario\_tecnico.md`

`  - Documentación técnica:`

`      - CORE: technical/core.md`

`      - Motion API: technical/motion\_api.md`

`      - UI LINCAT: technical/ui\_lincat.md`

`      - EtherCAT: technical/ethercat.md`

`      - PLC: technical/plc.md`

`      - Drivers: technical/drivers.md`

`      - Motor simulado: technical/simulation.md`

`      - Motor real: technical/real\_engine.md`
```

# **4. Archivos clave**

### **index.md**

Página principal del sitio web. Debe enlazar a:

- portada visual

- índice maestro

- diagrama general

- roadmap

### **portada.md**

Usa el contenido de `13\_portada\_visual.md`.

### **roadmap.md**

Usa el contenido de `12\_roadmap\_tecnico.md`.

# **5. Tema recomendado**

**Material for MkDocs** Industrial, limpio, moderno, perfecto para documentación técnica.

# **6. Publicación en GitHub Pages**

Estructura recomendada:

Código

```
`docs/ → contenido`

`mkdocs.yml → configuración`
```

Luego:

Código

```
`mkdocs gh-deploy`
```

# **7. Resultado final**

Un sitio web:

- profesional,

- navegable,

- con buscador,

- con estructura industrial,

- perfecto para presentar el ecosistema al mundo.


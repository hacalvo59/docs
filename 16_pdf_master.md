# 📘 **16\_pdf\_master.md**

**Documento maestro para generar el PDF completo del ecosistema LINCAT / CNC‑CAT**

# **1. Objetivo**

Este archivo define:

- el orden oficial del PDF,

- la estructura de capítulos,

- los títulos,

- los enlaces internos,

- y el contenido que debe incluirse.

Sirve como **índice maestro para Pandoc**.

# **2. Estructura del PDF**

El PDF final debe contener, en este orden:

## **Portada**

Usar el contenido de:

- `13\_portada\_visual.md`

## **Índice general**

Usar:

- `14\_indice\_maestro.md`

## **Parte I — Documento Maestro (00–10)**

1. `00\_internacionalizacion.md`

2. `01\_vision\_lincat.md`

3. `02\_arquitectura\_ecosistema.md`

4. `03\_diseno\_ui\_lincat.md`

5. `04\_cnc\_cat\_motor.md`

6. `05\_ethercat\_layer.md`

7. `06\_plc\_integrado.md`

8. `07\_cam\_blendercam.md`

9. `08\_estandares\_visuales.md`

10. `09\_estandares\_documentacion.md`

11. `10\_glosario\_tecnico.md`

## **Parte II — Documentación técnica (technical/)**

1. `technical/core.md`

2. `technical/motion\_api.md`

3. `technical/ui\_lincat.md`

4. `technical/ethercat.md`

5. `technical/plc.md`

6. `technical/drivers.md`

7. `technical/simulation.md`

8. `technical/real\_engine.md`

## **Parte III — Diagramas**

1. `diagrama\_general.md`

2. Diagramas UML (si los exportas a `.md` o `.png`)

3. Ciclo de control

4. Planner + interpolación

5. Parser G‑code

6. Estados y alarmas

7. Drivers + EtherCAT

8. UI LINCAT

*(Puedes añadirlos como imágenes o como texto ASCII.)*

## **Parte IV — Documentos estratégicos**

1. `readme/README.md`

2. `readme/README\_GITHUB.md`

3. `12\_roadmap\_tecnico.md`

# **3. Archivo maestro para Pandoc**

Guarda este archivo como:

Código

```
`pdf\_master.md`
```

Contenido:

markdown

```
`% LINCAT / CNC‑CAT  `

`% Plataforma Industrial Libre  `

`% 2026`


`\# Portada`

`!include 13\_portada\_visual.md`


`\# Índice Maestro`

`!include 14\_indice\_maestro.md`


`\# Parte I — Documento Maestro`

`!include 00\_internacionalizacion.md`

`!include 01\_vision\_lincat.md`

`!include 02\_arquitectura\_ecosistema.md`

`!include 03\_diseno\_ui\_lincat.md`

`!include 04\_cnc\_cat\_motor.md`

`!include 05\_ethercat\_layer.md`

`!include 06\_plc\_integrado.md`

`!include 07\_cam\_blendercam.md`

`!include 08\_estandares\_visuales.md`

`!include 09\_estandares\_documentacion.md`

`!include 10\_glosario\_tecnico.md`


`\# Parte II — Documentación Técnica`

`!include technical/core.md`

`!include technical/motion\_api.md`

`!include technical/ui\_lincat.md`

`!include technical/ethercat.md`

`!include technical/plc.md`

`!include technical/drivers.md`

`!include technical/simulation.md`

`!include technical/real\_engine.md`


`\# Parte III — Diagramas`

`!include diagrama\_general.md`


`\# Parte IV — Documentos Estratégicos`

`!include readme/README.md`

`!include readme/README\_GITHUB.md`

`!include 12\_roadmap\_tecnico.md`
```

# **4. Comando para generar el PDF**

Una vez tengas Pandoc y LaTeX instalados:

bash

```
`pandoc pdf\_master.md -o lincat\_cnc-cat\_documentacion.pdf --toc --pdf-engine=xelatex`
```

# **5. Resultado final**

Obtendrás un PDF:

- profesional,

- completo,

- con portada,

- con índice,

- con todo el ecosistema documentado,

- listo para entregar a empresas, partners o certificación.


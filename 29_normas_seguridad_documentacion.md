# 📘 **29\_normas\_seguridad\_documentacion.md**

**Normas oficiales de seguridad en documentación — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad, control, integridad y trazabilidad** aplicables a toda la documentación del ecosistema CNC‑CAT, garantizando:

- coherencia

- protección del conocimiento

- control de versiones

- trazabilidad

- integridad técnica

- cumplimiento industrial

Estas normas son **obligatorias** para cualquier documento del proyecto.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 La documentación es parte del sistema

Sin documentación fiable → no hay sistema fiable.

### ✔️ 2.2 La documentación debe ser coherente

Todo documento debe seguir los estándares oficiales.

### ✔️ 2.3 La documentación debe ser trazable

Cada cambio debe poder auditarse.

### ✔️ 2.4 La documentación debe ser segura

Nada de información crítica expuesta sin control.

# ⭐ 3. Control de versiones

### ✔️ 3.1 Uso obligatorio de Git

Toda documentación debe estar versionada.

### ✔️ 3.2 Ramas dedicadas

Los cambios en documentación deben hacerse en ramas:

Código

```
`docs/\<tema\>`
```

Ejemplos:

- `docs/seguridad`

- `docs/ui`

- `docs/ethercat`

### ✔️ 3.3 Commits claros

Formato obligatorio:

Código

```
`docs: descripción clara del cambio`
```

Ejemplo:

Código

```
`docs: añadir sección de offsets en UI LINCAT`
```

# ⭐ 4. Integridad del contenido

### ✔️ 4.1 Prohibido duplicar información

Cada concepto debe existir en un único documento.

### ✔️ 4.2 Prohibido contradicciones

Si un documento contradice otro → corregir inmediatamente.

### ✔️ 4.3 Prohibido contenido ambiguo

Todo debe ser:

- claro

- directo

- técnico

- verificable

### ✔️ 4.4 Prohibido contenido obsoleto

Si algo cambia en el sistema → actualizar documentación.

# ⭐ 5. Seguridad del conocimiento

### ✔️ 5.1 Documentación crítica protegida

Incluye:

- arquitectura

- Motion API

- drivers

- EtherCAT

- ciclo de control

- estados y alarmas

Debe estar en repositorios privados o con permisos controlados.

### ✔️ 5.2 Prohibido compartir documentación interna sin autorización

Especialmente:

- diagramas

- UML

- especificaciones

- protocolos

### ✔️ 5.3 Prohibido almacenar documentación en servicios no controlados

Nada de:

- Google Drive

- Dropbox

- servicios personales

# ⭐ 6. Estructura obligatoria

Toda documentación debe seguir:

- numeración

- secciones estándar

- formato Markdown

- diagramas en ASCII

- ejemplos reales

- historial de cambios

# ⭐ 7. Auditoría de documentación

### ✔️ 7.1 Registrar cambios críticos

Incluye:

- arquitectura

- Motion API

- drivers

- ciclo de control

- estados

- alarmas

### ✔️ 7.2 Revisiones periódicas

Revisión recomendada:

Código

```
`Cada 3 meses`
```

### ✔️ 7.3 Validación cruzada

Cada documento debe ser revisado por:

- autor

- revisor técnico

- revisor de estándares

# ⭐ 8. Seguridad en distribución

### ✔️ 8.1 Documentación pública

Solo:

- manual de usuario

- guía de instalación

- guía de operación

### ✔️ 8.2 Documentación interna

Incluye:

- arquitectura

- drivers

- EtherCAT

- ciclo

- planner

- interpolador

Debe permanecer privada.

### ✔️ 8.3 Documentación confidencial

Incluye:

- protocolos internos

- diagramas completos

- especificaciones de hardware

Acceso solo para administradores.

# ⭐ 9. Prohibiciones absolutas

- publicar documentación interna sin permiso

- almacenar documentación en servicios no controlados

- duplicar contenido

- mezclar documentación técnica con documentación de usuario

- usar formatos no estándar

- eliminar historial de cambios

- ignorar contradicciones

- documentar sin seguir estándares

# ⭐ 10. Objetivo final

Estas normas garantizan que la documentación CNC‑CAT sea:

- segura

- coherente

- profesional

- industrial

- mantenible

- trazable

Son las normas oficiales de seguridad en documentación del ecosistema CNC‑CAT.


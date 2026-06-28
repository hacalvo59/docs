# 📘 **SECURITY.md**

**Guía oficial de seguridad del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Este documento define las políticas de seguridad del proyecto:

- cómo reportar vulnerabilidades,

- cómo gestionarlas,

- cómo proteger el ecosistema,

- cómo mantener la integridad del código,

- cómo actuar ante incidentes.

El objetivo es garantizar que el ecosistema LINCAT / CNC‑CAT sea **seguro, confiable e industrial**.

# ⭐ 2. Alcance

Esta política aplica a:

- UI LINCAT

- CNC‑CAT Core

- Motion API

- Motores (sim/real)

- EtherCAT Layer

- PLC integrado

- Drivers

- Documentación

- Scripts y herramientas

# ⭐ 3. Reporte de vulnerabilidades

Si encuentras una vulnerabilidad:

1. **No abras un issue público.**

2. Envía un correo privado al mantenedor del proyecto:

Código

```
`security@lincat-industrial.org`
```

3. Incluye:

   - descripción del problema,

   - pasos para reproducir,

   - impacto potencial,

   - sugerencia de solución (si la tienes).

4. Recibirás respuesta en un máximo de **72 horas**.

# ⭐ 4. Tipos de vulnerabilidades cubiertas

- Ejecución remota de código

- Elevación de privilegios

- Acceso no autorizado

- Manipulación de IO

- Corrupción de memoria

- Fugas de información

- Problemas en EtherCAT Layer

- Problemas en PLC integrado

- Problemas en Motion API

- Problemas en drivers

- Problemas en UI LINCAT

- Problemas en simulación

# ⭐ 5. Proceso de gestión de vulnerabilidades

1. **Recepción**

   - Se recibe el reporte privado.

2. **Evaluación**

   - Se clasifica según severidad (Critical / High / Medium / Low).

3. **Reproducción**

   - Se verifica el problema en un entorno controlado.

4. **Mitigación**

   - Se desarrolla un parche.

5. **Validación**

   - Se prueba el parche en simulación y hardware real (si aplica).

6. **Publicación**

   - Se lanza una versión `PATCH` o `MINOR` según impacto.

7. **Divulgación responsable**

   - Se publica un aviso de seguridad.

# ⭐ 6. Política de divulgación responsable

- No se revelan vulnerabilidades antes de que exista un parche.

- No se publican exploits.

- No se exponen máquinas reales.

- No se compromete la seguridad de terceros.

# ⭐ 7. Seguridad del código

### **7.1 Reglas estrictas**

- No se aceptan dependencias inseguras.

- No se aceptan librerías sin mantenimiento.

- No se aceptan módulos sin revisión.

- No se aceptan PRs sin análisis de impacto.

### **7.2 Revisión obligatoria**

Todo PR debe ser revisado por al menos **1 mantenedor**.

# ⭐ 8. Seguridad en EtherCAT

- Validación estricta de PDO/SDO

- Comprobación de estados (INIT → PREOP → SAFEOP → OP)

- Watchdog activo

- Sincronización DC validada

- Protección ante pérdida de sincronía

- Protección ante fallos de servo

# ⭐ 9. Seguridad en PLC integrado

- Runtime determinista

- Aislamiento de memoria

- Validación de bytecode

- Protección ante loops infinitos

- Protección ante acceso ilegal a IO

# ⭐ 10. Seguridad en UI LINCAT

- No ejecutar código arbitrario

- No cargar scripts externos

- No permitir acceso directo al sistema

- Validación de entradas del usuario

# ⭐ 11. Seguridad en documentación

- No incluir credenciales

- No incluir rutas sensibles

- No incluir configuraciones privadas

- No incluir datos de máquinas reales

# ⭐ 12. Objetivo final

Garantizar que el ecosistema LINCAT / CNC‑CAT sea:

- seguro

- confiable

- industrial

- robusto

- preparado para producción


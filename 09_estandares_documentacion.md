# ⭐ **ESTÁNDARES DE DOCUMENTACIÓN — CNC‑CAT v1.0**

## **1. Propósito del documento**

Establecer un **estándar profesional, consistente y mantenible** para toda la documentación del ecosistema CNC‑CAT. La documentación es parte del código: *sin documentación, un módulo no está completo* .

## **2. Principios generales**

- **Claridad**: textos directos, sin ambigüedades.

- **Estructura fija**: todos los módulos siguen el mismo formato.

- **Modularidad**: cada archivo cubre un único tema.

- **Consistencia visual**: títulos, bloques, diagramas y listas con el mismo estilo.

- **Internacionalización**: textos preparados para traducción.

- **Profesionalismo industrial**: tono técnico, preciso y limpio.

## **3. Estructura obligatoria de cada documento**

Cada módulo del proyecto debe incluir, como mínimo:

- **Objetivo**

- **Diagrama de flujo**

- **Interfaces públicas**

- **Estados y eventos**

- **Limitaciones**

- **Plan de crecimiento**

Esta estructura aparece explícitamente en tu documento *visión-cnc-cat.md*.

## **4. Estándares de formato**

### **4.1 Encabezados**

- H1 para el título del documento.

- H2 para secciones principales.

- H3 para subsecciones.

- Nada de H4+ salvo casos excepcionales.

### **4.2 Código**

- Usar bloques triple backtick.

- Lenguaje especificado cuando corresponda (`python`, `json`, `bash`).

- No mezclar pseudocódigo con código real.

### **4.3 Diagramas**

- Preferencia por diagramas ASCII simples.

- UML siempre en bloques de texto monoespaciado.

- Diagramas deben ser **coherentes con la arquitectura oficial**.

### **4.4 Listas**

- Viñetas para conceptos.

- Listas numeradas para procesos o secuencias.

## **5. Estándares de contenido**

### **5.1 Tono**

- Técnico, directo, industrial.

- Sin adornos innecesarios.

- Sin opiniones personales.

### **5.2 Terminología**

- Usar siempre los nombres oficiales de módulos:

  - **CORE**, **simulation/**, **real/**, **drivers/**, **Motion API**, **UI LINCAT**, **Cycle**, etc.

- Evitar sinónimos que generen confusión.

### **5.3 Ejemplos**

- Siempre breves.

- Siempre funcionales.

- Nunca ficticios si pueden ser reales.

## **6. Estándares de organización del repositorio**

Los documentos se agrupan en:

- **index/** → índice maestro

- **readme/** → documentación de entrada

- **technical/** → documentación técnica por módulo

## **7. Estándares de actualización**

Cada documento debe indicar:

- Fecha de última modificación

- Versión del módulo

- Cambios relevantes (changelog breve)

## **8. Filosofía final**

La documentación es un **pilar del proyecto**. Es lo que permite que CNC‑CAT sea:

- mantenible,

- escalable,

- profesional,

- adoptable por fabricantes,

- traducible,

- y duradero.


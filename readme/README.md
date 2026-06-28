# **README — Ecosistema LINCAT / CNC‑CAT**

**Plataforma industrial libre para CNC, PLC, EtherCAT y CAM**

## **Visión general**

LINCAT y CNC‑CAT forman un ecosistema industrial moderno, modular y completamente libre, diseñado para:

- control CNC profesional,

- automatización mediante PLC integrado,

- comunicación en tiempo real con EtherCAT,

- flujo CAM → CNC completo,

- operación remota,

- UI moderna y multilingüe,

- arquitectura escalable y mantenible.

Este proyecto nace para convertirse en el **estándar mundial de automatización industrial en Linux**, sin firmware propietario, sin licencias por eje y con una arquitectura clara y profesional.

## **Arquitectura del ecosistema**

El ecosistema se organiza en capas:

Código

```
`UI LINCAT`

`    ↓`

`Motion API`

`    ↓`

`CNC‑CAT (core, sim, real)`

`    ↓`

`EtherCAT Layer`

`    ↓`

`PLC Integrado`

`    ↓`

`Drivers / Hardware`
```

Cada capa es independiente, modular y documentada.

## **Componentes principales**

### **UI LINCAT**

Interfaz humana del sistema. Incluye:

- ejecución CNC,

- offsets,

- herramientas,

- MDI,

- alarmas,

- PLC editor/debugger,

- EtherCAT topología,

- CAM preview,

- operación remota.

### **CNC‑CAT (Motor CNC)**

Motor CNC industrial moderno:

- parser G‑code,

- planner,

- interpolador,

- ciclo de control,

- estados,

- alarmas,

- simulación y motor real.

### **EtherCAT Layer**

Comunicación industrial en tiempo real:

- maestro EtherCAT,

- topología,

- diagnóstico,

- PDO/SDO,

- sincronización DC,

- mapeo de IO.

### **PLC Integrado**

PLC nativo con:

- editor ST,

- compilador,

- runtime determinista,

- debugger,

- acceso a IO EtherCAT,

- integración con CNC‑CAT.

### **CAM Integrado**

Flujo CAM → CNC:

- integración con BlenderCAM,

- postprocesador CNC‑CAT,

- simulación,

- vista previa 3D.

## **Documentación**

Toda la documentación oficial se encuentra en:

Código

```
`C\_Pilot\_Docs/`
```

Incluye:

- Documento Maestro (secciones 00–10)

- README maestro

- Índice general

- Documentación técnica del código

## **Roadmap**

### **v1.0 — Arquitectura completa**

✔ Documento Maestro ✔ Diseño UI ✔ Arquitectura CNC‑CAT ✔ EtherCAT Layer ✔ PLC Integrado ✔ CAM Integrado ✔ Glosario técnico

### **v2.0 — Implementación**

- Motor CNC completo

- EtherCAT master

- PLC runtime

- UI LINCAT v2

- Simulador CNC

- Postprocesador CAM

### **v3.0 — Industrialización**

- Panel táctil industrial

- Operación remota segura

- Integración con máquinas reales

- Certificación CE/ISO

## **Licencia**

El ecosistema es **100% libre**, orientado a uso industrial profesional, sin firmware propietario ni restricciones.

## **Objetivo final**

Crear la plataforma industrial libre más completa del mundo:

- CNC

- PLC

- EtherCAT

- CAM

- UI

- Simulación

- Documentación

- Estándares

Todo sobre Linux. Todo modular. Todo profesional.


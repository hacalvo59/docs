# 📘 **MAINTENANCE\_GUIDE.md**

**Guía oficial de mantenimiento del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Esta guía define **cómo mantener** el ecosistema en condiciones óptimas:

- mantenimiento del software

- mantenimiento del hardware

- mantenimiento del sistema EtherCAT

- mantenimiento del PLC

- mantenimiento de la UI

- mantenimiento de logs y diagnósticos

- mantenimiento preventivo y correctivo

El objetivo es garantizar un sistema **estable, seguro y duradero**.

# ⭐ 2. Mantenimiento del software

## **2.1 Actualización del ecosistema**

bash

```
`git pull origin main`

`pip install -r requirements.txt`
```

## **2.2 Limpieza de entornos**

bash

```
`rm -rf venv`

`python3 -m venv venv`

`pip install -r requirements.txt`
```

## **2.3 Regeneración de documentación**

bash

```
`mkdocs build`
```

## **2.4 Regeneración de PDF**

bash

```
`pandoc pdf\_master.md -o lincat\_cnc-cat\_documentacion.pdf --pdf-engine=xelatex`
```

# ⭐ 3. Mantenimiento del motor CNC‑CAT

## **3.1 Core**

- revisar planner

- revisar interpolador

- revisar modelos

- revisar estados

- revisar alarmas

## **3.2 Motion API**

- validar comandos

- validar respuestas

- validar errores

- validar integridad

## **3.3 Motores (sim/real)**

- actualizar configuraciones

- revisar parámetros

- revisar límites

- revisar homing

# ⭐ 4. Mantenimiento de EtherCAT

## **4.1 Comprobación de topología**

bash

```
`ethercat slaves`
```

## **4.2 Comprobación de estados**

bash

```
`ethercat state`
```

## **4.3 Comprobación de PDO**

bash

```
`ethercat pdos`
```

## **4.4 Reglas**

- todos los esclavos deben estar en `OP`

- sincronización DC debe estar estable

- watchdog debe estar activo

- no debe haber errores de PDO

# ⭐ 5. Mantenimiento del PLC integrado

## **5.1 Revisión del parser**

- sintaxis

- AST

- bytecode

## **5.2 Revisión del runtime**

- determinismo

- tiempos de ciclo

- acceso a IO

- temporizadores

## **5.3 Revisión del debugger**

- breakpoints

- inspección de variables

- ejecución paso a paso

# ⭐ 6. Mantenimiento de UI LINCAT

## **6.1 Revisión visual**

- paneles

- widgets

- iconos

- textos

- colores

## **6.2 Revisión funcional**

- señales/slots

- eventos

- estados

- alarmas

- comunicación con Motion API

## **6.3 Limpieza de caché**

Código

```
`~/.local/share/lincat/cache/`
```

# ⭐ 7. Mantenimiento de logs

## **7.1 Ubicaciones**

- motor: `/var/log/cnc-cat/engine.log`

- EtherCAT: `/var/log/cnc-cat/ethercat.log`

- UI: `~/.local/share/lincat/logs/`

## **7.2 Rotación**

bash

```
`logrotate /etc/logrotate.d/cnc-cat`
```

## **7.3 Limpieza**

bash

```
`rm -rf /var/log/cnc-cat/\*.old`
```

# ⭐ 8. Mantenimiento preventivo

## **8.1 Frecuencia**

- semanal

- mensual

- trimestral

## **8.2 Tareas**

- revisar límites

- revisar sensores

- revisar cables

- revisar conectores

- revisar armario eléctrico

- revisar ventilación

- revisar temperatura

# ⭐ 9. Mantenimiento correctivo

## **9.1 Procedimiento**

1. identificar problema

2. reproducir

3. aislar módulo

4. corregir

5. probar en simulación

6. probar en hardware

7. documentar

## **9.2 Reglas**

- nunca corregir sin reproducir

- nunca corregir sin test

- nunca corregir sin documentación

# ⭐ 10. Objetivo final

Garantizar que el ecosistema LINCAT / CNC‑CAT se mantenga:

- estable

- seguro

- industrial

- confiable

- duradero

- profesional


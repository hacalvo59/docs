# 📘 **DEPLOYMENT.md**

**Guía oficial de despliegue del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Esta guía define **cómo desplegar** el ecosistema en distintos entornos:

- desarrollo

- simulación

- hardware real

- producción industrial

El objetivo es garantizar un despliegue **seguro, reproducible y profesional**.

# ⭐ 2. Requisitos previos

## **2.1 Sistema operativo recomendado**

- Debian 12

- Ubuntu 22.04 LTS

- Kernel RT (solo producción)

## **2.2 Dependencias globales**

- Python 3.10+

- pip

- venv

- git

- Qt6 (PySide6)

- SOEM (si se usa EtherCAT real)

# ⭐ 3. Entorno de desarrollo

## **3.1 Crear entorno virtual**

bash

```
`python3 -m venv venv`

`source venv/bin/activate`
```

## **3.2 Instalar dependencias**

bash

```
`pip install -r requirements.txt`
```

## **3.3 Ejecutar UI LINCAT**

bash

```
`python3 lincat.py`
```

## **3.4 Ejecutar motor simulado**

bash

```
`python3 main\_simulation.py`
```

# ⭐ 4. Despliegue en simulación

## **4.1 Objetivo**

Probar todo el ecosistema sin hardware.

## **4.2 Componentes incluidos**

- UI LINCAT

- Motion API

- Motor simulado

- Planner

- Interpolador

- Estados y alarmas

## **4.3 Comando**

bash

```
`python3 main\_simulation.py`
```

## **4.4 Validaciones**

- homing simulado

- jog

- ejecución de G‑code

- alarmas virtuales

- IO virtual

# ⭐ 5. Despliegue en hardware real

## **5.1 Requisitos**

- EtherCAT Master operativo

- Drivers configurados

- Topología validada

- E‑STOP físico

- Límites mecánicos

- Armario eléctrico seguro

## **5.2 Comando**

bash

```
`sudo python3 main\_real.py`
```

## **5.3 Validaciones obligatorias**

- estados EtherCAT (INIT → OP)

- PDO/SDO correctos

- sincronización DC

- homing real

- límites físicos

- husillo

- sondas

# ⭐ 6. Despliegue en producción industrial

## **6.1 Requisitos**

- kernel RT

- watchdog hardware

- UPS

- armario certificado

- documentación completa

- pruebas HIL aprobadas

## **6.2 Pasos**

1. Congelar versión (`main`)

2. Generar ISO o instalador

3. Configurar servicios systemd

4. Activar logs persistentes

5. Validar ciclo 1 kHz

6. Validar seguridad

7. Sellar configuración

# ⭐ 7. Servicios systemd (opcional)

## **7.1 Motor real**

`/etc/systemd/system/cnc-cat.service`

Código

```
`\[Unit\]`

`Description=CNC-CAT Real Engine`

`After=network.target`


`\[Service\]`

`ExecStart=/usr/bin/python3 /opt/cnc-cat/main\_real.py`

`Restart=always`


`\[Install\]`

`WantedBy=multi-user.target`
```

## **7.2 UI LINCAT**

`/etc/systemd/system/lincat.service`

Código

```
`\[Unit\]`

`Description=LINCAT UI`

`After=cnc-cat.service`


`\[Service\]`

`ExecStart=/usr/bin/python3 /opt/lincat/lincat.py`

`Restart=always`


`\[Install\]`

`WantedBy=multi-user.target`
```

# ⭐ 8. Logs y diagnóstico

## **8.1 Logs del motor**

Código

```
`/var/log/cnc-cat/engine.log`
```

## **8.2 Logs de EtherCAT**

Código

```
`/var/log/cnc-cat/ethercat.log`
```

## **8.3 Logs de UI**

Código

```
`~/.local/share/lincat/logs/`
```

# ⭐ 9. Objetivo final

Garantizar que el ecosistema LINCAT / CNC‑CAT pueda desplegarse:

- en desarrollo,

- en simulación,

- en hardware real,

- en producción industrial,

de forma **segura, reproducible y profesional**.


# 📘 **NETWORKING\_GUIDE.md**

**Guía oficial de red y comunicaciones del ecosistema LINCAT / CNC‑CAT**

# **1. Propósito**

Esta guía define cómo configurar y mantener las comunicaciones del ecosistema:

- red del sistema

- comunicación UI ↔ Motion API

- comunicación Motion API ↔ Motores

- comunicación con EtherCAT

- comunicación con PLC

- puertos, sockets y protocolos

- seguridad de red

El objetivo es garantizar una red **estable, segura y determinista**, apta para uso industrial.

# ⭐ 2. Arquitectura de comunicaciones

El ecosistema LINCAT / CNC‑CAT utiliza una arquitectura de red híbrida:

Código

```
`UI LINCAT → Motion API → Motor (sim/real) → EtherCAT → Drivers → Hardware`
```

Cada capa tiene su propio canal de comunicación.

# ⭐ 3. Comunicación UI ↔ Motion API

## **3.1 Protocolo**

- TCP

- JSON estructurado

- Mensajes síncronos y asíncronos

## **3.2 Puerto por defecto**

yaml

```
`ui:`

`  port: 5555`
```

## **3.3 Reglas**

- la UI nunca accede al hardware

- la UI solo habla con Motion API

- Motion API valida todos los comandos

# ⭐ 4. Comunicación Motion API ↔ Motor

## **4.1 Protocolo**

- llamadas directas en memoria (Python)

- sin red

- sin sockets

- comunicación determinista

## **4.2 Razón**

- máxima velocidad

- mínima latencia

- cero jitter

# ⭐ 5. Comunicación Motor ↔ EtherCAT

## **5.1 Protocolo**

- EtherCAT (IEC 61158)

- PDO (Process Data Objects)

- SDO (Service Data Objects)

- DC Sync (Distributed Clocks)

## **5.2 Requisitos**

- NIC dedicada

- modo real‑time

- SOEM instalado

## **5.3 Comandos útiles**

bash

```
`ethercat slaves`

`ethercat pdos`

`ethercat sdos`

`ethercat state`
```

# ⭐ 6. Configuración de red para EtherCAT

## **6.1 NIC dedicada**

Ejemplo recomendado:

Código

```
`eth1 → EtherCAT`

`eth0 → Internet / UI`
```

## **6.2 Desactivar servicios innecesarios**

bash

```
`sudo systemctl stop NetworkManager`

`sudo systemctl disable NetworkManager`
```

## **6.3 Configurar NIC en modo real‑time**

bash

```
`sudo ethtool -C eth1 rx-usecs 0`

`sudo ethtool -C eth1 tx-usecs 0`
```

## **6.4 Desactivar ahorro de energía**

bash

```
`sudo ethtool -s eth1 wol d`
```

# ⭐ 7. Comunicación con PLC integrado

## **7.1 Protocolo**

- memoria compartida

- acceso seguro

- ciclo independiente

## **7.2 Reglas**

- PLC nunca bloquea el motor

- PLC nunca accede a hardware directamente

- PLC solo accede a IO virtualizado

# ⭐ 8. Puertos utilizados

| **Componente** | **Puerto** | **Protocolo** |
| :-: | :-: | :-: |
| **UI ↔ Motion API** | 5555 | TCP |
| **Diagnóstico** | 7777 | TCP |
| **Web docs (mkdocs serve)** | 8000 | HTTP |

# ⭐ 9. Seguridad de red

## **9.1 Reglas estrictas**

- nunca exponer Motion API a Internet

- nunca exponer EtherCAT a Internet

- nunca mezclar red industrial con red doméstica

- firewall obligatorio

## **9.2 Firewall recomendado**

bash

```
`sudo ufw allow 5555/tcp`

`sudo ufw allow 7777/tcp`

`sudo ufw enable`
```

## **9.3 Aislamiento**

- UI puede estar en otra máquina

- Motor debe estar en máquina dedicada

- EtherCAT debe estar en NIC exclusiva

# ⭐ 10. Diagnóstico de red

## **10.1 Latencia**

bash

```
`ping 192.168.1.10`
```

## **10.2 Jitter**

bash

```
`cyclictest -t1 -p99 -n -i1000`
```

## **10.3 Estado EtherCAT**

bash

```
`ethercat diag`
```

# ⭐ 11. Objetivo final

Garantizar que la red del ecosistema LINCAT / CNC‑CAT sea:

- estable

- determinista

- segura

- industrial

- confiable

- libre de jitter

- apta para producción


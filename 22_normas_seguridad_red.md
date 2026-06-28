# 📘 **22\_normas\_seguridad\_red.md**

**Normas oficiales de seguridad de red — CNC‑CAT / LINCAT**

# ⭐ 1. Propósito

Definir las **normas de seguridad de red** que deben cumplirse en cualquier instalación de CNC‑CAT, garantizando:

- aislamiento de la máquina

- protección contra accesos no autorizados

- integridad del sistema

- prevención de ataques externos

- cumplimiento industrial

Estas normas son **obligatorias** en entornos profesionales.

# ⭐ 2. Principios fundamentales

### ✔️ 2.1 La máquina CNC debe estar aislada

Nunca debe estar expuesta a internet.

### ✔️ 2.2 EtherCAT requiere red dedicada

No se comparte con otros servicios.

### ✔️ 2.3 Todo acceso remoto debe ser autenticado

Nada de accesos abiertos.

### ✔️ 2.4 La red debe ser predecible y estable

Sin DHCP, sin cambios dinámicos.

# ⭐ 3. Aislamiento de red

### ✔️ 3.1 Red física separada

La máquina debe tener su propia red:

Código

```
`\[PC CNC\] — \[Switch industrial\] — \[Esclavos EtherCAT\]`
```

### ✔️ 3.2 Prohibido conectar la red CNC a internet

Ni directa ni indirectamente.

### ✔️ 3.3 Prohibido Wi‑Fi

Toda comunicación debe ser cableada.

# ⭐ 4. Configuración de red del PC CNC

### ✔️ 4.1 NIC dedicada para EtherCAT

Nunca compartir con:

- internet

- red corporativa

- servicios de archivos

### ✔️ 4.2 IP fija

Ejemplo recomendado:

Código

```
`192.168.7.1`
```

### ✔️ 4.3 Sin DHCP

Todo debe ser estático.

# ⭐ 5. Seguridad en EtherCAT

### ✔️ 5.1 Cables industriales

Cat5e/Cat6 blindado.

### ✔️ 5.2 Topología lineal

Evitar bifurcaciones.

### ✔️ 5.3 Sin switches intermedios

EtherCAT va directo.

### ✔️ 5.4 Supervisión de watchdog

Si un esclavo no responde → detener máquina.

# ⭐ 6. Acceso remoto seguro

### ✔️ 6.1 Prohibido acceso remoto sin autenticación

Nunca permitir:

- VNC abierto

- SSH sin contraseña

- Escritorio remoto sin PIN

### ✔️ 6.2 Acceso remoto solo por VPN

Y solo en entornos controlados.

### ✔️ 6.3 Logs obligatorios

Registrar:

- IP

- hora

- usuario

- acciones

# ⭐ 7. Firewall obligatorio

### ✔️ 7.1 Bloquear todo excepto lo necesario

Reglas mínimas:

- permitir EtherCAT

- permitir UI local

- bloquear todo lo demás

### ✔️ 7.2 Prohibido exponer puertos

Nada de:

- 22

- 3389

- 5900

- 8000+

### ✔️ 7.3 Sin servicios innecesarios

Deshabilitar:

- Samba

- FTP

- HTTP

- mDNS

# ⭐ 8. Seguridad en la Motion API

### ✔️ 8.1 No exponer Motion API a la red

Debe ser local.

### ✔️ 8.2 Validar origen de comandos

Solo UI local.

### ✔️ 8.3 Prohibido ejecutar comandos remotos sin autenticación

# ⭐ 9. Seguridad en actualizaciones

### ✔️ 9.1 Actualizaciones solo desde medios confiables

USB verificado o repositorio interno.

### ✔️ 9.2 Prohibido actualizar desde internet

Nunca.

### ✔️ 9.3 Verificación de integridad

Checksum obligatorio.

# ⭐ 10. Seguridad física de la red

### ✔️ 10.1 Armario eléctrico cerrado

Evitar accesos no autorizados.

### ✔️ 10.2 Cables protegidos

Nada debe poder desconectarse accidentalmente.

### ✔️ 10.3 Etiquetado obligatorio

Cada cable debe estar identificado.

# ⭐ 11. Prohibiciones absolutas

- conectar la máquina a internet

- usar Wi‑Fi

- usar DHCP

- exponer puertos

- permitir acceso remoto sin autenticación

- mezclar red CNC con red corporativa

- usar cables no blindados

- usar switches domésticos

- permitir Motion API remota

# ⭐ 12. Objetivo final

Estas normas garantizan que la red CNC‑CAT sea:

- segura

- aislada

- estable

- profesional

- industrial

- confiable

Son las normas oficiales de seguridad de red del ecosistema CNC‑CAT.


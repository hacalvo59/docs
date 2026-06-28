# 📘 **FAQ.md**

**Preguntas frecuentes del ecosistema LINCAT / CNC‑CAT**

# ⭐ **1. ¿Qué es CNC‑CAT?**

CNC‑CAT es un motor CNC moderno, modular e industrial diseñado desde cero para:

- ser claro

- ser estable

- ser extensible

- ser profesional

- funcionar con EtherCAT

- integrarse con UI LINCAT

# ⭐ **2. ¿Qué es LINCAT?**

LINCAT es la **interfaz humana** del ecosistema CNC‑CAT:

- moderna

- modular

- rápida

- profesional

- construida en Python + Qt6

# ⭐ **3. ¿Qué es la Motion API?**

Es la **interfaz universal** entre:

- UI LINCAT

- motor simulado

- motor real

Permite intercambiar motores sin tocar la UI.

# ⭐ **4. ¿Puedo usar CNC‑CAT sin hardware?**

Sí. El motor simulado permite:

- ejecutar G‑code

- probar la UI

- validar la Motion API

- depurar estados y alarmas

Todo sin hardware real.

# ⭐ **5. ¿Qué hardware necesito para usar EtherCAT?**

- NIC dedicada (Intel i210 recomendada)

- drivers EtherCAT

- servos industriales

- sensores de homing y límites

- armario eléctrico seguro

# ⭐ **6. ¿Qué lenguajes soporta el PLC integrado?**

El PLC integrado soporta:

- **Structured Text (ST)**

- parser propio

- AST propio

- bytecode propio

- runtime determinista

# ⭐ **7. ¿Cómo ejecuto el motor simulado?**

bash

```
`python3 main\_simulation.py`
```

# ⭐ **8. ¿Cómo ejecuto el motor real?**

bash

```
`sudo python3 main\_real.py`
```

# ⭐ **9. ¿Cómo inicio la UI LINCAT?**

bash

```
`python3 lincat.py`
```

# ⭐ **10. ¿Qué sistema operativo se recomienda?**

- Debian 12

- Ubuntu 22.04 LTS

- Kernel RT para producción

# ⭐ **11. ¿Qué hago si el homing falla?**

Revisar:

- sensores

- límites

- wiring

- PDO EtherCAT

- alarmas activas

# ⭐ **12. ¿Qué hago si EtherCAT no pasa a OP?**

Revisar:

- PDO

- SDO

- sincronización DC

- cableado

- alimentación

# ⭐ **13. ¿Qué hago si la UI no arranca?**

- reinstalar dependencias

- borrar caché

- revisar PySide6

# ⭐ **14. ¿Cómo actualizo el sistema?**

bash

```
`git pull origin main`

`pip install -r requirements.txt`
```

# ⭐ **15. ¿Cómo genero la documentación?**

bash

```
`mkdocs build`
```

# ⭐ **16. ¿Cómo genero el PDF?**

bash

```
`pandoc pdf\_master.md -o lincat\_cnc-cat\_documentacion.pdf`
```

# ⭐ **17. ¿Cómo reporto un bug?**

1. reproducir

2. aislar

3. documentar

4. abrir issue

5. incluir logs

# ⭐ **18. ¿Cómo contribuyo al proyecto?**

Seguir:

- CONTRIBUTING.md

- CODE\_STYLE.md

- DOC\_STYLE.md

- BRANCHING\_MODEL.md

# ⭐ **19. ¿Qué hago si el servo se mueve de forma brusca?**

Revisar:

- interpolador

- planner

- parámetros del servo

- jitter EtherCAT

# ⭐ **20. ¿Qué hago si aparece una alarma?**

1. leer descripción

2. revisar módulo afectado

3. corregir causa

4. limpiar alarma

5. repetir operación

# ⭐ **Objetivo final**

Este FAQ permite:

- resolver dudas rápidas

- entender el ecosistema

- operar con seguridad

- trabajar con profesionalidad


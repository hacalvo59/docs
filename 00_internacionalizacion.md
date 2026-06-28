# **00 — Internacionalización y Alcance Global**

## **0.1 Propósito de la internacionalización**

LINCAT nace como un ecosistema industrial global. Su objetivo es ser utilizado por ingenieros, operadores, integradores, fabricantes y desarrolladores de todo el mundo. Por ello, la internacionalización (i18n) no es un añadido posterior: **es un pilar fundamental del diseño desde su origen.**

## **0.2 Idiomas oficiales del proyecto**

La documentación y la UI se publicarán inicialmente en:

- Alemán

- Inglés

- Francés

- Italiano

- Chino (simplificado)

- Español

Estos idiomas representan los principales mercados industriales del planeta.

## **0.3 Alcance de la internacionalización**

La internacionalización abarca:

- Interfaz gráfica (UI)

- Documentación técnica

- Manuales de usuario

- Diagramas UML

- Mensajes del sistema

- Alarmas y códigos de error

- Logs y eventos

- PLC (editor, runtime, debugger)

- EtherCAT (diagnóstico, topología)

- CAM integrado

## **0.4 Reglas de diseño multilingüe**

Para garantizar consistencia visual y funcional:

- Ningún texto estará embebido en el código.

- Todos los textos se gestionarán mediante archivos externos de traducción.

- La UI debe adaptarse a longitudes variables (alemán largo, chino corto).

- Iconografía ISO 7000 / IEC 60417.

- Colores según IEC 60204‑1.

- Mensajes críticos: código + texto traducible.

- Manual maestro redactado primero en inglés.

## **0.5 Glosario técnico internacional**

Se creará un glosario maestro con equivalencias exactas para todos los idiomas soportados. Será obligatorio para:

- Estados

- Alarmas

- Terminología CNC

- Terminología EtherCAT

- Terminología PLC

- Terminología CAM

- Elementos UI

## **0.6 Objetivo final**

Garantizar que LINCAT pueda ser adoptado como **estándar mundial de automatización industrial en Linux**, sin barreras idiomáticas ni culturales, con una experiencia profesional uniforme en cualquier país.


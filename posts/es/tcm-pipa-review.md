---
id: "tcm-pipa-review"
title: "PIPA Review: Practical IoT Pentest Associate 2026"
author: "gorka-vila-perez"
publishedDate: 2026-04-07
updatedDate: 2026-04-07
image: ""
description: "Reseña de la certificación Practical IoT Pentest Associate (PIPA) de TCM Security, con la estructura del examen, el contenido del curso y mi experiencia personal."
categories:
  - "certifications"
draft: false
featured: false
lang: "es"
---

Siempre me ha llamado la atención el mundo del IoT porque mezcla dos áreas que por separado ya son interesantes, como la electrónica y las redes, y juntas abren bastantes frentes desde el punto de vista de la seguridad. Eso fue lo que me animó a sacarme la certificación **Practical IoT Pentest Associate (PIPA)**, que antes se llamaba Practical Junior IoT Tester o PJIT. Cambió el nombre, pero el contenido sigue siendo el mismo.

![Insignia PIPA de TCM Security](https://api.accredible.com/v1/frontend/credential_website_embed_image/certificate/161911026)

El pentesting en entornos IoT sigue siendo un nicho más reciente que el pentesting web o de aplicaciones tradicional, pero cada vez tiene más peso. Cada día se despliegan más dispositivos conectados, y muchos de ellos manejan datos sensibles con medidas de seguridad bastante pobres. Si te interesa empezar en seguridad IoT, creo que tiene bastante sentido hacerlo desde una base sólida.

Para preparar el examen, TCM ofrece el curso **Beginner's Guide to IoT and Hardware Hacking**, donde se tratan temas como:

- Fundamentos de electrónica: ley de Ohm, leyes de Kirchhoff, circuitos en serie y paralelo, condensadores, inductores, diodos, transistores, analizadores lógicos y UART
- Reconocimiento, enumeración y OSINT: arquitectura IoT, sistemas embebidos, UART
- Extracción y análisis de firmware: SPI, inspección de firmware, extracción manual e ingeniería inversa

Gran parte de ese contenido se puede encontrar repartido entre blogs, vídeos y tutoriales sueltos, pero aquí la ventaja está en que todo sigue un orden lógico y resulta fácil de seguir. En lugar de ir saltando de una fuente a otra, tienes una ruta de aprendizaje bastante bien hilada. Además, Andrew explica los conceptos con claridad y ofrece varias formas de contacto, algo que se agradece si te surge alguna duda durante el curso.

El curso completo está disponible en YouTube aquí:

[Beginner's Guide to IoT and Hardware Hacking](https://www.youtube.com/watch?v=j8SqZLr64NA)

- [Electrónica (mi experiencia)](#electrónica-mi-experiencia)
- [Equipamiento: opcional, pero lo recomiendo](#equipamiento-opcional-pero-lo-recomiendo)
- [La parte divertida: extraer e inspeccionar el firmware](#la-parte-divertida-extraer-e-inspeccionar-el-firmware)
- [Formato del examen (¡importante!)](#formato-del-examen-importante)
- [Dificultad y requisitos previos](#dificultad-y-requisitos-previos)
- [Mi valoración general](#mi-valoración-general)

## Electrónica (mi experiencia)

La parte de fundamentos de electrónica está pensada para gente que parte de cero o casi de cero. En mi caso, al venir de una formación técnica, esta sección me sirvió más como repaso que como contenido nuevo, pero aun así no está de más volver a los conceptos básicos de vez en cuando.

## Equipamiento: opcional, pero lo recomiendo

Comprar el material del curso no es obligatorio, pero si puedes permitírtelo, merece bastante la pena. La parte práctica ayuda mucho a fijar conceptos y hace que el aprendizaje sea más entretenido. Además, cuando montas cosas por tu cuenta siempre acabas equivocándote en algo, y normalmente es justo ahí donde más aprendes.

Si haces el curso sin el material, la sensación es un poco la de estar viendo a otra persona trastear con hardware en lugar de hacerlo tú. Sigue siendo útil, pero se pierde parte de la gracia.

## La parte divertida: extraer e inspeccionar el firmware

Cuando empiezas a trabajar con las herramientas, te das cuenta de lo relativamente sencillo que puede llegar a ser extraer información de un dispositivo. En el curso utilizan un router TP-Link, y tanto la captura de logs de arranque por **UART** como la extracción del firmware por **SPI** con cables jumper se sienten muy prácticas y satisfactorias. Es justo el tipo de habilidad que puede marcar la diferencia cuando te enfrentas a un pentest con componentes de hardware.

## Formato del examen (¡importante!)

Si te preguntas cómo puede ser el examen al haber componentes hardware de por medio, la respuesta es muy sencilla: el examen se centra sobre todo en la parte de **Ingeniería Inversa de Firmware**.

Te dan acceso a una máquina virtual con **capturas del analizador lógico** y **firmware ya extraído**, y a partir de ahí tienes que identificar vulnerabilidades usando **PulseView** y **Ghidra**, dos herramientas que se trabajan durante el curso. Además, el examen aporta contexto sobre el sistema para que entiendas cómo encaja el dispositivo dentro de un entorno IoT más amplio y qué fugas de información tendrían realmente impacto o no.

El examen dura **4 días en total**:

- **Los 2 primeros días:** búsqueda de vulnerabilidades en la máquina virtual
- **Los 2 últimos días:** redacción del informe

Algo que me sorprendió bastante es que terminé dedicando **más tiempo al informe** que a la parte técnica del examen. Si localizas rápido las vulnerabilidades principales, seguramente tengas ya suficiente para aprobar y te compense pasar antes a la fase de reporte, pero hay una pega importante: **una vez cambias a la fase de redacción, ya no puedes volver atrás**. Por eso merece mucho la pena documentarlo todo bien desde el principio: comandos, capturas, evidencias y cualquier detalle relevante.

Para el informe facilitan una plantilla y unas pautas bastante claras sobre lo que esperan ver. En mi caso, preparé mi propia base justo antes del examen y la adapté a esos requisitos. Gracias a eso pude perder menos tiempo con el formato y centrarme más en el contenido.

Consejo: yo usé SysReptor, que es una herramienta muy buena para escribir informes de pentesting. Tiene un montón de funcionalidades que facilitan el proceso, y es gratuita para uso individual. Puedes echarle un vistazo aquí: [SysReptor](https://docs.sysreptor.com/).

## Dificultad y requisitos previos

Más allá del contenido, una de las cosas que más suele pesar al decidir si merece la pena una certificación es la dificultad. En este caso, yo diría que PIPA encaja bastante bien como una **certificación de entrada** para empezar en hardware hacking y seguridad IoT. No hace falta tener una experiencia previa fuerte en electrónica o hardware.

Eso sí, venir con cierta soltura en **Linux** y con unos mínimos de **informática** ayuda bastante, sobre todo en la parte de ingeniería inversa de firmware, donde vas a encontrarte con código en C. La parte buena es que el propio curso cubre lo necesario para llegar al examen con garantías, así que no hace falta estudiar mucho más por tu cuenta salvo que quieras profundizar.

## Mi valoración general

Si buscas una forma estructurada y asequible de empezar en **seguridad IoT**, PIPA me parece un muy buen comienzo. Eso sí, conviene rebajar las expectativas ya que no es un curso centrado en protocolos inalámbricos de IoT, sino más bien en interfaces hardware y análisis de firmware.

En conjunto, el contenido está bien planteado, el examen es práctico y bastante alineado con situaciones reales, y como primera toma de contacto creo que funciona muy bien. Si te interesa la seguridad en IoT, es una certificación que puede ayudarte a empezar con buen pie y a ganar confianza trabajando con hardware.

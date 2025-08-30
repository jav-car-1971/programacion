---
title: "Instalando Linux Mint en Máquina Virtual"
date: 2025-08-30
draft: false
tags:
- linux
- linux mint
- virtualbox
---
Con el objetivo de preparar un entorno de escritorio aislado para testeos y desarrollo, descartamos las versiones, Cinnamon y MATE a favor de XFCE por su bajo consumo de recursos.

Después de descargar el ISO desde la página oficial y una vez configurada la máquina virtual asignándole los recursos necesarios, comenzamos la instalación:

![Paso 1 de la instalación](001.png)

Al arrancar la máquina, VirtualBoxVM te vuelve a pedir la dirección del ISO.

![Paso 2 de la instalación](002.png)

Una vez aclarado ese punto, la máquina arranca en modo LIVE.

![Paso 3 de la instalación](003.png)

El menu ofrece seleccionar el idioma.

![Paso 4 de la instalación](004.png)

La distribuciòn de teclado de preferencia del usuario. Elijo UK porque alguna vez, con alguna distribución, tuve problemas de compatibilidad.

![Paso 5 de la instalación](005.png)

Lo que viene después asusta un poco, si no fuera porque es una máquina virtual y no hay nada que borrar porque justamente es un entorno totalmente aislado.

![Paso 6 de la instalación](006.png)

La zona horaria

![Paso 7 de la instalación](007.png)

El nombre del usuario y el password. Este paso es importante, para tener algún control sobre algunos comandos "sudo".

![Paso 8 de la instalación](008.png)

En pocos minutos, el sistema operativo está instalado y la máquina funcionando.

![Paso 9 de la instalación](009.png)

Hay que confirmar que se borre el medio de instalación. Eso no borra el ISO original, ya que estaba fuera de la carpeta asignada a la máquina virtual, por lo que queda disponible en su carpeta para seguir utilizándolo.

![Paso 10 de la instalación](011.png)

Linux Mint te pide la contraseña para arrancar.

Te da la bienvenida.

Y listo.

Tratándose en este caso de una máquina virtual, no hay que olvidar que para que el teclado pueda operar fuera de la máquina virtual, debe presionarse una vez la tecla control de la derecha solamente.

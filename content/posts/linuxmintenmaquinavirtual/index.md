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

{{< figure src="001.png" title="Configuración de la máquina virtual" >}}

Al arrancar la máquina, VirtualBoxVM te vuelve a pedir la dirección del ISO.

{{< figure src="002.png" title="Solicitud de dirección del ISO" >}}

Una vez aclarado ese punto, la máquina arranca en modo LIVE.

{{< figure src="003.png" title="Menú de instalación en modo LIVE" >}}

El menu ofrece seleccionar el idioma.

{{< figure src="004.png" title="Selección de idioma" >}}

La distribuciòn de teclado de preferencia del usuario. Elijo UK porque alguna vez, con alguna distribución, tuve problemas de compatibilidad.

{{< figure src="005.png" title="Selección de teclado" >}}

Lo que viene después asusta un poco, si no fuera porque es una máquina virtual y no hay nada que borrar porque justamente es un entorno totalmente aislado.

{{< figure src="006.png" title="Tipo de instalación" >}}

La zona horaria.

{{< figure src="007.png" title="Selección de zona horaria" >}}

El nombre del usuario y el password. Este paso es importante, para tener algún control sobre algunos comandos "sudo".

{{< figure src="008.png" title="Creación de usuario y password" >}}

En pocos minutos, el sistema operativo está instalado y la máquina funcionando.

{{< figure src="009.png" title="Proceso de instalación" >}}

Hay que confirmar que se borre el medio de instalación. Eso no borra el ISO original, ya que estaba fuera de la carpeta asignada a la máquina virtual, por lo que queda disponible en su carpeta para seguir ustilizándolo.

{{< figure src="011.png" title="Confirmación de borrado de medio" >}}

Linux Mint te pide la contraseña para arrancar.

Te da la bienvenida.

Y listo.

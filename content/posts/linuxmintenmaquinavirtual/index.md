--- 
title: "Instalando Linux Mint en Máquina Virtual"
date: 2025-08-30
draft: false 
tags: 
- linux 
- linux mint 
- virtualbox 
---
Con el objetivo de preparar un entorno de escritorio aislado para testeos y desarollo, descartamos las versiones, Cinnamon y MATE a favor de XFCE por su bajo consumo de recursos,.

Despuès de descargar el ISO
**ISO** desde la página oficial y una vez configurada la máquina virtual asignándole los recursos necesarios, comenzamos la instalación:

![[Pasted image 20250830131549.png]]

![[Pasted image 20250830132158.png]]

Al arrancar la máquina, VirtualBoxVM te vuelve a pedir la dirección del ISO. 

Una vez aclarado ese punto, la máquina arranca en modo LIVE

![[Pasted image 20250830132557.png]]

El menu ofrece seleccionar el idioma.

![[Pasted image 20250830132850.png]]

La distribucciòn de teclado de preferencia del usuario. Elijo UK porque alguna vez, con alguna distribución, tuve problemas de compatibilidad.

![[Pasted image 20250830133050.png]]
    
Lo que viene después asusta un poco, si no fuera porque es una máquina virtual y no hay nada que borrar porque justamente es un entorno totalmente aislado.

![[Pasted image 20250830133253.png]]


La zona horaria

![[Pasted image 20250830133402.png]]


El nombre del usuario y el password. Este paso es importante, para tener algún control sobre algunos comandos "sudo". 

![[Pasted image 20250830133444.png]]


![[Pasted image 20250830133559.png]]

En pocos minutos, el sistema operativo está instalado y la máquina funcionando.

![[Pasted image 20250830134941.png]]

Hay que confirmar que se borre el medio de instalación. Eso no borra el ISO original, ya que estaba fuera de la carpeta asignada a la máquina virtual, por lo que queda disponible en su carpeta para seguir ustilizándolo


![[Pasted image 20250830135426.png]]

Linux Mint te pide la contraseña para arrancar

![[Pasted image 20250830135540.png]]

Te da la bienvenida.

![[Pasted image 20250830135720.png]]


Y listo.

![[Pasted image 20250830135838.png]]

Tratándose en este caso de una máquina virtual, no hay que olvidar que para que el teclado pueda operar fuera de la máquina virtual, debe presionarse una vez la tecla control de la derecha solamente. 

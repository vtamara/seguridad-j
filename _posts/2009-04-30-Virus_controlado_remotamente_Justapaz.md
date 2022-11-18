---
title:  "Virus Controlado Remotamente Justapaz"
header:
  teaser: "/assets/images/500x300.png"
categories: 
  - Seguridad
tags:
  - seguridad
---


Como se narra en [Virus Spam Justapaz], por un reporte del servidor de correo en listas negras de Spam se detectaron en la red interna de Justapaz el 10.Abr.2008:

* Un computador con Windows XP y un virus que enviaba el SPAM
* Un computador con Windows XP que hacia conexiones extrañas e intercambiaba información.
* Posteriormente este virus apareció en otros dos computadores. 

Aunque esos computadores tenían antivirus actualizados, estos no detectaban los virus que estaban produciendo ese tráfico. De hecho el segundo virus no pudo ser detectado con los mejores y más recientes antivirus de ese momento ---pues uno de los computadores fue llevado para analizarlo por una persona experta en soporte Windows.

Algunas características que encontramos fueron:
* El virus intentaba resolver crank.yourtrap.com (que resolvió a diversas IPs en los días que se analizó) y conectarse enviando información al parecer encriptada.
* El intento de conexión a crank.yourtrap.com lo hacía permanentemente, desde que arrancaba el computador.
* Cuando ocurrió el evento, se buscó en Internet sobre el asunto sin éxito. (hoy en día hay un par de reportes)

Al no encontrar solución, tuvieron que aislarse de la red estos computadores mientras fueron formateados.

En resumidas cuentas se trataba de un proceso que se ejecutaba desde el arranque, que enviaba información a un sitio en Internet y tal vez podía también recibir ordenes, es decir posiblemente el atacante tenía control total del computador.   

Según dos reportes que hoy en día están disponibles en Internet al respecto:
* http://www.prevx.com/filenames/2549894302369767251-X1/89356402.EXE.html
* http://www.threatexpert.com/report.aspx?uid=3643d776-7f11-416a-9834-d0cfa540260b
este virus se conecta a un servidor IRC ---desde el cual podría controlarse.

A raíz de este problema se propuso migración paulatina a Linux Ubuntu.

Esta información se cede al dominio público. 2009. vtamara@pasosdeJesus.org

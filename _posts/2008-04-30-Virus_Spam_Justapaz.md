---
title:  "Virus Spam Justapaz"
header:
  teaser: "/assets/images/500x300.png"
categories: 
  - Seguridad
tags:
  - seguridad
---


El 10 de Abril de 2008 empezó a salir de la IP de Justapaz SPAM como el siguiente:

----
<pre>
From fnjoyful@4webmed.com Thu Apr 10 16:10:10 2008
 victim@smtp.example
Delivery-date: Thu, 10 Apr 2008 16:10:10 -0400
Received: from [200.93.171.42] (helo=cortafuegos.justapaz.org)
by mail.victim.example with smtp (Exim 4.63)
(envelope-from <fnjoyful@4webmed.com>)
id 1Jk361-0000pj-HB; Thu, 10 Apr 2008 16:10:10 -0400
From: "Shirley Abel" <fnjoyful@4webmed.com>
To: "Jadedrpgeri" <victim@smtp.example>
Subject: 3 months of pregnancy may increase the length of pregnancy, canonical
Date: Thu, 10 Apr 2008 15:10:10 -0500
MIME-Version: 1.0
        boundary="----=_NextPart_000_0017_01C89B1C.F8282830"

------=_NextPart_000_0017_01C89B1C.F8282830
        charset="UTF-8"



Disappointed with your sexual health?!!

Your sex life is about to be ruined? You can''t make your girl groan from =
pleasure? !

Try our services!

Amazing prices!
</pre>
----

La IP fue reportada en diversas listas negras de spam, y los servidores de correo empezaron a rechazar correo proveniente del servidor de correo de Justapaz.
Analizando el tráfico en la red (con tcpdump en el cortafuegos que también es OpenBSD distribución adJ) se descubrieron:

* Un computador con Windows XP y un virus que enviaba el SPAM
* Otro computador con Windows XP que hacia conexiones extrañas e intercambiaba información.
* Posteriormente el segundo virus apareció en otros dos computadores. 

Aunque esos computadores tenían antivirus actualizados, estos no detectaban los virus que estaban produciendo ese tráfico. De hecho el segundo virus no pudo ser detectado con los mejores y más recientes antivirus (ver [Virus Controlado Remotamente Justapaz]).

Tuvieron que aislarse de la red estos computadores mientras fueron formateados y mientras tanto se procedió a sacar la IP de varias listas negras:

* 13.Abr http://psbl.surriel.com/evidence?ip=200.93.171.42&action=Check+evidence
* 13.Abr http://cbl.abuseat.org/remove.cgi
* 14.Abr http://www.five-ten-sg.com/blackhole.php?ip=200.93.171.42
* 15.Abr http://www.barracudacentral.com/index.cgi?p=lookups&r=1&ip=200.93.171.42 

Después los servidores grandes (gmail, hotmail y yahoo) empezaron a recibir nuevamente los correos de Justapaz, aunque en algunos servidores hubo repercusiones hasta el 21.Abr.

A raíz de este problema se propuso migración paulatina a Linux Ubuntu en los computadores de usuarios, la cual se ha venido implementando.

Esta información se cede al dominio público. 2008. vtamara@pasosdeJesus.org','


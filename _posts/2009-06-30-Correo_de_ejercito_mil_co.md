---
title:  "Correo de ejercito.mil.co"
header:
  teaser: "/assets/images/500x300.png"
categories: 
  - Seguridad
tags:
  - seguridad
---


El 24.Jun.2009 Vladimir Támara recibió un correo con tema ==OFENSIVA==, sin cuerpo y procedente de ==DPTOE-5@ejercito.mil.co==

A la fecha ==ping ejercito.mil.co== muestra la IP ==201.234.71.183==.

Al examinar las cabeceras incluidas más adelante, se ve que el correo no es una suplantación de dominio, pues la IP de la cual proviene es efectivamente la de ==ejercito.mil.co==

----
<pre>
From DPTOE-5@ejercito.mil.co  Tue Jun 23 18:36:07 2009
Received: from microsweb01.impsat.net.co (201.234.71-183.static.impsat.com.co [201.234.71.183] (may be forged))
        by mailgw3.uni-kl.de (8.13.8/8.13.8/Debian-3) with ESMTP id n5NNZga4002735
        (version=TLSv1/SSLv3 cipher=DHE-RSA-AES256-SHA bits=256 verify=NOT)
        for <vtamara@informatik.uni-kl.de>; Wed, 24 Jun 2009 01:35:52 +0200
Received: from localhost (microsweb01.impsat.net.co [127.0.0.1])
        by microsweb01.impsat.net.co (8.13.8/8.13.8) with SMTP id n5NNRrDw026489
        for <vtamara@informatik.uni-kl.de>; Tue, 23 Jun 2009 18:27:53 -0500
Date: Tue, 23 Jun 2009 18:27:53 -0500
Message-Id: <200906232327.n5NNRrDw026489@microsweb01.impsat.net.co>
MIME-Version: 1.0
Subject: OFENSIVA
From: DPTOE-5@ejercito.mil.co
To: vtamara <vtamara@informatik.uni-kl.de>
Status: RO
</pre>
----

Las dos opciones posibles son:
# Un funcionario autorizado envió el correo
# Una persona no autorizada logró enviar correo desde el servidor 201.234.71.183

!!OPCIÓN 1. UN FUNCIONARIO AUTORIZADO ENVIÓ EL CORREO

En el primer caso ha resultado prudente enviar correo por reenviadores/proxys para que la ubicación del remitente sea difícil o imposible de rastrear para el atacante, denunciar públicamente y formalmente, exigir explicación y garantías por parte de las autoridades y orar a Dios quien verdaderamente protege.

El 27.Jun.2009 ante la ausencia de respuesta se publica el siguiente correo:

<pre>
Date: Wed, 24 Jun 2009 07:58:33 -0500                                           
From: Vladimir Támara Patiño <vtamara@pasosdejesus.org>                         
To: atencionciudadanoejc@ejercito.mil.co, DPTOE-5@ejercito.mil.co               
Subject: Correo procedente de ejercito.mil.co                                   
Reply-To: Vladimir Támara Patiño <vtamara@pasosdejesus.org>                     
User-Agent: Mutt/1.5.18 (2008-05-17)                                            

Buenos días en el Señor

Escribo para reportar que hoy recibí un correo procedente de
DPTOE-5@ejercito.mil.co con tema "OFENSIVA"

Para su análisis, publiqué las cabeceras del correo en:

http://seguridad.pasosdejesus.org/?id=Correo+de+ejercito.mil.co

Si se trata de un ingreso no autorizado a su servidor de correo,
agradezco me envíe los registros de las bitácoras que muestren de donde
provino el ingreso.

--                                                                              
Dios, gracias por tu amor infinito.                                             
http://www.primarilypublicdomain.org/letter/                                    
--                                                                              
  Vladimir Támara Patiño.                                                       
  http://www.geocities.com/v-tamara                                             
</pre>

Por la misma ausencia de respuesta, para comparar entre opción 1 y opción 2 se procede a publicar posibilidades de la segunda opción.

!!OPCIÓN 2. USO NO AUTORIZADO DE 201.234.71.183

Para evitar la segunda opción es importante tener correo-web (webmails) sin vulnerabilidades conocidas.  En el caso de ==www.ejercito.mil.co== la herramienta ==nikto== reporta:

----
<pre>
- Nikto v2.03/2.04
---------------------------------------------------------------------------
+ Target IP:          201.234.71.183
+ Target Hostname:    www.ejercito.mil.co
+ Target Port:        80
+ Start Time:         2009-06-25 8:11:08
---------------------------------------------------------------------------
+ Server: Apache/2.2.10 (Unix) mod_ssl/2.2.10 OpenSSL/0.9.8i
- /robots.txt - contains 4 ''disallow'' entries which should be manually viewed. (
GET)
+ OSVDB-0: ETag header found on server, inode: 2105479, size: 92, mtime: 0x460a0
b1bf9800
+ mod_ssl/2.2.10 appears to be outdated (current is at least 2.8.31) (may depend
 on server version)
+ mod_ssl/2.2.10 OpenSSL/0.9.8i - mod_ssl 2.8.7 and lower are vulnerable to a re
mote buffer overflow which may allow a remote shell (difficult to exploit). http
://cve.mitre.org/cgi-bin/cvename.cgi?name=CAN-2002-0082.
+ OSVDB-0: GET /CVS/Entries : CVS Entries file may contain directory listing inf
ormation.
+ OSVDB-0: GET /index.php?module=My_eGallery : My_eGallery prior to 3.1.1.g are 
vulnerable to a remote execution bug via SQL command injection.
+ OSVDB-877: TRACE / : TRACE option appears to allow XSS or credential theft. Se
e http://www.cgisecurity.com/whitehat-mirror/WhitePaper_screen.pdf for details

+ OSVDB-877: TRACE / : TRACE option appears to allow XSS or credential theft. Se
e http://www.cgisecurity.com/whitehat-mirror/WhitePaper_screen.pdf for details
+ OSVDB-3092: GET /tools/ : This might be interesting...
+ OSVDB-3093: GET /index.php?base=test%20 : This might be interesting... has bee
n seen in web logs from an unknown scanner.
+ OSVDB-3093: GET /index.php?IDAdmin=test : This might be interesting... has bee
n seen in web logs from an unknown scanner.
+ OSVDB-3093: GET /index.php?pymembs=admin : This might be interesting... has be
en seen in web logs from an unknown scanner.
+ OSVDB-3093: GET /index.php?SqlQuery=test%20 : This might be interesting... has
 been seen in web logs from an unknown scanner.
+ OSVDB-3093: GET /index.php?tampon=test%20 : This might be interesting... has b
een seen in web logs from an unknown scanner.
+ OSVDB-3093: GET /index.php?topic=&amp;lt;script&amp;gt;alert(document.cookie)&
amp;lt;/script&amp;gt;%20 : This might be interesting... has been seen in web lo
gs from an unknown scanner.
+ 3577 items checked: 14 item(s) reported on remote host
+ End Time:        2009-06-25 8:16:08 (324 seconds)
---------------------------------------------------------------------------
+ 1 host(s) tested

Test Options: -host www.ejercito.mil.co
---------------------------------------------------------------------------
----
</pre>

la dirección http://www.ejercito.mil.co//CVS/Entries responde 

<pre>
D/cache////
D/documentacion////
D/js////
D/recursos_user////
D/tools////
D/_administracion////
D/_config////
D/_crontab////
D/_db////
D/_editor////
D/_include////
D/_interfaz////
D/_lib////
D/_templates////
D/_templates_boletin////
/.htaccess/1.1/Fri Nov 11 19:34:16 2005//
/.project/1.1/Thu Sep 14 16:07:03 2006//
/giveprivileges/1.1/Thu Jun 22 14:50:53 2006//
/index.php/1.1/Wed Nov 29 13:52:41 2006//
/info.php/1.1/Tue Feb 28 19:43:19 2006//
/robots.txt/1.1/Tue Aug 16 16:54:52 2005//
/contenido.xml/1.2/Thu Dec 14 00:07:15 2006//
/BannerNavidad.jpg/1.1/Thu Dec 14 22:01:17 2006/-kb/
/foto_noticias.swf/1.1/Wed Dec 20 20:41:50 2006/-kb/
/foto_noticias_ingles.swf/1.1/Wed Dec 20 20:20:16 2006/-kb/
D/recursos_foto_noticia////
</pre>

http://www.ejercito.mil.co/giveprivileges es

<pre>
#/bin/sh
chmod 777 -R _administracion/templates_c/ cache/ _templates/Default/templates_c/
</pre>

http://www.ejercito.mil.co//CVS/Root es

<pre>
:pserver:aforero@linuxserver:2401/home/cvs
</pre>

http://www.ejercito.mil.co//CVS/Repository es

<pre>
ejercito2007
</pre>


Revisando otros CVS/Entries de otros directorios:

<pre>
http://www.ejercito.mil.co/documentacion/CVS/Entries
D/bd////

http://www.ejercito.mil.co/documentacion/bd/CVS/Entries
D/MSSQL////
D/MySQL////
D/Oracle////
D/PostgreSQL////
/bd[16-11-2005].dds/1.1/Wed Jan 11 17:51:06 2006/-kb/
/bdmysql-25-07-2006.sql/1.1/Fri Oct  6 15:33:04 2006//
/delbdmysql.sql/1.1/Fri Oct  6 15:30:23 2006//
</pre>

y así puede continuarse examinando la estructura del CMS, conociendo los nombres de los archivos pueden revisarse y algunos revelan más información por ejemplo:
http://www.ejercito.mil.co/documentacion/bd/bdmysql-25-07-2006.sql


!!CONCLUSIÓN EN PROGRESO

* Se ha podido revelar información privada del manejador de contenidos sobre el que está ==ejercito.mil.co== (que es el mismo de otros sitios desarrollados por ==micrositios.net== como por ejemplo ==www.fac.mil.co==).
* En el momento está fuera de servicio ==correo.ejercito.mil.co== que es importante para el webmail.  Extraña que la IP de ==correo.ejercito.mil.co== es 190.24.146.70 que es diferente a la de ==www.ejercito.mil.co== 201.234.71.183, pues de esta última procedió el correo que ha motivado esta investigación.
* Siguen siendo plausibles las dos opciones, pues ha sido relativamente fácil encontrar y explotar una vulnerabilidad del CMS de ==www.ejercito.mil.co== y en analogía un atacante externo a ==ejercito.mil.co== pudo haber encontrado alguna vulnerabilidad en el sistema de correo para enviar el correo que motivó esta investigación. Sin embargo hasta el momento no se han encontrado vulnerabilidades en el webmail y se ha identificado que la dirección remisora es del webmaster de ==ejercito.mil.co== (ver http://www.ejercito.mil.co/index.php?idcategoria=225253 ), por lo que no se descarta que el correo haya sido escrito por dicho funcionario.



---
title:  "Crackeada pagina Contagio Radio"
header:
  teaser: "/assets/images/500x300.png"
categories: 
  - Seguridad
tags:
  - seguridad
---


El comunicado disponible en:

http://www.colectivodeabogados.org/Contagio-Radio-victima-de-hackeo

es:

! Contagio Radio víctima de Hackeo Medios Alternativos

A nuestras y nuestros oyentes, a la opinión pública nacional e internacional, que infortunadamente hoy 23 de marzo, a las 11:40 a.m. hemos sido víctimas de hackeo en la página web de !ContagioRadio, vulnerando nuestro derecho a la libertad de expresión y el derecho a la información a nuestros abonados que ya suman 140 mil.

Con esta actuación se pretende acallar el trabajo periodístico que realiza !ContagioRadio, desde hace más de un año, dando seguimiento a situaciones de amenazas de muerte y crimenes de defensores y defensoras de Derechos Humanos y líderes comunitarios y activistas, habitantes de iniciativas alternativas urbanas y rurales, de las Zonas Humanitarias y de Biodiversidad, la crisis ambiental, el desplazamientos forzado, las desapariciones forzadas, las detenciones masivas, ejecuciones extrajudiciales, la humanización del onflicto armado, el entramado del paramilitarismo y sus relaciones con el presidente de Colombia, Álvaro Uribe Vélez y en general la violación extrema a los derechos humanos que se vive en nuestro país.

Coincidentemente la semana anterior desde !ContagioRadio informamos de primera mano sobre el capítulo de la paraeconomía con la orden de captura contra los 24 empresarios palmeros acusados de desplazamientos forzados y asesinatos en el Curvaradó y Jiguamiandó, la decisión de la Corte Constitucional de impedir la entrega de tierras a personas afines a estos empresarios, las audiencias ante la Corte Interamericana de Derechos Humanos, las acciones ilegales de inteligencia hechas por el DAS específicamente el juicio que se adelanta contra Jorge Noguera, El asesinato del defensor de derechos humanos Rogelio Martínez, las amenazas a organizaciones internacionales como WOLA junto con 80 organizaciones nacionales defensoras de Derechos Humanos, la decisión de negar la libertad del Coronel (r) Alfonso Plazas Vega implicado en la desaparición forzada de 11 personas en la retoma del Palacio de Justicia, logrando un alto pico de sintonía.

A este hackeo se suman las acusaciones de las que hemos sido víctimas cuando nos señalan de hablar contra el desarrollo y el gobierno, como se referencia en la Constancia del pasado 10 de mayo, de la Comisión de Justicia y Paz, en la que un informe militar señala que “tienen una emisora contra el gobierno, donde hablan contra el desarrollo, y hablan el CAJAR, los Colombianos Juristas, y organizaciones contra el gobierno”. Igualmente, algunas de nuestras emisiones han sido usadas ante la Corte Interamericana de Derechos HUmanos para desvirtuar alegatos en la caso del asesinato de Manuel Cepeda Vargas.

Aún a pesar de los intentos por callar nuestras voces, buscaremos alternativas para que ellas salgan siempre con el propósito de construir desde la diversidad y la diferencia una Colombia donde el respeto a los Derechos Humanos y a los derechos de los pueblos sea una realidad.

Estaremos intentado restablecer nuestra página web para seguir con nuestra programación habitual y Otra mirada a las 4 pm, de lo contrario haremos llegar nuestros programas a la red social Facebook y Twitter y sus correos.

Agradecemos al Colectivo de Abogados, al Movice y a la Comisión de Justicia y Paz por este envío.

Con indignación y preocupación

Equipo de !ContagioRadio

------
En el momento de este escrito Contagio Radio transmite desde la
IP 72.29.81.233 cuyos puertos abiertos son :

<pre>
PORT      STATE  SERVICE
21/tcp    open   ftp
22/tcp    closed ssh
25/tcp    open   smtp
26/tcp    open   rsftp
53/tcp    open   domain
80/tcp    open   http
110/tcp   open   pop3
143/tcp   open   imap
443/tcp   open   https
587/tcp   closed submission
993/tcp   open   imaps
995/tcp   open   pop3s
30000/tcp closed unknown
</pre>

Justamente los mismos de la IP 207.7.84.33 que está sirviendo www.contagioradio.com.  Este último es un servidor ubicado en Estados
Unidos  ( http://ip-address-lookup-v4.com/lookup.php?ip=207.7.84.33 )
de Private Systems.


El puerto 21 de ambos servidores es atendido por Pure-FTPd (que no es típico de OpenBSD) y no permite conexiones anonimas por que lo que debe ser el método empleado para transmitir archivos a ese servidor. Es inseguro sus claves pueden conocerse en los sitios por donde pasan conexiones así como la información transmitida.

El puerto 22 está infortunadamente cerrado en ambos, justamente ssh y sftp si son servicios encriptados.

El puerto 25 es atentido por exim (que tampoco es típico de OpenBSD). Sólo en el servidor 207.7.84.33 está habilitado también el 465.

Los servicios IMAP y POP en puertos 110 y 143 son inseguros por cuanto transmiten claves e información desencriptada.   Mejor usar contrapartes POPS e IMAPS en puertos 993 y 995.

Con respecto al servicio WEB tienen instalado cPanel por ejemplo http://www.contagioradio.com:2082/login/

El gestor de contenidos de www.contagioradio.com es Joomla (según el encabezado Joomla 1.5 que ha tenido problemas de seguridad reportados recientemnete).

Según "nmap -O" ambas IPs corren posiblemente OpenBSD, por los servicios que se ven en los puertos debe haber una DMZ con cortafuegos OpenBSD y servidor con Linux.



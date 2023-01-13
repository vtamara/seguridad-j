---
title:  "Vulneración a la seguridad de la Fiscalía General de Colombia por parte
de Guacamaya en Agosto de 2022"
header:
categories: 
  - Seguridad
tags:
  - seguridad
---

Según <https://enlacehacktivista.org/index.php?title=Fiscalia> es posible
para los colombianos solicitar allí los 5TB de correos que el grupo 
centroamericano Guacamaya le extrajo a la Fiscalía.  Posiblemente así
lo hizo Revista Semana que con acceso a la información publicó 
en <https://www.semana.com/nacion/articulo/este-es-el-mega-hackeo-a-la-fiscalia-que-puso-en-evidencia-la-vulnerabilidad-de-la-ciberseguridad-en-el-pais/202248/>
detalles de la información filtrada que incluye procesos penales, seguimientos,
informes de policía judicial, solicitudes y resultados de interceptaciones
telefónicas, pruebas de balística, interrogatorios y conclusiones
de investigaciones en todo el país.

Según
<https://www.elespectador.com/opinion/columnistas/carolina-botero-cabrera/las-filtraciones-de-guacamaya/>
por tratarse de información de interés público sobre corrupción o 
violaciones a derechos humanos su publicación está protegida por
la libertad de expresión.

Según
<https://www.eltiempo.com/tecnosfera/novedades-tecnologia/fiscalia-hackeada-analisis-de-jose-carlos-garcia-711854> la fiscalía intento responsabilizar a su
proveedor de infraestructura y comunicaciones, Movistar como responsable,
pero el mismo artículo dice que eso no es admisible pues "Proteger la
información sensible que manejan, de seguridad nacional, no se descarga en un
tercero con un contrato de servicio."

Según
<https://devel.group/blog/guacamaya-hacks-libera-correos-robados-mediante-vulnerabilidad-en-exchange/> el método empleado por Guacamaya con otras
filtraciones latinoamericanas en el 2022 fue emplear las vulnerabilidades 
CVE-2021-34523 y CVE-2021-31207 
para autenticarse y ganar privilegios del servidor de correo Microsoft 
Exchange para hacer la descarga de los correos, después mediante un 
documento malicioso abierto por un usuario en la Intranet tuvieron acceso
al servidor de la Intranet.  Estas y otras vulnerabilidades
para estos ataques son confirmadas por
<https://www.ciberseguridadlatam.com/2022/12/14/las-vulnerabilidades-aprovechadas-por-el-grupo-guacamaya-continuan-dejando-victimas-en-america-latina-alerta-kaspersky/>

A lo largo del tiempo he visto más vulnerabilidades en servidores 
Windows que en servidores tipo Unix, eso sumado a la pereza o falta
de tiempo para actualizar los servidores deja huecos conocidos abiertos.
Repetimos entonces:

1. Para resguardar información sensible elegir herramientas con base
   en su historial de seguridad --no su popularidad.

2. Establecer rutinas de seguridad que incluyan actualización periódica y
   revisión de estas por un par.

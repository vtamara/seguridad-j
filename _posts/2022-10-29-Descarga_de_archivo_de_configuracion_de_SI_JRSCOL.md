---
title:  "Descarga de archivo de configuración de SI-JRSCOL"
header:
categories: 
  - Seguridad
tags:
  - seguridad
---

Problema: Acceso a información de configuración de la aplicación que no se
esperaba que fuera descargada .git/config y .env desde la IP 184.73.5.45 y
desde otras 19 IPs en menor medida.

Se debió a una configuración errada de servidor web.

# Identificación:

La información de `.git/config` (y de `.git`) podía descargarse con
<https://colombiajrs.info/.git/config> Sin embargo se trata de  información
pública porque es la misma de <https://gitlab.com/pasosdeJesus/si_jrscol>

La información de `.env` podía descargase con <https://colombiajrs.info/.env>
Esta información es  privada de la configuración de la aplicación, pero se
auditó más a profundidad y se verificó que o bien no podía usarse para extraer
información del servidor de JRS-Colombia desde fuera del mismo servidor o que
no hubo intentos.  Se tuvo que auditar servidor de correo de Pasos de Jesús
porque en el archivo .env había credenciales del usuario sijrscol usado para
enviar correos, no se encontró evidencia de usos no autorizados.

Contención:

* Se arreglo configuración del servidor web para evitar acceso a archivos de
  configuración 

* Se cambió clave de usuario en base de datos (no era necesario porque se
  verificó que no podía usarse desde fuera del servidor por el cortafuegos
  de Banco de Datos y el interno del servidor de JRS ).

* Se mejoró configuración de copias de respaldo y anexos. Se verificó que
  con la información de .env, aún con la configuración errada del servidor
  no podía accederse.  En todo caso se auditaron bitácoras del servidor
  web más a profundidad buscaron intentos de acceso a copias o anexos
  desde el web sin encontrar evidencia.

* En servidor de correo de Pasos de Jesús, se cambio clave del usuario
  sijrscol que envía correos con notificaciones.  Se verificó que era
  posible el ingreso con la información del archivo .env pero no se
  encontró evidencia de ingreso alguno en bitácoras ni usos del servicio
  SMTP fuera de los generados por el sistema.

* Se reportó la IP 184.73.5.45 en
  <https://www.abuseipdb.com/check/184.73.5.45> y  se bloqueó en
  cortafuegos de BD  así como las  otras 19 IPs que descargaron el
  archivo `.env`: 
  103.167.84.15
  109.237.100.22
  13.74.160.19
  165.22.101.86
  172.105.120.53
  177.8.200.5
  185.174.28.39
  185.83.144.103
  185.83.146.154
  186.29.79.105
  20.171.47.42
  20.38.2.237
  45.130.97.117
  46.28.108.153
  51.140.251.74
  51.141.30.109
  52.176.207.199
  88.214.43.164
  89.252.177.18

# Restauración

Se reiniciaron servicios tras cambios en configuración y se verificó
funcionalidad y que ya no es explotable la falla en la
configuración.

No se requirieron más acciones de restauración por cuanto no hubo
modificación ni perdida de información. 


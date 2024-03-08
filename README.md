# Práctica 2- Servidor alojamiento web
## Se pide las instalación, configuración y puesta en marcha de un servidor que ofrezca servicio de alojamiento web configurable.

Este proyecto se centra en brindar un servicio completo de alojamiento web. Este servicio incluirá soporte tanto para páginas estáticas como dinámicas desarrolladas en PHP. Cada cliente recibirá un directorio de usuario personalizado que contendrá una página web predeterminada. Además, se facilitará a los usuarios la gestión de bases de datos SQL a través de la interfaz de phpMyAdmin. Para la administración de archivos, se implementará un acceso seguro mediante FTP con TLS y SSH/SFTP. 

- Instalacion del sistema operativo, en nuestro caso usaremos Ubuntu Server-22.04.3
- 
  ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/9a308fd3-435b-4c05-9060-f523f5a5c8d8)


                                INSTALACION DE SERVICIOS NECESARIOS

  Actualizamos el indice de paquetes

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/1cbf158e-5bbb-4c82-887f-4b20b0ead993)

Instalación de Apache con el comando: sudo apt-get install apache2

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/2d506c40-6798-4f6f-9b15-9d3f30230470)


Instalación de php con el comando: sudo 

  ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/9f9c7d5e-4482-4290-a848-a13785c6a7c5)
  

Instalación Php: librerías de php para apache: sudo apt-get install php libapache2-mod-php


![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/9bcf3ee3-8c5c-44cd-9f0a-3c35c1609029)


 
  Instalación de PHPMYADMIN

  ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/d59c273a-f22e-4d2f-b4f3-dbbb15ff7c47)



  Instalación de MYSQL

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/3ec43cf1-fbec-484c-a427-e434922e1a07)



Instalación Dns (bind9):

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/a4c67ab4-f14f-48b6-878e-4e0e98d4c7e5)

Instalación Python: módulo de python3 para apache.

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/e18b5224-3a27-4d90-9a75-76804c7225dc)


Instalación ProFtpd:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/4915bc0f-dfbc-4d9e-bad5-86c7aac8c5de)


Instalación OpenSsl:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/dd8278c6-264c-42b0-8641-e1ea74ffbd73)


Instalación Filezilla:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/92b545f6-c4fe-47c4-a506-350485add406)


Instalación Postfix:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/a3f65419-ec79-4182-8b15-0bfd90bf60c0)


Instalación Dovecot:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/3229e522-8621-4a8e-b86d-42066ace1382)

Instalación de vsftpd:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/373ac666-9507-4a0c-a52f-2ee52569f767)


Después de instalar estos paquetes, tenemos un servidor web Apache en funcionamiento con soporte para PHP y una base de datos MySQL instalada. phpMyAdmin te proporcionará una interfaz web para administrar tus bases de datos MySQL.


CONFIGURAMOS LOS SERVICIOS INSTALADOS

Generamos un certificado SSL

 Creamos un directorio para almacenar los certificados SSL:
 
 ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/dcda8f25-c235-4397-a2c4-9d782f29159c)

Genera un certificado autofirmado:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/8d3bebb9-46bc-4dc4-bc17-80b296a52a9b)

Configuramos filezilla para entrar, usamos certificado ssl:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/f0d5839e-1977-44de-afbb-34e8dca2a618)

Configuramos Postfix

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/818c270c-8c39-4a0c-bb72-92412560d01c)

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/abb64398-32ae-4c1c-bd99-20010b16b715)

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/b4ad3f21-ad76-4a03-aa49-13e62b7a8320)

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/9a1bcb38-1fb1-4df4-8ff6-f937a2fbca4e)

Configuramos los protocolos pop3 e imap en dovecot.

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/de53d574-c0ee-4445-9fad-6d6b2deef79b)

Comprobamos que dovecot tiene activado ssl.

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/6bd2d6b5-996d-4a47-8dd5-6a538f303857)


DESCRIPCIÓN COMPLETA DEL SCRIPT

                #!/bin/bash

                usuario=$1
                contra=$2
                ip=$3
                dominio="${usuario}.marisma.local"

                if [ $# -ne 3 ]; then
                  echo "Error: Debes proporcionar exactamente 3 argumentos - nombre, contraseña e IP."
                  exit 1
                fi

                #Variables para las rutas de zonas
                zona_directa="/etc/bind/zones/db.marisma.local"
                zona_inversa="/etc/bind/zones/db.192.168.195"

                #Creación del directorio de trabajo
                sudo useradd -m -d /home/$usuario -s /bin/bash $usuario

                #Configuración de la contraseña del usuario
                echo "$usuario:$contra" | sudo chpasswd

                
                #Configuración subdominio DNS
                #Zona directa
                echo "\$ORIGIN ${dominio}." >> $zona_directa
                echo "@ IN A ${ip}" >> $zona_directa
                echo "www IN A ${ip}" >> $zona_directa
                #Zona inversa
                echo "${ip} IN PTR ns.${dominio}." >> $zona_inversa


              service apache2 reload > /dev/null
              service bind9 reload > /dev/null
              service proftpd reload > /dev/null


              #Configuración del host virtual en Apache
              ruta_a="/etc/apache2/sites-available/${dominio}.conf"
              ruta_e="/etc/apache2/sites-enabled/${dominio}"
              document_root="/var/www/html/$usuario"
              dir_python="${document_root}/python-web"
              app_python="${dir_python}/mypythonapp"
              public_python="${dir_python}/public_html"
              controller_py="${app_python}/controller.py"

              #Añadir el dominio al fichero hosts

              echo "${ip} ${dominio}" >> /etc/hosts
              echo "127.0.0.1 ${dominio}" >> /etc/hosts

              mkdir $document_root
              mkdir $dir_python
              mkdir $app_python
              mkdir $public_python

              #Crear fichero python

              touch $controller_py
              echo "# -*- coding: utf-8 -*-
              def application(environ,start_response):
              status= '200 OK'
              html = 'Página del usuario ${usuario} python'
              html = bytes(html,encoding='utf-8')
              response_header = [('Content-type','text/html')]
              start_response(status,response_header)
              yield html" > ${controller_py}

              #Crear el archivo de configuración del host virtual
              echo "<VirtualHost *:80>
              ServerAdmin admin@$dominio
              ServerName $dominio
              WSGIScriptAlias / $controller_py
              DocumentRoot $public_python
              <Directory />
              Options FollowSymLinks
              AllowOverride all
              </Directory>
              ErrorLog /var/log/apache2/$dominio.errorLog.log
              CustomLog /var/log/apache2/$dominio.customLog.log combined
              </VirtualHost>" | sudo tee $ruta_a > /dev/null


              #Verificar la configuración de Apache
              apache2ctl configtest

              #Habilitar el sitio y reiniciar Apache si la verificación es exitosa
              if [ $? -eq 0 ]; then
              a2ensite $dominio > /dev/null
              systemctl restart apache2
              else
              echo "Error en la configuración de Apache. No se ha habilitado el sitio."
              fi

              #Configuración base de datos
              mysql -u root -e "CREATE DATABASE $usuario;"
              mysql -u root -e "CREATE USER '$usuario'@'localhost' IDENTIFIED BY  '$contra';"
              mysql -u root -e "GRANT ALL PRIVILEGES ON $usuario.* TO '$usuario'@'localhost';"
              mysql -u root -e "FLUSH PRIVILEGES;"

              echo "El usuario ${usuario} ha sido creado con exito"

  
------------------------------------------------------------------------------------------------
EN EL PROCESO ANTERIOR HABIA QUE CUMPLIR LO SIGUIENTE...

- ***Se dará alojamiento a páginas web tanto estáticas como dinámicas con “php”.***

- ***Los clientes dispondrán de un directorio de usuario con una página web por defecto.*** 

- ***Además contarán con una base de datos sql que podrán administrar con phpmyadmin.***

- ***Los clientes podrán acceder mediante ftp para la administración de archivos configurando adecuadamente TLS.***

- ***Se habilitará el acceso mediante ssh y sftp.*** 

- ***Se configura de forma adecuada postfix y dovecot imap y pop3***

- ***Se automatizará mediante el uso de scripts:***

- ***La creación de usuarios y del directorio correspondiente para el alojamiento web.***

- ***Host virtual en apache.***

- ***Creación de usuario del sistema para acceso a ftp, ssh, smtp, …***

- ***Se creará un subdominio en el servidor DNS con las resolución directa e inversa.***

- ***Se creará una base de datos además de un usuario con todos los permisos sobre dicha base de datos (ALL PRIVILEGES).***

- ***Se habilitará la ejecución de aplicaciones Python con el servidor web.***


-----------------------------------------------------------------------------------

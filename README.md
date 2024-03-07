# Práctica 2- Servidor alojamiento web
## Se pide las instalación, configuración y puesta en marcha de un servidor que ofrezca servicio de alojamiento web configurable.

Este proyecto se centra en brindar un servicio completo de alojamiento web. Este servicio incluirá soporte tanto para páginas estáticas como dinámicas desarrolladas en PHP. Cada cliente recibirá un directorio de usuario personalizado que contendrá una página web predeterminada. Además, se facilitará a los usuarios la gestión de bases de datos SQL a través de la interfaz de phpMyAdmin. Para la administración de archivos, se implementará un acceso seguro mediante FTP con TLS y SSH/SFTP. 

- Instalacion del sistema operativo, en nuestro caso usaremos Ubuntu Server-22.04.3
- 
  ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/9a308fd3-435b-4c05-9060-f523f5a5c8d8)


INSTALACION DE SERVICIOS NECESARIOS

Instalación de Apache con el comando: sudo apt-get install apache2

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/2d506c40-6798-4f6f-9b15-9d3f30230470)




























------------------------------------------------------------------------------------------------

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



INSTALACION DE SERVICIOS NECESARIOS

  Instalación de APACHE



  
  Instalación de PHP

  ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/9f9c7d5e-4482-4290-a848-a13785c6a7c5)


  Instalación de MYSQL

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/3ec43cf1-fbec-484c-a427-e434922e1a07)

  
  Instalación de PHPMYADMIN

  ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/d59c273a-f22e-4d2f-b4f3-dbbb15ff7c47)

  Instalación de VSFTPD

  ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/4686d8fd-0ac4-4022-b00f-771b90d4798c)
  

  Instalación de OPENSSH

  ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/1e7805cc-c0ec-4ab0-8d7c-8b4c29c39f11)

  

  Instalación de POSTFIX Y DOVECOT

  ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/e7194ca4-1b07-4c8c-9784-327e7e6eb34e)
  

  Instalación de PYTHON Y modulos necesarios.


  ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/2c893265-1d45-45a5-b7dc-7da186918a39)


  ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/e090129f-85ef-4788-9ba8-5eceef5129cb)


 CONFIGURACION DE SERVICIOS INSTALADOS


-------------- NUEVO ------------------

Instalación de Apache, MySQL, PHP y phpMyAdmin:

Instala Apache, MySQL/MariaDB, PHP y phpMyAdmin en tu servidor. 

instalar Apache, MySQL/MariaDB, PHP y phpMyAdmin en sistemas basados en Debian/Ubuntu (apt) y en sistemas basados en Red Hat/CentOS (yum). Utilizaré el paquete apache2 para Apache, mysql-server para MySQL/MariaDB, php para PHP y phpmyadmin para phpMyAdmin.

Actualizamos el indice de paquetes

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/1cbf158e-5bbb-4c82-887f-4b20b0ead993)

Instalamos Apache

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/bf93c08e-70f4-472d-96ff-9636b50c2db1)

Instala MySQL/MariaDB:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/223cbeaf-b52d-4733-8a73-db6e4db7ad66)

Instala PHP:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/17848095-79d1-4bae-bc97-2cc1f4952574)

Instala phpMyAdmin:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/348a7f24-7fc5-47b5-b4d2-2ea87aece6d4)

Durante la instalación de phpMyAdmin, se te pedirá que elijas el servidor web que estás utilizando (Apache o Nginx), y phpMyAdmin se configurará automáticamente para funcionar con el servidor web seleccionado.

Después de instalar estos paquetes, deberías tener un servidor web Apache en funcionamiento con soporte para PHP y una base de datos MySQL/MariaDB instalada. phpMyAdmin te proporcionará una interfaz web para administrar tus bases de datos MySQL/MariaDB.

Recuerda ajustar la configuración de seguridad según sea necesario, como configurar contraseñas para MySQL/MariaDB y restringir el acceso a phpMyAdmin mediante configuraciones de Apache.


Aquí tienes los pasos para configurar vsftpd para conexiones FTP seguras mediante TLS/SSL, generar certificados SSL/TLS y configurar el cortafuegos para permitir el tráfico FTP:

Instalación de vsftpd:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/373ac666-9507-4a0c-a52f-2ee52569f767)

Generación de certificados SSL/TLS:

Crea un directorio para almacenar los certificados SSL/TLS:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/5c80c40c-071f-4b2b-bee0-7b34647a19ff)

Genera un certificado autofirmado:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/48a47a1b-9dc3-4ec0-b054-7d53781afd71)


![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/af2b447a-a666-4214-a49b-01b9be417c35)


Durante este proceso, se te pedirá que proporciones la información de tu certificado, como el nombre de la organización, la ubicación, etc. Puedes completar estos campos según tu preferencia.
Configuración de vsftpd:

Abre el archivo de configuración de vsftpd:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/e8cd9d57-b078-4064-acb4-a45206536d52)


Dentro del archivo, asegúrate de tener estas líneas descomentadas o añádelas:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/0754f586-690e-42f8-9899-64e039f76bb2)


Reinicia vsftpd para aplicar los cambios:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/0cb6a8f9-e084-40e3-ac45-3902d8102a37)

Configuración del cortafuegos:

Si estás utilizando UFW (Uncomplicated Firewall), puedes permitir el tráfico FTP con TLS ejecutando:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/784cba0d-986b-46aa-82cd-1311c06c3f60)


Con estos pasos, deberías tener vsftpd configurado para permitir conexiones FTP seguras mediante TLS/SSL, con certificados SSL/TLS generados y el tráfico FTP permitido a través del cortafuegos. Recuerda que los certificados autofirmados proporcionan seguridad básica, pero para un entorno de producción, considera obtener un certificado SSL/TLS de una autoridad de certificación reconocida.



Para habilitar SSH y SFTP en tu servidor, así como configurar la autenticación de claves SSH para una mayor seguridad, sigue estos pasos:

Instala OpenSSH:
Si no está instalado, instala el paquete OpenSSH en tu servidor. Dependiendo de tu distribución de Linux, puedes usar los siguientes comandos:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/54488911-68f4-4efe-a02d-d6ef3369de5a)


Verifica el estado de SSH:
Una vez instalado, verifica que el servicio SSH esté en ejecución utilizando el siguiente comando:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/de217c1f-f00f-465c-8ddd-85a6e746d1ef)


Si SSH no está en ejecución, puedes iniciarlo con el siguiente comando:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/73a9b7d1-99e8-4d70-8eef-7e4d0c684c13)

Configuración de SSH:
Puedes ajustar la configuración de SSH según tus necesidades en el archivo de configuración principal /etc/ssh/sshd_config. Por ejemplo, puedes cambiar el puerto predeterminado de SSH (22) o habilitar/deshabilitar ciertas opciones de seguridad.

Habilitar SFTP:
SFTP está integrado en OpenSSH y generalmente está habilitado por defecto. Los usuarios pueden conectarse a través de SFTP utilizando sus credenciales de SSH.

Configuración de la autenticación de claves SSH:
La autenticación de claves SSH proporciona una capa adicional de seguridad al requerir que los usuarios proporcionen una clave privada junto con su nombre de usuario al conectarse al servidor SSH. Para configurar la autenticación de claves SSH, sigue estos pasos:

Genera un par de claves SSH (pública y privada) en tu cliente local si aún no tienes uno:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/0efdbef8-d422-43bf-8953-5f2c32bb51d3)

Copia la clave pública (id_rsa.pub) al servidor remoto. Puedes hacerlo manualmente o utilizando el comando ssh-copy-id:

------------------------------------------------------
1. Creación de usuarios y directorios para el alojamiento web:
Crea un usuario para cada sitio web que desees alojar en el servidor. Por ejemplo, puedes utilizar el comando sudo adduser nombre_usuario.
Crea un directorio para cada sitio web en el directorio de documentos del servidor web. Por ejemplo, mkdir /var/www/nombre_sitio.
Asigna los permisos adecuados al directorio para que el usuario del sitio web tenga acceso. Puedes hacerlo con chown y chmod.
2. Configuración de host virtual en Apache:
Crea un archivo de configuración para el host virtual dentro del directorio de configuración de Apache, como /etc/apache2/sites-available/.
Configura el host virtual con la directiva VirtualHost, especificando el nombre de dominio y el directorio raíz del sitio web.
Habilita el host virtual utilizando el comando a2ensite.
3. Creación de usuario del sistema para acceso a FTP, SSH, SMTP, etc.:
Utiliza el comando adduser para crear un nuevo usuario en el sistema.
Configura los permisos adecuados para el usuario, como permitir o denegar el acceso SSH, FTP, etc.
4. Configuración de subdominio en el servidor DNS:
Agrega un nuevo registro DNS en el panel de control de tu proveedor de dominios para el subdominio.
Configura la resolución directa e inversa en el servidor DNS para el nuevo subdominio.
5. Creación de base de datos y usuario con privilegios:
Utiliza el sistema de gestión de bases de datos que estés utilizando (como MySQL o PostgreSQL) para crear una nueva base de datos y un usuario asociado con todos los privilegios (ALL PRIVILEGES) sobre esa base de datos.
6. Habilitación de ejecución de aplicaciones Python con el servidor web:
Instala el módulo mod_wsgi en Apache para ejecutar aplicaciones Python.
Configura un nuevo host virtual en Apache con soporte para aplicaciones Python y especifica la ruta de acceso a la aplicación WSGI.
Una vez que hayas completado estos pasos adicionales, habrás extendido la configuración de tu servidor de alojamiento web para satisfacer las necesidades adicionales mencionadas. Recuerda siempre realizar pruebas exhaustivas después de cada configuración para garantizar su correcto funcionamiento

1. Crear un usuario para cada sitio web:
Utiliza el comando adduser para crear un nuevo usuario en el sistema. Por ejemplo, si tu sitio web se llama "ejemplo", puedes ejecutar:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/0c43e533-f6dd-44cb-a887-375c2755768f)


2. Crear un directorio para cada sitio web:
Crea un directorio dentro del directorio de documentos del servidor web, como /var/www/, para cada sitio web. Por ejemplo:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/c6e8d8ad-d49a-42ba-af3d-83776da5451c)

3. Asignar los permisos adecuados al directorio:
Para que el usuario del sitio web tenga acceso al directorio, puedes cambiar el propietario y el grupo del directorio al usuario que acabas de crear. También puedes establecer los permisos apropiados. Por ejemplo:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/d174541b-5762-4b73-b210-7b12c906eab9)


En este caso, -R indica que los cambios se aplicarán recursivamente a todos los archivos y subdirectorios dentro de /var/www/ejemplo. Los permisos 755 otorgan permisos de lectura, escritura y ejecución al propietario, y permisos de lectura y ejecución al grupo y a otros usuarios.

Ahora, el usuario "ejemplo" tendrá acceso al directorio /var/www/ejemplo y podrá colocar los archivos del sitio web en ese directorio. Asegúrate de repetir estos pasos para cada sitio web que desees alojar en el servidor.
---------------------2222222222222----------
1. Crear un archivo de configuración para el host virtual:
Accede al directorio de configuración de Apache donde se encuentran los archivos de configuración de los sitios virtuales. Por lo general, este directorio es /etc/apache2/sites-available/.
Crea un nuevo archivo de configuración para tu host virtual. Puedes usar cualquier editor de texto, por ejemplo:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/142df974-37fc-4b3e-bc13-e73e124d2959)

2. Configurar el host virtual:
Dentro de este archivo, configura el host virtual utilizando la directiva VirtualHost. Especifica el nombre de dominio y el directorio raíz del sitio web. Aquí tienes un ejemplo básico de configuración:
![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/522c3533-1407-4610-a84d-6e09d26764ec)


3. Habilitar el host virtual:
Utiliza el comando a2ensite para habilitar el host virtual que acabas de crear:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/ad652409-ef88-4ca7-bc75-dd3e52844f0b)

4. Reiniciar Apache:
Para que los cambios surtan efecto, reinicia el servicio de Apache:


![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/689bea84-8338-4ae8-bb0d-57fd9acabf20)

Con estos pasos, has configurado correctamente un host virtual en Apache para tu sitio web. Ahora puedes acceder a tu sitio web a través del nombre de dominio especificado en la configuración del host virtual.


-------------3333333333-----------------

1. Crear un nuevo usuario:
Puedes utilizar el comando adduser o useradd para crear un nuevo usuario en el sistema. La diferencia principal entre ellos radica en la forma en que manejan algunos aspectos específicos de la configuración del usuario. A continuación, se muestra cómo usar adduser:


![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/dc998761-54c7-4bed-b39c-1a2120a9226f)

Contraseña: angelausuario


![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/76ac0a71-6fff-43e6-855e-8424d16631a8)


2. Configurar permisos para acceso a servicios:
Una vez que el usuario ha sido creado, puedes configurar los permisos para determinar su acceso a servicios como SSH, FTP, etc.

INSTALACION servicio SSH

El servicio SSH no está instalado: Es posible que el servidor SSH no esté instalado en tu sistema. En sistemas basados en Debian/Ubuntu, el paquete se llama openssh-server, mientras que en sistemas basados en Red Hat/CentOS, puede ser openssh-server. Puedes instalarlo usando el gestor de paquetes correspondiente a tu distribución. Por ejemplo:


![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/bb22eefb-f0fd-4da1-8416-d7a9b8be4993)


![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/2fa7073f-d4c6-4ff3-8fe1-6cfd9d1670b6)

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/89132837-d30d-4847-a499-b5f1509de125)


![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/36a86801-c9eb-4529-8b43-7deb0a384bf7)






SSH:
Para permitir o denegar el acceso SSH al nuevo usuario, puedes editar el archivo de configuración /etc/ssh/sshd_config y ajustar las directivas según sea necesario. Por ejemplo, para permitir el acceso solo a ciertos usuarios, puedes agregar o modificar la línea:

Abre el archivo de configuración de SSH:


![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/b1947819-3acd-429a-bacd-a92d257c6373)


Dentro del archivo, busca la línea que comienza con AllowUsers. Si no existe, puedes agregarla al final del archivo.

Agrega el nombre de usuario al que deseas permitir el acceso SSH:

 ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/28c5c54a-70a3-4ea0-97a6-7093dd23777a)


Guarda los cambios y cierra el editor.

Reinicia el servicio SSH para que los cambios surtan efecto:

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/69b95a10-865e-44c1-88d8-4a8828a9b299)


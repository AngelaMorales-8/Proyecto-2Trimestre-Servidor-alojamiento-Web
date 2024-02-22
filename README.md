# Práctica 2- Servidor alojamiento web
## Se pide las instalación, configuración y puesta en marcha de un servidor que ofrezca servicio de alojamiento web configurable:

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

- Instalacion de Ubuntu Server-22.04.3
  ![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/9a308fd3-435b-4c05-9060-f523f5a5c8d8)
  

- Actualizamos el sistema:
![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/ac25efa7-9e9c-4d47-b8bf-5a191d5805c2)

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/e53b0a03-1555-40f3-89d8-7180bde1e4c4)



- Instalamos el software necesario

  Instalación de APACHE

![image](https://github.com/AngelaMorales-8/Proyecto-2Trimestre-Servidor-alojamiento-Web/assets/122454505/2d506c40-6798-4f6f-9b15-9d3f30230470)

  
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





















 

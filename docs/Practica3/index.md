# Instalar, configurar y securizar phpMyAdmin

## Prerrequisitos
Antes de instalar PHP, deberías instalar:
* Apache (hecho en la práctica anterior)
* MySQL
  * sudo apt update
  * sudo apt install mysql-server

![mysql](mysql-server.png)


## Instalación de phpMyAdmin
1. Instala phpMyAdmin junto con las extensiones PHP necesarias.
* sudo apt install php-mbstring php-zip php-gd php-json php-curl
```
php-mbstring, php-zip, php-gd, php-json, php-curl
```
![php-instalacion](instalar-php.png)
* sudo apt install php libapache2-mod-php

![php-instalacion](mas-php.png)

Para comprobar que hemos instalado bien php crearemos un archivo con la siguiente información y lo buscaremos a través del navegador.
* sudo nano /var/www/info.php
```
<?php
phpinfo();
?>
```
* http://*IP*/*nombre_archivo*
  * En mi caso será * http://10.10.10.196/info.php
![php-funciona](funciona-php.png)


1. Configurar phpMyAdmin para que funcione con Apache.




3. Habilita la extensión mbstring y reinicia Apache
* sudo systemctl restart apache




------------------------------------------------------------------------

## Configuración del Acceso por Contraseña para la Cuenta Root de MySQL
1. Cambia el método de autenticación del usuario root de MySQL (de auth_socket a caching_sha2_password o mysql_native_password)
* sudo 




2. Verificar los métodos de autenticación empleados por cada uno de tus usuarios.





------------------------------------------------------------------------

## Configuración del Acceso por Contraseña para un Usuario Dedicado de MySQL
1. Crear un nuevo usuario de MySQL con una contraseña segura.
* sudo 





2. Otorgar al nuevo usuario los privilegios apropiados para gestionar las bases de datos a través de phpMyAdmin





------------------------------------------------------------------------

## Asegurando tu Instancia de phpMyAdmin
1. Habilitar el uso de sobrescrituras de archivos **.htaccess** en la configuración de Apache para phpMyAdmin.





2. Crear un archivo **.htaccess** en el directorio de phpMyAdmin para implementar autenticación básica.




3. Crear un archivo **.htpasswd** para almacenar las credenciales de usuario y contraseña.




4. Reiniciar Apache para aplicar los cambios.







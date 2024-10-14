# Instalar, configurar y securizar phpMyAdmin


## Instalación de phpMyAdmin
1. Instala phpMyAdmin junto con las extensiones PHP necesarias.
```
php-mbstring, php-zip, php-gd, php-json, php-curl
```




2. Configurar phpMyAdmin para que funcione con Apache.




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







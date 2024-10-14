# Instalar, configurar y securizar phpMyAdmin


## Instalación de phpMyAdmin

Para crear el certificado autofirmado utilidadopenssl usaremos el siguiente comando: 
```
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/apache-selfsigned.key -out /etc/ssl/certs/apache-selfsigned.crt
```
Introducimos unos datos que se añadirán al certificado.
En mi caso he añadido los siguientes:
![cert](crearcertificado.png)


## Configuración del Acceso por Contraseña para la Cuenta Root de MySQL
Crearemos un script bash donde especificaremos los argumentos que le pasaremos al comando
anterior a través del parámetro **-subj**.


## Configuración del Acceso por Contraseña para un Usuario Dedicado de MySQL







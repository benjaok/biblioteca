Guía paso a paso para instalar el “Sistema de biblioteca Unifranz”

Descripción: desarrollado en PHP con una base de datos,  MySQL.


1. Instalar un servidor local (XAMPP, WAMP, MAMP, etc.)

Opción 1: XAMPP (Windows, Linux, macOS)

Descarga: Ve al sitio web oficial de XAMPP y descarga la versión para tu sistema operativo.

Instalación:

    1. Ejecuta el instalador.
    2. Selecciona los componentes que desees instalar. Para este proyecto, selecciona Apache (servidor web) y MySQL (base de datos).
    3. Completa la instalación y abre el panel de control de XAMPP.

Configura XAMPP:

    1. Inicia el servidor de Apache y MySQL desde el panel de control de XAMPP.

Opción 2: WAMP (Windows)

Descarga e instala WAMP.
2. Descargar el código del sistema de biblioteca
Si ya tienes el código fuente del sistema de biblioteca, simplemente descárgalo en tu computadora.
Si el sistema está en GitHub, usa el siguiente comando en la terminal (si tienes Git instalado):
git clone <[URL_DEL_REPOSITORIO](https://github.com/benjaok/biblioteca)>
3. Mover el código al directorio raíz del servidor

Mueve la carpeta con el código del sistema de biblioteca a la carpeta raíz de tu servidor web. Si estás usando XAMPP, es la carpeta:

C:\xampp\htdocs

Para WAMP:

C:\wamp64\www

Renombra la carpeta de acuerdo al proyecto, por ejemplo biblioteca.


4. Crear la base de datos

Abre tu navegador y accede a phpMyAdmin (normalmente en http://localhost/phpmyadmin).

Crea una nueva base de datos:

1. Haz clic en "Nueva" en la barra lateral izquierda.
2. Asigna un nombre a tu base de datos (por ejemplo, biblioteca).


3. Haz clic en "Crear".




5. Importar la base de datos

En phpMyAdmin, selecciona la base de datos recién creada.

Haz clic en la pestaña "Importar" y selecciona el archivo .sql que contiene la estructura y los datos de la base de datos del sistema de biblioteca.

Haz clic en "Continuar" para completar la importación.


6. Configurar la conexión a la base de datos en el proyecto PHP

Abre el archivo de configuración de base de datos, que suele encontrarse en una carpeta como config, db.php o database.php.

Configura las credenciales de la base de datos, por ejemplo:

$servername = "localhost";
$username = "root";  // o el usuario que hayas configurado
$password = "";  // Si no tienes contraseña para MySQL, deja vacío
$dbname = "biblioteca";

Asegúrate de que estas credenciales coincidan con la configuración de tu base de datos.


7. Configurar permisos (en caso de usar Linux/Mac)

Si usas Linux o macOS, es posible que debas ajustar los permisos de las carpetas. Desde la terminal, navega hasta el directorio del proyecto:

cd /opt/lampp/htdocs/biblioteca
sudo chmod -R 755 .
sudo chown -R www-data:www-data .

8. Probar el sistema

Abre el navegador e ingresa http://localhost/biblioteca (o el nombre de la carpeta que hayas usado).

El sistema debería mostrarse correctamente si todo está configurado bien.


9. Solucionar problemas comunes

Pantalla en blanco: Revisa los logs de Apache, normalmente están en:

XAMPP: C:\xampp\apache\logs\error.log

WAMP: C:\wamp64\logs\


Error de conexión a la base de datos: Revisa las credenciales de la base de datos en el archivo de configuración.


10. Acceder al sistema

Una vez que todo esté funcionando, deberías poder acceder al sistema, registrarte como usuario o administrador y gestionar los libros y préstamos.

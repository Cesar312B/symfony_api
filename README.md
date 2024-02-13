# symfony_api
Symfony API CRUD

-PHP 7.4 
-Mysql 10.4.27-MariaDB
Puedes instalar Xammp 3.3.0 para instalar estos componentes en Windows con el siguiente enlace:
https://sourceforge.net/projects/xampp/files/XAMPP%20Windows/7.4.33/xampp-portable-windows-x64-7.4.33-0-VC15.zip/download
-Postman
https://www.postman.com/downloads/
Instrucciones 
Primero instale Xammp descargando el archivo zip del primer enlace y descomprima su contenido en C:\

Tras la descompresión del archivo zip entre en la carpeta xammp y ejecute xammp dando clic en su archivo xammp-control.exe

Elija el idioma y se muestra una pantalla para iniciar los servicios web del servidor PHP.

Encienda los servicios de Apache y MySQL para probar el servidor web.




 Copie la carpeta user_api en la carpeta xammp/htdocs

Dentro de xammp-phpmyadmin importa la base de datos del proyecto dando clic en la cabecera de la página de administración de MySQL en la sección importar.







Para importar la base de datos elija el archivo usuarios.sql que se encuentra dentro de la aplicación (user_api/script/usuario.sql) y de clic en importar.

Nota si tiene una base de datos aparte puede configurar el archivo env en la siguiente línea para establecer la configuración de la base de datos de su preferencia.

DATABASE_URL=mysql://db_user:db_password@127.0.0.1:3306/db_name




Habrá su navegador y coloque esta dirección: http://localhost/user_api/ para abrir la aplicación.

Symfony 5.4 LTS(Versión de Largo Mantenimiento).
La aplicación tiene las funciones crud desarrolladas tanto de manera monolítica como a través de un api.
UsuarioController -> App Monolítica MVC con vistas twig.
ApiController->Api Crud con métodos Json 
App Monolítica 
El formulario de la sección monolítica de la app contiene validaciones para no mandar datos en null y el campo DNI y Celular solo aceptan números.
Como extra la app ya implementa Boostrap 5.3 y Jqery para mejorar el diseño de la app y mostrar los Datatables para listar los datos.


API Usuarios
Para poder probar la API debe tener instalado Postman y abrir el archivo json en la ruta (user_api/json/Symfony API.json) 
En el json ya se listan las funciones del crud para que pueda probar cada función.






En la función para agregar un usuario debe colocarse en la sección body y elegir la opción raw para crear una matriz que contenga los campos que se van a enviar a la base de datos.
http://localhost/user_api/api/usuariosCon la función editar repetimos el mismo procedimiento que en la función de crear agregando en la url el id del usuario que se va a editar.
http://localhost/user_api/api/edit_usuarios/6




Para eliminar un usuario en la url solo especificamos el id del usuario que vamos a eliminar
http://localhost/user_api/api/delete_usuarios/6


Nota: la aplicación está en modo producción así que no se requiere de ningún comando para levantarla, vasta con que este creada la base de datos y la carpeta user_api se encuentre dentro del servidor web para funcionar.


librerias complemetarias para crear api:<br> en Symfony 
Elao Json Form <br>
https://github.com/Elao/ElaoJsonHttpFormBundle<br>
Nelmio Cors<br>
https://github.com/nelmio/NelmioCorsBundle<br>
Tokens<br>
https://github.com/lexik/LexikJWTAuthenticationBundle<br>

composer require symfony/validator <br
composer require symfony/form <br
composer require symfony/orm-pack <br>
composer require symfony/maker-bundle







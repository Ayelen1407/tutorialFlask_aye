# tutorialFlask_aye
<!--
skr routes --- Te muestra todas las rutas que tienes definidas
venv --- es el entorno virtual

try --- prueba el siguiente renglon de codigo
pass --- no te corta el codigo (te lo pasa de largo)
EJEMPLO
try:
        os.makedirs(app.instance_path) -- tiraria error porque instance ya existe
    except OSError: -- en vez de tirar OSError
        pass -- lo deja pasar

finally --- garantiza que se ejecute el siguiente renglon de codigo
SECRET-KEY --- es lo que utiliza el flask
g --- es unico por cada conexión/pedido (es mas conveniente cuando se utiliza el flask)
with --- mecanismo de pytohn para abrir un recurso, ponerle un nombre a la variable, ejecuta el
         código y por ultimo se cierra
Blueprint --- organiza un grupo de vistas (la funcion que devuelve el htm) y otro codigo relacionado
              Tiene un nombre y un prefigo (no siempre coinciden el nombre del blueprint con el prefigo de la ruta)
IMPORTANTE --- en la aplicacion principal se deben registrar todas las vistas de Blueprint sino no apareceran al ejecutar "skr routes" en la terminal

SIGNIFICADOS
200 -- OK
302 -- FOUND > es redireccion
304 -- NOT MODIFIED > como un css sin cambios
404 -- NOT FOUND
500 -- INTERNAL SERVER ERROR > Respuesta posible para GET

generate_password_hash --- encripta la contraseña
*Poner claves en archivos es un error tipico
*El objeto g(global) existe hasta que termina el request
*Si se borra de la base de datos el usuario que esta logeado
*Si se borra las cookies el navegador no se entera a menos que recargues la página ()
que pasa si borro el usuario de la base de datos? en g.user se queda guardado None porque es como si *no estuviera logeado
*fetchall -- si no hay nada devuelve una lista vacia
*PLANTILLA -- puede contener datos estáticos o datos dinámicos
*extens(extiende) -- vincula un archivo(html) anterior con el actual/ una plantilla se puede conectar con otra
*como se convina dos html?
GIT
que es github? es una plataforma online que permite guardar repositorios
git log te muestra todos los cambios que se realizaron (el historial de los commits) desde la creación del repositorio(se puede hacer un checkout desde cualquier punto).Muestra el autor, fecha. mensaje
El ENCABEZADO es informacion extra que va con el pedido, tiene metodo,ruta y puede tener (tiene en general) encabezados > info que se ve en f12
request > puede mandar datos: nombre, contraseña
Los errores de flash() > se ubican en una lista de string, se crea una lista vacía de errores.Te permite agregar mensajes de errores a esa lista.
get_flashed_message > Es para obtener la lista. Te devulve todo lo que contiene la lista de flash()
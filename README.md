**********************************
# Koover description / Descripción
**********************************

Project 1st year Circo-bIt
Group composed of Camilo, Darío, Maite, Mathias and Victoria
//
Proyecto 1er año Circo-bIt
Grupo integrado por Camilo, Darío, Maite, Mathias y Victoria.


********************************************************
### Development environment / Ambiente de desarrollo ###
********************************************************
We will use conda as a virtual development environment. In your version 3.18.9
Django as a development framework in your version 2.0
MySQL in this latest version.
//
Utilizaremos conda como entorno virtual de desarrollo. En su version 3.18.9
Django como framework de desarrollo en su version 2.0.2
MySQL en su ultima versión.

### Instrucciones para poder crearlo ###
1- instalar anaconda.

2- Abrir anaconda powershell promp.

3- En la consola colocar el siguiente comando( conda create -n py36 python==3.6 ).

4- Una vez terminada la instalación ejecutar el siguiente comando (activate py36), para iniciar el ambiente de prueba.

5- Cuando este inicializado el ambiente instalaremos django 2.0.2 a través de pip ejecutando el siguiente comando (pip install django==2.0.2).

6- Ahora crearemos el proyecto Django Koover para poder ver exactamente estos recursos, unificarlos e ir actualizando el proyecto
EJECUTAMOS en la consola **IMPORTANTE= si quieren instalar el proyecto en una ruta especifica puede ejecutar el siguiente comando "cd C:\{aqui especifican el archivo ejemplo si esta en el escritorio y se llama koover la carpeta sera: C:\DESKTOP\koover} presionamos enter y allí ejecutamos el comando del proyecto"** (django-admin startproject koover).

7- Nos dirigimos a la carpeta user en nuestro pc buscamos a nuestro usuario ejempo MathiasPC y alli buscamos nuestro proyecto koover el cual al iniciarse contiene las siguientes carpetas:

/manage.py

../koover/

../koover/__init__.py

../koover/settings.py

../koover/urls.py

../koover/wsgi.py

8- Ahora podemos abrir nuestro editor de codigo de preferencia. (Recomendamos usar Visual estudio code ya que detecta el ambiente de desarrollo automaticamente, lo vemos en el borde inferior izquierdo del editor tenemos que abrir el archivo manage.py (Demora un poco en cargar el ambiente pero tendria que cargarles algo como esto "Python 3.7.6 (conda)"), cuando les aparezca el ambiente le vamos a dar click y en el buscador vamos a colocar py36 y le vamos a dar click. Se va a recargar la pagina y luego vamos a abrir la terminal.)

El resultado de este punto es:

Microsoft Windows [Versión 6.3.9600]
(c) 2013 Microsoft Corporation. Todos los derechos reservados.

C:\curso-python\koover>C:\ProgramData\Miniconda3\Scripts\activate C:\Users\MathiasPC\Anaconda3\envs\py36

(py36) C:\curso-python\koover>

9- Vamos a instalar un par de complementos uno de ellos sera el resaltador de codigo **pylint**

En la consola ya posicionados en nuestro ambiente vamos a colocar el siguiente comando:

conda install pylint

Presionamos enter y dejamos que la magia suceda. Luego le decimos que procesa presionando la tecla **Y**. 

*************************************************
### Descripcion de los archivos que instalo Django ###
*************************************************

**/manage.py** - Es un script que sirve para gestionar todo nuestro proyecto desde la conosola y lo vamos a usar un monton.

**../koover/** - Esta carpeta contiene todos los scripts iniciales de configuracion y de despliegue del proyecto.

**../koover/__init__.py** - El init nos indica que esta carpeta es un paquete 

**../koover/settings.py** - El settings es el que contiene la configuración del proyecto, es decir donde la magia sucede.

**../koover/urls.py** - Es el fichero encargado de manejar las urls de la web, direcciones amigables, etc.

**../koover/wsgi.py** - Contiene el codigo que desplegara nuestro proyecto en producción.

*****************************************************
### Comenzando a entender la cosa ###
*****************************************************
Una vez configurado el ambiente y entendiendo un poco más de que va la cosa, vamos a ver unas cositas importantes.
La primera es que pasa si ejecutamos desde la consola el archivo manage.py.

(Para poder hacerlo desde visual estudio code, vamos a pararnos arriba del archivo y con el botón derecho vamos a presionar run python file in terminal)

Este script contiene escondidos muchos comandos importantes que al realizar esta acción nos empieza a revelar un poco la cosa. 
A demas de abrirnos la carpeta raiz del proyecto (No se asusten jajaj).

Uno de los comandos importantes es runserver.

Ahora como desplegamos el servidor en nuestro entorno de desarrollo. 
Es algo simple, lo que vamos a tener que ejecutar en la consola de comandos de visual estudio code es un comando y vamos a colocarlo ***python manage.py runserver**** presionamos enter y vamos a ver que pasa!

Sí, ahora tenemos nuestro servidor local! Que divino y tambien vamos a tener unos archivos magicos que voy a estar describiendo más adelante. 

Por si no se dieron cuenta el localhost, servidor local se abre con la siguiente dirección: http://127.0.0.1:8000/
Podemos copiar la dirección o simplemente en la terminar apretar alt+click y nos abre el enlace en nuestro navegador de preferencia.

Otra cosa que les dije antes. Uno de los archivos magicos que crea es la base de datos db.sqlite3.

Cuando abrimos el servidor local vemos la bienvenida de Django a nuestro proyecto y tambien vemos que nos muestra que desde nuestro archivo settings esta activado el MODE DEBUG, que es correcto ya que lo desactivariamos unicamente en el modo de producción. Es decir cuando este funcional o en linea.

El archivo de la instalación inicial esta en inglés y porque el mio se ve en español. Porque le modifique una variable en la pagina settings. Modificando el "lenguaje_code='en-us'" por "LANGUAGE_CODE = 'es'"

Ahora volviendo a lo importante nosotros dijimos que ibamos a usar mysql como gestor de base de datos pero django trae por defecto a sqlite3 (son similares asi que vamos a utilizar la por defecto por ahora).

¿Que tenemos que hacer ahora para poder configurar la base de datos?
Acá fue donde me perdí un poco pero cuando realice la instalción de django en uno de los mensajes de la consola decia que la aplicacion no iba a funcionar correctamente hasta que no migrara los 14 archivos. "You have 14 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them." Enconces bueno hay que aplicar esa configuración.

Tenemos que pausar el servidor presionando control+c y luego aplicamos el comando ***python manage.py migrate*** presionamos enter y dejamos que la magia suceda.

OK, todo muy lindo pero ¿Por qué elegimos DJango?
Porque Django va a instalar estas APPS que nos permiten optimizar y reutilizar codigo de una manera asombrosa (Me estoy enamorando de esto! me preocupa el despliege pero esto es simplemente un parentesis no me hagan caso).

Donde vemos estas apps que instalamos las vemos luego de ejecutar el comando manage.py migrate en el archivo settings.py en el diccionario creado llamado 

**INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]**

Acá es donde vamos a modularizar las apps que vamos a ir creando es decir las funciones que las podemos ir reutilizando! 

Entonces que vamos hacer ahora el nucleo de nuestra aplicación, el core.

Para poder hacerlo vamos a ir a nuestra consola y vamos a escribir python manage.py startapp core 
Luego de realizado esto es que se crea la carpeta **CORE**.

El core tiene nuevos ficheros que se corresponden a la libreria de las apps, pero de estos ficheros el mas importante es el views.py que es el que voy a empezar a utilizar.
Lo voy a empezar a utilizar porque es aca donde se definen las vistas de la app.

Lo primero que cree fue el importador del HttpResponse, voy a empezar a crear las vistas y luego desde el archivo urls.py y voy a importar las vistas. 
¿Como importo las vistas? lo realizo colocando el siguiente codigo: from core import views (Es decir realizo la importación).
Luego coloco el path que se coloca dentro desde las URLPATTERS, llamando al parche (path). path('', views.home, name="home")
Esta vista creada de ejemplo es el HOME el nuevo INICIO.

Conociendo a donde tenemos que empezar a realizar los cambios lo que vamos a comenzar a hacer es a intervenir el CORE para que de esta manera podamos ejecutar cada una de nuestras vistas es decir nuestros archivos HTML creados anteriormente. 
Para eso tomo a Koover.uy/beta como punto de referencia funcional y empiezo a llamar a los archivos

Index.html ahora Inicio.html
Login.html 
Registro.html
Nosotros.html

y de esta manera lo hacemos con todos los archivos.


### Sobre los templates ###
Ahora luego que vimos toda la parte funcional y sabiendo que ya tenemos hecha toda la estructura lo que se procede a realizar es a llamar a los templates. 
Los templates estan ubicados en la carpeta core/templates. Para de esta manera seguir la logica del modelo controlador, modelo y template (CMT o controlador, modelo y vista. Controlador y modelo forman parte del backend y vista el front.)

Ahora como estamos trabajando con django tenemos que crear una carpeta core dentro de la carpeta templates, para de esta manera continuar respetando la logica del framework. Entonces lo que hacemos es colocar todos los archivos HTML dentro de la carpeta ***templates/core/***
Logica:

Cada uno de los templates desde el archivo de las vistas fue llamado al archivo de las urls.py y es definido y rotulado.

La función para declarar las plantillas es:

***def tpsicologos(request):
    return render(request,"core/terapeuticos-psicologos.html")
	***
	
#### Herencia en las plantillas ####
Como ya sabran en programación cuando estamos repitiendo el codigo es porque algo estamos haciendo mal, y sí, lo hemos estando realizado mal. El motivo era claro, se debía a que html es un leguaje estructural e inmutable pero con Django la historia es otra.
Lo que realizaremos es la creacion de los bloques de contenido que lo vamos a ver modularizado en el nuevo archivo creado llamado template.html. El cual se va a estar extendiendo a lo largo de todas las plantillas.

¿Como se crea una extención o un bloque de contenido?

Lo estaremos creando con el siguiente código {% block content %} {% endblock %}, el cual es creado en la plantilla eliminando lo que seria el contenido dinamico.
Que realiza este bloque una extencion en una plantilla fija. En otras palabras, en la plantilla.html dejamos los elementos que vamos a mostrar de manera permanente en todos nuestros archivos html y extendemos el bloque a las plantillas que queremos optimzar el codigo.

Para extender tenemos que utilizar el bloque extends llamandolo {% extends 'core/plantilla.html' %} y colocando el contenido dinamico de nuestras plantillas como la de la pagina de incio dentro del bloque. {% block content %} codigo html {% endblock %}

Los únicos archivos templates html que son diferentes al resto de los archivo son el login y el registro.


***********************************************
###  Create functions // Funciones a desarrollar ### 
***********************************************

1- Register and login to profile users area // Registro y login hacia el area del perfil de usuario.

2- Search and request info of kooveters // Buscar y solicitar información de los kooveters.

3- Filter koover category by require of the final users //  Flitrar categorias de kooveters por la solicitud requerida por el usaurio final.

4- Create a chat to start a conversation with the kooveters // Crear un chat para hablar con los kooveters cuando sea necesario.

******************************************************************************************
### Important info  and contact info/ Información importante e información de contacto ### 
******************************************************************************************

PCNAME de desarrllo padre MATHIAS PC.
PCNAMES de prueba CAMILO, DARIO, MAITE y VICTORIA.

Referente del grupo Darío Finelli = @dariofin
Unificación de versiones a cargo de Mathias Alvez = @msalvez
Desarrolladores de ambientes de prueba = Maite Navratil(@maitomomi), Victoria Flores(@VitoFlores) y Camilo Mandressi(@camilomandressi).

*********************
### CONTROL LOGS ### 
*********************

***07/03 - 15:30: Cambio de la estructura general del proyecto (Mathias A.)***

1- Se remplazan carpetas por las carpetas a utilizar en la version final del proyecto.







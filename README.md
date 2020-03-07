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
### Descripcion de los archivs que instalo Django ###
*************************************************

**/manage.py** - Es un script que sirve para gestionar todo nuestro proyecto desde la conosola y lo vamos a usar un monton.

**../koover/** - Esta carpeta contiene todos los scripts iniciales de configuracion y de despliegue del proyecto.

**../koover/__init__.py** - El init nos indica que esta carpeta es un paquete 

**../koover/settings.py** - El settings es el que contiene la configuración del proyecto, es decir donde la magia sucede.

**../koover/urls.py** - Es el fichero encargado de manejar las urls de la web, direcciones amigables, etc.

**../koover/wsgi.py** - Contiene el codigo que desplegara nuestro proyecto en producción.


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







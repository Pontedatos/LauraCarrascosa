# Documentar el proceso de aprendizaje de clase

A continuación, voy a hacer un resumen de todo lo realizado durante todas las clases de la asignatura Periodismo de datos. 

## 1. Instalación de un programa de emulación de la terminal
Durante el curso, teniendo como sistema operativo Windows, hemos instalado dos terminales diferentes. 

Lo primero que hicimos para poder comenzar esta asignatura fue instalarnos Ubuntu, una virtualización de Linux, terminal que no conseguí instalar, a pesar de seguir todos los pasos. Por tanto, instalé la terminal Git Bash, [según la página oficial]( https://gitforwindows.org/) que es una emulación de BASH que se usa para ejecutar Git desde la línea de comandos. 

Para visualizar todos los pasos que hemos hecho en dicha terminal, se ha abierto el documento del historial con el siguiente comando “cat .bash_history”. 

El segundo programa instalado fue Cygwin, es un emulador de los sistemas Unix para Windows. 

Las dos terminales se instalaron desde la descarga del ejecutable de las páginas oficiales. El ejecutable de GitBash se llama Git-2.35.1.2-64-bit y el de Cywing setup-x86_64.exe.

A la hora de ejecutar el .exe de cada programa como administradores, nos aparece un cuadro de diálogo que nos guía todo el proceso de instalación. Como todo programa nos indica en qué unidad del ordenador queremos instarlarlo y seleccionamos la Unidad C:.

GitBash se instaló siguiendo los pasos del cuadro de diálogo. 
Cygwin por otra parte, antes de finalizar la instalación, teníamos que instalar una serie de paquetes que fueron los siguientes: libcurl4, wget, ca-certificates-letsencrypt, lynx, nano y openss. Se seleccionó la ultima versión de cada paquete. Con todos estos pasos, finalizamos la instalación de las dos terminales. 

## 2. Configuración del programa

Lo primero que hicimos fue meternos en nuestra carpeta local de Periodismo de datos con el comand cd Documents/Universidad/5º/2º\ cuatri/Periodismo\ de\ Datos/. A continuación, miramos el contenido de la carpeta con el comando ls y creamos una nueva carpeta con mkdir llamada “laura-carrascosa”. Después nos metimos en la carpeta, de nuevo con el comando cd.

Primero se estableció alias micasa y se igualó a la dirección de carpeta que queríamos (alias micasa="cd Documents/Universidad/5º/2º\ cuatri/Periodismo\ de\ Datos/"). A continuación con el comando echo establecemos que la terminal sepa cuál es la home, entonces hicimos “echo $home” y luego lo hacemos con nuestra carpeta de periodismo de datos: “echo "alias micasa='cd Documents/Universidad/5º/2º\ cuatri/Periodismo\ de\ Datos/'”. Después, abrimos el el archivo nano (nano $HOME/.bashrc) y escribimos lo siguiente: 
#Aqui creo un alias para ir a mi directorio de trabajo en clase
alias micasa="cd Documents/Universidad/5º/2º\ cuatri/Periodismo\ de\ Datos/"
Esto es para que la terminal guardase la dirección. 

En Cywing seguimos el mismo procedimiento. 
Primero se estableció alias micasa y se igualó a la dirección de carpeta que queríamos (alias micasa="cd Documents/Universidad/5º/2º\ cuatri/Periodismo\ de\ Datos/"). A continuación con el comando echo establecemos que la terminal sepa cuál es la home, entonces hicimos “echo $home” y luego lo hacemos con nuestra carpeta de periodismo de datos: “echo "alias micasa='cd Documents/Universidad/5º/2º\ cuatri/Periodismo\ de\ Datos/'”. Después, abrimos el el archivo nano (nano $HOME/.bashrc) y escribimos lo siguiente: 
"# Aqui creo un alias para ir a mi directorio de trabajo en clase
alias micasa="cd Documents/Universidad/5º/2º\ cuatri/Periodismo\ de\ Datos/""
Esto es para que la terminal guardase la dirección. 

"# Aqui creo un alias para ir a mi directorio de trabajo en clase
alias micasa="cd Documents/Universidad/5º/2º\ cuatri/Periodismo\ de\ Datos/""

### Configurar GitHub
El paso siguiente fue clonar nuestro repositorio personal con el comando git clone https://github.com/lauracarrascosa99/practica1_periodismodatos.git practica-1. Una vez, trasladado nuestro repositorio a nuestro archivo local, abrimos el archivo README.md con el comando cat. También editamos el texto con nano. Luego establecimos nuestra carpeta de periodismo de datos como nuestra home predeterminada.
Empleamos “git init” para copiar todas las propiedades de la carpeta de github a nuestro repositorio del ordenador. Posteriormente, configuramos el nombre de usuario y el correo electrónico git config --global user.name git config --global user.email.
Y después, configuramos para que nuestro editor de texto sea nano en nuestra terminal Git Bash. Lo realizamos con el comando git config --global core.editor nano.



## 3. Configuración de un programa de edición de texto
Para poder configurar el programa de edición de texto, en nuestro caso, nano con el archivo de configuración. Para ello, abrimos el archivo nano de configuración: nano $HOME/.nanorc (en Git Bash) y nano /c/Users/LAURA/ .nanorc (en Cygwin) y ponemos lo siguiente: 
Git Bash: 
"## Spread overlong lines over multiple screen lines.
set softwrap"
"## Display line numbers to the left of the text.
set linenumbers"
 
 
 
 
Podemos editar el comportamiento de nuestro editor de texto nano a través de su archivo de configuración. En nuestro caso, vamos a hacer que se ajuste el texto a la resolución de la pantalla y que aparezca el número de las líneas para poder visualizar y localizar mejor el contenido del archivo. Para ello, lo editamos de la siguiente forma: nano $HOME/.nanorc y ponemos lo siguiente:
"# Ajustar el texto a pantalla
set softwrap"
"# Numerar las líneas
set linenumbers"
## 4. Configuración y funcionamiento de un gestor de paquetes/programas del emulador de la terminal. 
Primero antes de adentrárnos en este punto, voy a definir qué es un gestor de paquetes. [Según OpenWeibnars](https://openwebinars.net/blog/que-es-un-paquete-en-linux-y-que-gestores-existen/) es el conjunto de herramientas que facilitan el proceso de instalación y muestran la información de los paquetes y dependencia. 
En el caso de GitBash y Cygwin, el gestor de paquetes es apt-cyg. Un APT (Advanced Package Tool) es un conjunto de herramientas que permite manejar los paquetes de los sistemas. 
En nuestro caso, hemos instalado apt-cyg install tree (esta es para que la información salga mostrada en forma de árbol) y apt-cyg install git. apt-cyg install ruby y gem instal lolcat, este último en cygwin.

## 5. Versión del lenguaje de SHELL utilizado.
Según los apuntes de Periodismo de Datos, Shell es el lenguaje que emplea la terminal. Para comprobar cuál es en GitBash ejecutamos el comando echo $0 y nos encontramos que es el siguiente: /usr/bin/bash. Para saber qué versión de Bash está manejando lo hacemos con el comando “bash -help” y nos da la información: GNU bash, version 4.4.23(2)-release-(x86_64-pc-msys). 
En Cygwin realizamos los mismos pasos:
Ejecutamos el comando echo $0 y nos dice que el lenguaje es:  -bash
Después ponemos “bash -help” y nos da la versión de Bash de Cygwin GNU bash, version 4.4.12(3)-release-(x86_64-unknown-cygwin)
 
 
## 6. Valor de la variable de entorno PATH
Para poder consultar la variable de entorno PATH lo ejecutamos con el comando “echo $PATH” que nos da la información de donde está la ruta de la terminal instalada en nuestro ordenador. 
### PATH GitBash
echo $PATH
/c/Users/LAURA/bin:/mingw64/bin:/usr/local/bin:/usr/bin:/bin:/mingw64/bin:/usr/bin:/c/Users/LAURA/bin:/c/Program Files (x86)/Intel/Intel(R) Management Engine Components/iCLS:/c/Program Files/Intel/Intel(R) Management Engine Components/iCLS:/c/WINDOWS/system32:/c/WINDOWS:/c/WINDOWS/System32/Wbem:/c/WINDOWS/System32/WindowsPowerShell/v1.0:/c/WINDOWS/System32/OpenSSH:/c/Program Files (x86)/Intel/Intel(R) Management Engine Components/DAL:/c/Program Files/Intel/Intel(R) Management Engine Components/DAL:/c/Program Files/dotnet:/c/Program Files (x86)/Calibre2:/cmd:/c/Users/LAURA/AppData/Local/Microsoft/WindowsApps:/usr/bin/vendor_perl:/usr/bin/core_perl:/cygdrive/c/Users/LAURA/bin:/cygdrive/c/Users/LAURA/bin
 
### PATH Cygwin
echo $PATH
/usr/local/bin:/usr/bin:/cygdrive/c/Program Files (x86)/Intel/Intel(R) Management Engine Components/iCLS:/cygdrive/c/Program Files/Intel/Intel(R) Management Engine Components/iCLS:/cygdrive/c/WINDOWS/system32:/cygdrive/c/WINDOWS:/cygdrive/c/WINDOWS/System32/Wbem:/cygdrive/c/WINDOWS/System32/WindowsPowerShell/v1.0:/cygdrive/c/WINDOWS/System32/OpenSSH:/cygdrive/c/Program Files (x86)/Intel/Intel(R) Management Engine Components/DAL:/cygdrive/c/Program Files/Intel/Intel(R) Management Engine Components/DAL:/cygdrive/c/Program Files/dotnet:/cygdrive/c/Program Files (x86)/Calibre2:/cygdrive/c/Program Files/Git/cmd:/cygdrive/c/Users/LAURA/AppData/Local/Microsoft/WindowsApps:/cygdrive/c/Users/LAURA/bin
 
## 7. Comandos utilizados y ejemplos.
A continuación, se muestra una lista de comandos utilizados a lo largo del curso: 
- **pwd**: nos indica en qué carpeta o directorio nos encontramos. Por ejemplo: /c/Users/LAURA/Documents/Universidad/5º/2º cuatri/Periodismo de Datos
- **cd**: nos permite movernos a unn directorio diferente al que estamos. Por ejemplo si quiero entrar a la carpeta que está vinculada a mi repositorio de github (estando dentro de la ruta anterior) escribo el comando cd y escribo el nombre del directorio: cd laura-carrascosa/. Sin embargo, si quiero volver al directorio anterior, tenemos que poner “cd -”.
- **ls**: con este comando nos muestra o lista el interior de una carpeta de un directorio. 
- **nano**: es el comando con el que se nos abre el editor de texto nano y podemos editar archivos markdown 
- **mkdir**: con él podemos crear carpetas.

- **cat**: dicho comando sirve para concantenar o unir archivos. También tiene una doble función que es visualizar los archivos markdown. 
- **mv**: su función es mover un archivo de un origen a otro destino diferente.
- **echo**: con este comando, podemos decirle a la terminal que nos diga una serie de palabras y nos lo devolverá escrito poniendo echo “hola mundo”, la terminal te responde lo que has escrito entre comillas:
LAURA@LAPTOP-CK2VU2S6 ~
$ echo "hola mundo"
hola mundo
También nos puede decir cuál es nuestra home poniendo echo $HOME: 
$ echo $HOME
/cygdrive/c/Users/LAURA
- **cp**: nos permite copiar archivos de una carpeta origen a otra destinataria. 
- **git init**: traslada las características de nuestro repositorio de Github a nuestra carpeta local del ordenador. 
- **whoami**: la terminal te devuelve quién eres. 
$ whoami
LAURA
- **Git clone**: se clona el repositorio en tu carpeta local del ordenador. Ejemplo: git clone https://github.com/lauracarrascosa99/practica1_periodismodatos.git practica-1
Pasos para subir archivos a github desde la terminal
- **Git status**: te indica el estado en el que está el repositorio de GitHub: archivos eliminados, archivos que faltan por subir…
- **Git add**: para subir los archivos.
- **Git commit -m**: se indica los cambios que se han realizado en los archivos. Ejemplo: git commit -m “subir Documentar el proceso de aprendizaje de clase”
- **Git pull**: Sirve para actualizar el repositorio con todos los cambios que hemos hecho anteriormente. 
- **Git push**: este comando nos pide el nombre de usuario y el token para poder subir todos los archivos y cambios realizados. 

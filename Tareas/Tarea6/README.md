# Instalación de JDK en el SO
## índice:
- Introducción
- ¿Cómo instalar Java en Ubuntu desde repositorios?
- ¿Cómo instalar una versión específica de Java?
- Configuración de las variables de entorno
- Listar la versiones de OpenJDK instaladas
- Actualización de las variables de entorno
---
### Introducción
Java sin dudas es un lenguaje de programación que es utilizado para diversos propósitos y es un complemento casi esencial para la ejecución y funcionamiento de diversas herramientas, la instalación de java es prácticamente una tarea esencial después de haber realizado la instalación de este.

### ¿Cómo instalar Java en Ubuntu desde repositorios?
Lo primero debemos de actualizar el sistema con el siguiente comando:

    sudo apt-get update
e instalamos Java con este comando:

    sudo apt-get install default-jdk


    Después comprobamos que tenemos instalado Java en nuestro sistema con solo ejecutar:

    java --version

![<Imagen 1>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%201.png>)

![<Imagen 2>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/captura%202.png>)

![<Imagen 3>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%203.png>)

![<Imagen 4>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%204.png>)

![<Imagen 5>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%205.png>)

![<Imagen 6>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%206.png>)

![<Imagen 7>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%207.png>)

![<Imagen 8>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%208.png>)

### ¿Cómo instalar una versión específica de Java?
Para instalar Ubuntu Java Open JDK debemos realizar los siguientes pasos:
- OpenJDK: 
    - 11

            sudo apt install openjdk-11-jdk
    - 13
    
            sudo apt install openjdk-13-jdk
    - 8
            
            sudo apt install openjdk-8-jdk
La versión que se debe de trabajar es la versión 8. Para ello verificaremos la versión de java que se esta ejecutando con la sentencia:

    java --version    
En caso que no se ejecuta la versión 8 se debe configurar las variables de entorno.

![<Imagen 8>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%208.png>)

![<Imagen 9>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%209.png>)

![<Imagen 10>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%2010.png>)

![<Imagen 11>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%2011.png>)

![<Imagen 12>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%2012.png>)

![<Imagen 13>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%2013.png>)

###  Configuración de las variables de entorno
En mi caso tuve que cambiar a la versión 8 con las variables de entorno, como se muestra a continuación. 

Este paso es necesario porque cuando se usa Java, Linux necesita saber dónde está ubicado el programa para ejecutarlo y qué versión de Java usar de forma predeterminada. Para modificar esto, usaremos el editor de texto nano. Primero, abra el archivo en Nano.
### Listar la versiones de OpenJDK instaladas
A continuación se ejecuta el siguiente comando para verificar que se han descargado las diferentes versiones de OpenJDK.
    
    ls /usr/lib/jvm
### Actualización de las variables de entorno
Luego se edita y se modifica el fichero profile, con los comandos:

    sudo update-alternatives --config java

y selecciona la version 8.

![<Imagen 13>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%2013.png>)

En mi caso no hago los siguentes pasos porque con el primero me funcionó correctamente. Pero en el caso que no funcione se tendrá que realizar los pasos siguientes:

    JAVA_HOME=/usr/lib/jvm/(SELECCIONA UN PATH DE LA VERSION QUE DESEAS QUE SE EJECUTE)
    PATH=$PATH:$HOME/bin:$JAVA_HOME/bin
    export JAVA_HOME
    export JRE_HOME
    export PATH
en 
    
    sudo nano /etc/profile.d/java.sh

Para hacer que el script sea ejecutable con chmod hay que ejecutar el sisguiente comando:

    sudo chmod +x /etc/profile.d/java.sh
Finalmente, hay que cargar las variables de entorno usando el comando de source:
        
        source /etc/profile.d/java.sh
![<Imagen 13>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea6/img/Captura%2014.png>)
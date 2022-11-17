# Instalación de MAVEN en el Ubuntu

## Índice:
- Introducción
- Instalar Apache Maven
    - Instalar Apache Maven con apt
    - Instalar una versión concreta de Apache Maven
        - Establcer variables de entorno
- Verificar la instalación

## Introducción
Apache Maven es una herramienta de gestión y comprensión de proyectos de código abierto que se utiliza principalmente para proyectos Java. Maven usa un modelo de objetos de proyecto (POM), que es esencialmente un archivo XML que contiene información del proyecto, detalles de configuración, dependencias del proyecto y más.

## Instalar Apache Maven

### · Instalar Apache Maven con apt
Instalar Maven en Ubuntu usando apt es un proceso simple y directo.

Primero hay que actualizar el índice del paquete e intalar Maven ingresando los siguientes comandos:

    sudo apt update
    sudo apt install maven

![<imgen 1>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea10/img/Instalar%20Maven%20part%201.png>)

![<imgen 2>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea10/img/Instalar%20Maven%20part%202.png>)

![<imgen 3>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea10/img/Instalar%20Maven%20part%203.png>)

![<imgen 4>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea10/img/Instalar%20Maven%20part%204.png>)

![<imgen 5>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea10/img/Instalar%20Maven%20part%205.png>)

![<imgen 6>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea10/img/Instalar%20Maven%20part%206.png>)

![<imgen 7>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea10/img/Instalar%20Maven%20part%207.png>)

Para vereficar la instalación tendremos que ejecutar 

     mvn -version

![<imgen 8>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea10/img/Instalar%20Maven%20part%208.png>)

La salida obtenida debería de verse de la siguiente manera:

    Apache Maven 3.6.3
    Maven home: /usr/share/maven
    Java version: 11.0.7, vendor: Ubuntu, runtime: /usr/lib/jvm/java-11-openjdk-amd64
    Default locale: en_US, platform encoding: UTF-8
    OS name: "linux", version: "5.4.0-29-generic", arch: "amd64", family: "unix"

### ·Instalar una versión concreta de Apache Maven
La versión que instalamos anteriormente es la versión 3.6.3, pero nosotros queremos instalar una versión más actualizada, como la 3.8.6. 
para ello podemos descargarlo en el directorio /temp con el siguiente comando:

    wget https://www.apache.org/dist/maven/maven-3/3.8.6/binaries/apache-maven-3.8.6-bin.tar.gz -P /tmp

Una vez que se complete la descarga tendremos que estraer el archivo en el directorio /opt con el siguiente comando:

    sudo tar xf /tmp/apache-maven-*.tar.gz -C /opt

Para teber más control sobre las actualizaciones de Maven, tendremos que crear un enlace simbólico que apunte al directorio de instalación de Maven. Esto se hace con el siguiente comando:

    sudo ln -s /opt/apache-maven-3.8.6 /opt/maven

sudo ln -s /opt/apache-maven-3.8.6 /opt/maven

Cuando se lanza una nueva versión, puede actualizar su instalación de Maven desempaquetando la última versión y cambiando el enlace simbólico para señalarla.

#### * Establecer variables de entorno
 A continuación, necesitaremos establecer las variables de entorno. Para hacer esto, abra su editor de texto y cree un nuevo archivo llamado mavenenv.sh en el directorio /etc/profile.d/. Esto se puede realizar con el siguiente comando:

    sudo nano /etc/profile.d/maven.sh

Una vez abierto el archivo tendremos que pegar el siguiente código:

    export M2_HOME=/opt/maven
    export MAVEN_HOME=/opt/maven
    export PATH=${M2_HOME}/bin:${PATH}

Una vez finalizado tendremos que guardar y cerrar el archivo. Este script se utilizará al iniciar el shell.

Para hacer que el script sea ejecutable con chmod hayq ue realizar el siguiente comando:

    sudo chmod +x /etc/profile.d/maven.sh

Finalemente hay que cargar las variables de entorno usando el comando de source:

    source /etc/profile.d/maven.sh

## Verificar la instalación
Para verificar que Maven está instalado, use el mvn -version que imprimirá la versión de Maven:

    mvn -version

Debería ver algo similar a lo siguiente:

    Apache Maven 3.8.6 (cecedd343002696d0abb50b32b541b8a6ba2883f)
    Maven home: /opt/maven
    Java version: 11.0.7, vendor: Ubuntu, runtime: /usr/lib/jvm/java-11-openjdk-amd64
    Default locale: en_US, platform encoding: UTF-8
    OS name: "linux", version: "5.4.0-29-generic", arch: "amd64", family: "unix"

Eso es todo. La última versión de Maven ahora está instalada en su sistema Ubuntu.
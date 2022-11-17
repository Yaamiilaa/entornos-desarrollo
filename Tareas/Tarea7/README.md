# Instalación del IDE Netbeans 12

## Índice:
- Instalación
- Ejecutando Netbeans
- Instalación a través de wget (Cualquier distribución de Linux)

### Instalación
Los paquetes Snap son paquetes de software universales prediseñados que se envían con las bibliotecas y dependencias requeridas por el paquete de software. Son independientes de la distribución y se pueden instalar en cualquier distribución principal de Linux. Los snaps son populares ya que no requieren ninguna dependencia durante la instalación, lo que hace que el proceso de instalación sea fluido y sin errores.

Para instalar la edición Netbeans, hay que ejecutar el siguiente comando:

    sudo snap install netbeans --classic

La instalación finalizará con el siguiente mensaje:

    netbeans 12.5 from Apache NetBeans✓ installed

### Ejecutando Netbeans 12
Ahora que Netbeans está instalado en su sistema Ubuntu, podemos iniciarlo escribiendo netbeans en su terminal o haciendo clic en el icono de Netbeans ( Activities -> Netbeans ).

### Instalaión a través wget (Cualquier distribución Linux)
Teniendo en cuenta que hemos completado la instalación de java en la tarea anterior, podemos realizar la instalación de Netbeans 12.5 a través de wget. De esta forma se podemos realizar la instalación en cualquier distribución de linux.

Los pasos son los siguientes:
- Navegando hasta la página de descarga de NetBeans IDE y descargando el último script de instalación de NetBeans IDE ( Apache-NetBeans-12.5-bin-linux-x64.sh ) para su distribución de Linux instalada.

Alternativamente, también podemos descargar el script de instalación de NetBeans IDE en su sistema a través de la utilidad wget, con el siguiente código:

    wget -c  https://archive.apache.org/dist/netbeans/netbeans/12.5/Apache-NetBeans-12.5-bin-linux-x64.sh

- Una vez completada la descarga, navegamos hasta el directorio donde se descargó el instalador de NetBeans IDE y ejecutamos el siguiente comando para que el script del instalador sea ejecutable y comazamos a instalarlo. 

Para ellos tenemos que otorgar permisos de ejecución con el siguiente comando:

    chmod +x Apache-NetBeans-12.5-bin-linux-x64.sh 

Una vez realizado este comando tenemos que ejecutar el script de instalación. 

    ./Apache-NetBeans-12.5-bin-linux-x64.sh

Por últimos, tenemos que ejecutar el script de instalación anterior, la “ Página de bienvenida ” del instalador se deben de seguir los pasos para personalizar la instalación (lenguajes soportados, etc).


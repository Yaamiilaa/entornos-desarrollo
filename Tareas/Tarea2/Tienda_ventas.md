# Tienda de ventas
## Índice:
- Enunciado.
- Análisis de requerimientos del sistema.
- Diseño.
- Codificación.
- Pruebas.
- Documentación.
- Explotación. 
- Mantenimiento. 
---
## Enunciado
La empresa Puerto Systems ha recibido un nuevo encargo de software.

Se trata de diseñar una aplicación para una tienda especializada en vender productos estéticos.

La tienda desea trabajar con software libre. Además, desea explícitamente que la aplicación sea capaz de cumplir las siguientes tareas:

Proporcionar facturas de las ventas.
Llevar la cuenta de lo que vende cada trabajador.
Controlar el stock de productos en almacén.
Operar con lector de código de barras y tarjetas de crédito.
Controlar los precios de los productos y ofrecer la posibilidad de operar con ellos.
El tiempo de respuesta de la aplicación ha de ser lo menor posible.
No se podrán procesar dos peticiones a la vez, aunque haya varios equipos funcionando simultáneamente.
La empresa también quiere almacenar información de sus trabajadores: DNI, nombre, apellidos, número de la Seguridad Social, fecha de nacimiento, teléfono y localidad. Asimismo, de los productos interesa almacenar: código, marca, nombre comercial, precio, cantidad.

Tendrás que diseñar una planificación del proyecto de desarrollo de ese software que cumpla con las premisas estudiadas en la presente unidad de trabajo.

Esencialmente, el proyecto se divide en los siguientes apartados:

Sintetiza el análisis de requerimientos del sistema para nuestro cliente.
Plantea el diseño y determina el modelo de ciclo de vida más idóneo para esta aplicación.
Planifica la codificación, indicando el lenguaje de programación y las herramientas que usarías para la obtención del código fuente, objeto y ejecutable, explicando por qué eliges esas herramientas.
Planifica las restantes fases del ciclo de vida, indicando en cada una el objetivo que persigues y cómo lo harías.

## Análisis de requerimientos del sistema
Comenzaremos nuestro análisis de requisitos del sistema detallando los requisitos funcionales y no funcionales del sistema.
Los requisitos funcionales podemos describirlos como las funciones que tendrá que realizar nuestra aplicación. En este caso son las siguientes:
- Proporcionar facturas de las ventas.

    - Operar con un módulo de lector de código de barras
    - Usar un módulo de lector de tarjetas de crédito.

- Llevar un control de ventas por empleado.
- Controlar el stock de productos que tienen en el almacén.
- Controlar los precios de los productos y ofrecer la posibilidad de operar con ellos.
- Almacenar información de los trabajadores (DNI, nombre, apellidos, número de la seguridad social, fecha de nacimiento, teléfono, y localidad).
- Almacenar información de los productos (código, marca, nombre comercial, precio, y cantidad).
Los requisitos no funcionales son la características que debe tener el programa al completos obviando los datos. Para nuestro caso serían las siguientes:
- Reducir el tiempo de respuesta de la aplicación, intentaremos obtener unos tiempos de respuesta que se adapten a las necesidades del cliente.
- Impedir el uso de dos peticiones simultáneamente, aunque hayan varios equipos trabajando al mismo tiempo.

Después de esto, planificaremos una serie de reuniones periódicas con el cliente con el fin de precisar cada uno de los requerimientos a desarrollar y comprobar las características hardware del equipamiento informático de nuestro cliente. Es fundamental una buena comunicación entre el analista y el cliente para que la aplicación que vamos a desarrollar cumpla con sus expectativas.
## Diseño
Una vez que tenemos perfectamente claro lo que nuestra aplicación debe hacer tras haber mantenido las comunicaciones con el cliente podemos proceder con el diseño de la misma.

Para este proyecto hemos decidido usar un modelo de ciclo de vida del programa Evolutivo, más concretamente el Modelo Iterativo Incremental, ya que debemos tener en cuenta la naturaleza cambiante y evolutiva del software.

La idea es comenzar con una implementación simple de los requerimientos del sistema, e iterativamente mejorar la secuencia evolutiva de versiones hasta que el sistema completo esté implementado. En cada iteración realizaremos cambios en el diseño y agregaremos nueva funcionalidades y capacidades al sistema dependiendo de las necesidades del cliente/usuario.
En cuanto al sistema gestor de Bases de Datos hemos decido usar MySql ya que es un sistema relacional y además se puede utilizar como software libre.
Las entidades y relaciones de la base de datos serán las siguientes:
- **Trabajadores**: dni (único), nombre, apellidos, nSegSocial, nacimiento, teléfono y dirección.
- **Clientes**: dni (único) nombre, apellidos, teléfono y dirección.
- **Facturas**: código (único), cod_cliente, dni_empleado, productos, precio y descuento.
- **Productos**: código, nombre, descripción, cantidad y precio.
## Codificación
En este apartado codificaremos toda la información que hemos visto anteriormente y la llevaremos a código fuente. Esta tarea la realizara el programador que además deberá cumplir con todos los datos impuestos en las etapas de análisis y diseño.
El Lenguaje de programación que vamos a utilizar es JAVA, ya que se adapta las necesidades del cliente al ser un software libre y también a nuestras necesidades al ser un lenguaje de programación orientado a objetos, mediante el cual desarrollaremos un código reutilizable, más fácil de mantener y modular.

Con el entorno de desarrollo NetBeans , al ser un entorno completo, cubriremos las tres partes de la codificación:
1. **Código Fuente**: Será tarea de los programadores desarrollar este
código en el entorno de desarrollo NetBeans utilizando el editor de código.
2. **Código Objeto**: Utilizando el compilador de NetBeans obtendremos el código binario resultante de compilar el código fuente.
3. **Código ejecutable**: Este código es el resultado de enlazar los archivos objeto, consta de un único archivo que puede ser ejecutado por el sistema operativo directamente. Este paso también lo realizaremos con la aplicación NetBeans.
## Pruebas
Esta fase consistirá en realizar una serie de pruebas para asegurar la validación y verificación del software desarrollado. Se dividirá en dos partes:
- **Pruebas unitarias**: En esta parte probaremos los diferentes módulos del software para comprobar su funcionamiento de manera independiente.
- **Pruebas de integración**: En esta parte probaremos el sistema completo con todas sus partes interrelacionadas.

Para finalizar esta fase del proyecto realizaremos una prueba final denominada BETA TEST, la cual realizaremos en el entorno de producción donde la aplicación va a ser utilizada por el cliente.
## Documentación
En esta fase desarrollemos la documentación necesaria para que todas las etapas queden perfectamente documentadas.
En concreto crearemos tres grandes documentos:

- **Guía técnica**: donde quedará reflejado el diseño de la aplicación, la codificación de los programas y las pruebas realizadas. Esta guía irá dirigida al personal técnico en informática (analistas y programadores) con el objetivo de facilitar un correcto desarrollo, realizar correcciones en los programas y permitir un mantenimiento futuro.

- **Guía de uso**: donde quedará reflejada la descripción de la funcionalidad de la aplicación, la forma de comenzar a ejecutar la aplicación los ejemplos de uso del programa los requerimientos software de la aplicación y la solución de los posibles problemas que se pueden presentar. Esta guía irá dirigida a los usuarios que van a usar la aplicación (clientes) con el objetivo de dar a los usuarios finales toda la información necesaria para utilizar la aplicación.

- **Guía de instalación**: donde quedará reflejada toda la información necesaria para la puesta en marcha de la aplicación, la explicación y la seguridad del sistema. Esta guía irá dirigida al personal informático responsable de la instalación, en colaboración con los usuarios que van a usar la aplicación (clientes) con el objetivo de dar toda la información necesaria para garantizar que la implantación de la aplicación se realice de forma segura, confiable y precisa.
## Explotación
Una vez que ya tenemos todas las fases documentadas, hemos realizado pruebas con el software para comprobar su fiabilidad y que carece de errores con la fase de explotación.

En esta fase realizaremos la instalación, configuración y puesta en funcionamiento de la aplicación en los equipos del cliente.
En esta fase realizaremos la última prueba denominada Beta Test, la  realizaremos en los equipos del cliente y siempre que sea posible con la presencia del mimo.

Para la instalación de nuestra aplicación acudiremos al cliente con nuestro software preparado para transferirlos a sus equipos, después será necesario configurar los parámetros de funcionamiento normal de la empresa. Por último los usuarios finales comenzaran a usar la aplicación.
## Mantenimiento
En esta fase realizaremos los procesos de control mejora y optimización del software, para ello pactaremos con el cliente los costes económicos y la duración del servicio de mantenimiento que mejor se adapten a sus necesidades.
El mantenimiento debe cubrir distintos cambios como pueden ser:
- **Perfectivos**: mejorar la funcionalidad del software.
- **Evolutivos**: cubrir las nuevas necesidades del cliente.
- **Adaptativos**: adaptarse a las nuevas tendencias del mercado o al nuevo hardware.
- **Correctivos**: corregir los errores que tenga en un futuro. 
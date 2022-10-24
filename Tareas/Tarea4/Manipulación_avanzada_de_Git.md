# Manipulación avanazada de GIT

## ÍNDICE:
- Ejercicios 1
- Ejercicios 2
- Ejercicios 3
- Ejercicios 4
- Ejercicios 5
- Ejercicios 6
- Ejercicios 7
- Ejercicios 8
- Ejercicios 9
---
## Ejercicio 1
En este ejericio se muestra el historial de los cambios del repositorio, se crea la carpeta capítulos y se crea dentro de ella el fichero  capitulo1.txt con el siguiente texto:

        Git es un sistema de control de versiones ideado por Linus Torvalds.
Además, se añaden los cambios a la zona de intercambio temporal, se hace un commit de los cambios con el mensaje **Añadido capítulo 1.** Y, por último, se vuelve a mostrar el historial de cambios del repositorio. 

![<Imagen 1>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%201.png>)

---
## Ejercicio 2
 En este ejercicio se crea el     fichero capitulo2.txt en la carpeta capítulos con el siguiente texto:

        El flujo de trabajo básico con Git consiste en: 1- Hacer cambios en el repositorio. 2- Añadir los cambios a la zona de intercambio temporal. 3- Hacer un commit de los cambios.
Por otro lado, se añade los cambios ala zona de intercambio temporal, se hace un commit de los cambios con el mensaje **Añadido capítulo 2.** Por último se muestran las diferencias entre la última versión yt las versiones anteriores. 

![<Imagen 2>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%202.1.png>)

![<Imagen 3>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%202.2.png>)


---
## Ejercicio 3
En este ejericicio se crea el fichero capítulo3.txt en la carpeta capítulos con el siguiente texto:

        Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.
Después de esto, se añaden los cambios a la zona de intercambio temporal, se hace un commit de los cambios con el mensaje **Añadido capítulo 3.** Por último se muestra las diferencias entre la primera y las últimas versiones del repositorio.

![<Imagen 4>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%203.1.png>)

![<Imagen 5>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%203.2.png>)

![<Imagen 6>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%203.3.png>)

---
## Ejercicio 4
En este ejercicio se crea el fichero *índice.txt* y se añade la siguiente línea:

        Indice de los cápitulos, con conceptos avanzados de git
Además, se añade los cambios a la zona de intercambio temporal, se hace un commit de los cambios con el mensaje **Indice de los cápitulos, con conceptos avanzados de git.** Y el último paso sería mostrar quién hizo dichos cambios en el fichero *indice.txt.*

![<Imagen 7>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%204.png>)

---
## Ejercicio 5
En este ejercicio solo se crea una nueva rama llamada *bibliografía* y se muestran las ramas del repositorio. 

![<Imagen 8>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%205.png>)

---
## Ejericio 6
En este ejercicio se crea el fichero *capitulos/capitulo4.txt* y se añpade el texto siguiente:

          En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.
Después de esto, se añade los cambios a la zona de intercambio temporal, se hace un commit con el mensaje **Añadido capítulo 4.** y se muestra el historial del repositorio incluyendo todas las ramas. 

![<Imagen 9>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%206.png>)

---
## Ejercicio 7
En este ejercicio se cambia a la rama *bibliografía*, se crea el fichero *bibliografia.txt* y se añade la siguiente referencia:

        Chacon, S. and Straub, B. Pro Git. Apress.
Además, se añade los cambios a la zona de intercambio temporal, se hace un commit con el mensaje **Añadida primera referencia bibliográfica.** y se muestra el historial del repositorio incluyendo todas las ramas. 

![<Imagen 10>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%207.1.png>)

![<Imagen 11>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%207.2.png>)

---
## Ejercicio 8
En este ejercicio se fusiona la rama *bibliografía* con la rama *main*, se muestra la historia del repositorio incluyendo todas las ramas, se elimina la rama *bibliografía* y se muestra de nuevo el historial del repositorio incluyendo todas las ramas. 

![<Imagen 12>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%208.1.png>)

![<Imagen 13>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%208.2.png>)

---
# Ejercicio 9
En este ejercico se crea la rama *bibliografía*, se cambia a dicha rama y se cambia el fichero *bibliografia.txt* para que contenga las siguientes referencias:

        Scott Chacon and Ben Straub. Pro Git. Apress.
        Ryan Hodson. Ry’s Git Tutorial. Smashwords (2014)
Después de esto, se cambia a la rama *main* y se cambia el fichero *bibliografia.txt* para que contenga las siguientes referencias: 

        Chacon, S. and Straub, B. Pro Git. Apress.
        Loeliger, J. and McCullough, M. Version control with Git. O’Reilly.
Además, se añaden los cambios a la zona de intercambio temporal y se hace un commit con el mensaje **Añadida nueva referencia bibliográfica.**. A continuación, se fusiona la rama *bibliografía* con la rama *main* y se resuelve el conflicto dejando el fichero *bibliografia.txt* con las referencias: 

        Chacon, S. and Straub, B. Pro Git. Apress.
        oeliger, J. and McCullough, M. Version control with Git. O’Reilly.
Por último se añaden los cambios a la zona de intercambio temporal, se hace un commit con el mensaje **Resuelto conflicto de bibliografía.** y se muetsra el historial del repositorio incluyendo todas las ramas. 

![<Imagen 14>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%209.1.png>)

![<Imagen 15>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%209.2.png>)

![<Imagen 16>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%209.3.png>)

![<Imagen 17>](<https://github.com/Yaamiilaa/entornos-desarrollo/blob/main/Tareas/Tarea4/img/paso%209.4.png>)
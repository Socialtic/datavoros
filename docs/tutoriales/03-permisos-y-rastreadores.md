# Permisos

En esta sección vamos a mostrar cómo averiguar cuáles son los permisos que están embebidos en el código de una aplicación y cuáles son aquellos que la Playstore nos muestra. 

## Permisos de la Playstore

1. Para averiguar los permisos de una aplicación desde la PlayStore de Google, lo primero que tenemos que hacer es acceder a la [PlayStore](https://play.google.com/store/apps). 

2. Activamos la opción de buscar:
![1](./capturas_de_pantalla/permisos/1-permisos-playstore.png)

3. Ponemos el nombre de la aplicación en la barra de búsqueda:
![2](./capturas_de_pantalla/permisos/2-permisos-playstore.png)

4. Entramos a la aplicación y bajamos hasta la sección de "Información de la aplicación":
![3](./capturas_de_pantalla/permisos/3-permisos-playstore.png)

5. Damos clic en "detalles" en la sección de "Permisos":
![4](./capturas_de_pantalla/permisos/4-permisos-playstore.png)

6. Así aparecen los permisos:
![5](./capturas_de_pantalla/permisos/5-permisos-playstore.png)

## Permisos mediante Exodus Privacy

A través del servicio en línea de [Exodus Privacy](https://exodus-privacy.eu.org/en/) podemos averiguar los permisos que están embebidos en el código de cada aplicación.

1. Entramos a este [enlace](https://reports.exodus-privacy.eu.org/en/).

2. Aquí podemos buscar la aplicación ya sea por su nombre o por la dirección URL que aparece en la PlayStore. Esta dirección es la que aparece en la barra de direcciones del paso 4 del tutorial anterior. En importante reconocer el nombre que aparece después del valor "id=", ya que este nombre de la aplicación nos servirá más adelante. 
![1](./capturas_de_pantalla/permisos/1-permisos-exodus.png)

3. Si la aplicación ya fue analizada con anterioridad por algún otro usuario, aparecerá en la lista de resultados. En este ejemplo, como nosotros la analizamos, aparece la app 9-1-1 Emergencias:
![2](./capturas_de_pantalla/permisos/2-permisos-exodus.png)

4. Si la aplicación no aparece o la versión de la aplicación es distinta a la que queremos analizar, entonces bajamos hasta la sección donde dice "Perform new analysis":
![3](./capturas_de_pantalla/permisos/3-permisos-exodus.png)

5. Nos solicita la dirección URL de la aplicación. Como se ve, a la hora de pegarla, no aparece la URL completa, sino el valor que mencionamos en el paso 2 de esta sección. Le damos click a "Perform analysis":
![4](./capturas_de_pantalla/permisos/4-permisos-exodus.png)

6. Nos aparecerá una pantalla que dice que se está realizando el análisis:
![5](./capturas_de_pantalla/permisos/5-permisos-exodus.png)

7. Terminado el análisis nos dirá que ya podemos analizar el reporte. Le damos click a "See the report":
![6](./capturas_de_pantalla/permisos/6-permisos-exodus.png)

8. Lo primero que vemos es un resumen con el número de rastreadores presentes y la cantidad de permisos:
![7](./capturas_de_pantalla/permisos/7-permisos-exodus.png) 

9. Si bajamos un en la página, llegaremos a la sección de permisos, donde se nos mostrarán todos los permisos embebidos en el código, algunos con explicación de qué es lo que hacen, otros no. Y además algunos con un signo de exclamación en rojo, que indica que es un permiso peligroso según lo considera Google.
![8](./capturas_de_pantalla/permisos/8-permisos-exodus.png)

# Rastreadores

Para averiguar qué rastreadores tiene una aplicación hay que seguir los mismos pasos de la sección anterior. En el listado de rastreadores, sin embargo, podemos acceder a una página de referencia con más información del rastreador en cuestión:
![9](./capturas_de_pantalla/permisos/9-permisos-exodus.png)

- En esta página aparecen datos relevantes sobre el rastreador. Hasta arriba, el nombre. Justo abajo, el tipo de rastreador, es decir, para qué se usa. En nuestro ejemplo "Advertising", es decir, para publicidad.

- "Present in" se refiere a la cantidad de aplicaciones en las cuales ha sido encontrado este rastreador.

- Luego tenemos dos enlaces a las páginas web del rastreador para desarrolladores y del lado derecho el enlace "Tracker web page" nos dirige a la página general del rastreador (Esta información no siempre aparece para todos los rastreadores).

- Por último tenemos la sección "Detection Rules". Estas son las reglas de detección del rastreador dentro del código de la aplicación. En otras palabras, cuando en el código de la aplicación aparece alguna de las cadenas de esta sección, entonces podemos estar seguros que el rastreador está presente. 





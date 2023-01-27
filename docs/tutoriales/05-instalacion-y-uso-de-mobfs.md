# Qué es MobSF

Mobile Security Framework es un programa que automatiza toda una serie de análisis tanto dinámicos como estáticos de aplicaciones, para poder identificar vulnerabilidades, tipos de malware y otros problemas de privacidad. En nuestro caso, es una herramienta que nos permitirá identificar de una manera bastante sencilla los permisos de la app y los trackers. Al mismo tiempo, tiene otras características que veremos más adelante que pueden hacer que nuestros análisis sean más completos.

# Instalación de MobSF

La guía de instalación de MobSF es muy completa, de tal manera que aquí solamente pondremos los links. Lo primero que hay que hacer es cumplir con los requerimientos para la instalación. Aquí están:
- [Requerimientos](https://mobsf.github.io/docs/#/requirements)   
MobSF permite el análisis dinámico de las aplicaciones, es decir, el análisis del comportamiento del código mientras se ejecuta la aplicación. Es importante aclarar que, para poder hacer este tipo de análisis, es necesario que MobSF no esté corriendo dentro de una máquina virtual. MobSF utiliza ya sea el emulador de Android Studio o GenyMotion (dos programas que crean máquinas virtuales donde se simula la ejecución de un celular) para llevar a cabo el análisis dinámico y, a la fecha, es imposible ejecutar un emulador dentro de una máquina virtual. 
- [Instalación](https://mobsf.github.io/docs/#/installation)

**Existe una versión en línea de [MobSF](https://mobsf.live/). El problema de esta versión es que: 1) Los análisis que se hacen son públicos, y 2)Probablemnete no duren en su base de datos más que algunas horas, antes de que sea substituido por el de alguna nueva aplicación, de tal manera que si uno quiere regresar a un análisis hecho, deberá volverlo a hacer**

# Ejecutar MobSF

Para poder ejecutar este programa, sólo es neceario ir a la terminal de linux, ir al directorio de instalación de MobSF (que es donde se guardó la carpeta clonada por medio del comando git) y ejecutar el siguiente comando:
``` 
./run.sh 127.0.0.1:8000
```
Después hay que abrir un explorador (el que sea) y poner en la barra de direcciones
```
http://localhost:8000/
```
Este comando ejecuta por medio de la orden **./** el script **run.sh.** en la llamada *dirección de loopback* o también conocida como *localhost*. Esta es una dirección ip que sirve para que el *host* de un servicio pueda dirigir el tráfico hacia sí mismo. En otras palabras, MobSF se ejecuta como una suerte de servidor web que redirige el tráfico hacia sí mismo. Esa es la razón que MobSF se ejecute en un explorador web.

# Cómo utilizar MobSF para análisis estáticos

- Una vez ejecutado el programa, deberíamos tener una pantalla similar a esta nuestro explorador:
![bienvenida](./capturas_de_pantalla/mobsf/1-mobsf-bienvenida.png)

Aquí podemos o bien arrastrar nuestro archivo apk a la pantalla, o dar click en "Upload & Analyze" y seleccionar nuestro archivo.    

- Aparecerá una pantalla como esta que nos indicará que se está analizando el archivo apk:
![analizando](./capturas_de_pantalla/mobsf/2-analizando.png)

- Al terminar aparecerá una pantalla similar a esta:
![hecho](./capturas_de_pantalla/mobsf/3-analisis-hecho.png)

- Si nos desplazamos hacia abajo, encontraremos la sección de permisos de la aplicación. Aquí vendrán listados todos los permisos, para qué sirven y su categoría de riesgo.
![permisos](./capturas_de_pantalla/mobsf/4-permisos.png)

- Luego encontraremos un mapa donde se listan los posibles dominios a donde a se conecta la aplicación. Es muy importante remarcar que esto no quiere decir que la aplicación por fuerza se conecte a estos dominios. Por eso necesitamos siempre hacer el anáisis de tráfico de red con Wireshark.
![servidores](./capturas_de_pantalla/mobsf/5-server%20locations.png)

- La siguiente sección, "Domain Malware Check", hace un análisis de los dominios anteriores para verificar que ninguno sea malicioso.
![malware](./capturas_de_pantalla/mobsf/6-domain-malware.png)

- Adelante aparece la sección de trackers donde se nos dice cuáles hay y se nos provee un link a la página del tracker del proyecto Exodus Privacy.
![trackers](./capturas_de_pantalla/mobsf/7-trackers.png)

Aunque está claro que la información proporcionada por este programa es muy amplia, esta es la manera de utilizarla para enfocarnos en lo que nos interesa para este proyecto.   
Incluso podemos, si le damos click del lado izquierdo a la sección "PDF Report", generar un reporte en PDF con todos los datos encontrados. Para poder hacer esto, sin embargo, necesitamos primero instalar la siguiente librería:
```
sudo apt install wkhtmltopdf
```
- Una vez que lo hayamos hecho, basta generar el reporte y tendremos un pdf con una carátula similar a esta:
![reporte](./capturas_de_pantalla/mobsf/8-report.png)





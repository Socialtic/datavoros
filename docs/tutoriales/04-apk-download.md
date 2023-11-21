# Apk Download

Apk, que quiere decir Android Package Kit, es el formato de archivo que usa Android para distribuir e instalar aplicaciones. Su pararalelo en Windows sería un archivo .exe. En un archivo apk están contenidos todos los elementos necesarios para poder instalar una aplicación en cualquier dispositivo Android.   
Para poder hacer uso de programas como MobSF, necesitamos poder acceder a los archivos apk. Hay varias formas de hacer esto. 

## Páginas web

Existen varias páginas que nos permitirán descaragar los archivos apk. Enumeramos algunas:

- [https://www.apkonline.net/apkdownloader.php](https://www.apkonline.net/apkdownloader.php)
- [https://apkpure.com/](https://apkpure.com/)
- [https://www.apkmirror.com/](https://www.apkmirror.com/)
- [https://apk-dl.com/](https://apk-dl.com/)
- [https://en.aptoide.com/](https://en.aptoide.com/)
- [https://www.apkmonk.com/](https://www.apkmonk.com/)
- [https://f-droid.org/](https://f-droid.org/) *Sólo aplicaciones FOSS*


Si bien sabemos que estas páginas son seguras, siempre existe la posibilidad que algun app que se descaraga de aquí pueda contener código malicioso. De tal manera que recomendamos ser precavidos. 

## Apkeep 
**Hast el 11/11/2022, este programa tiene un bug no resuelto, de tal manera que a veces funciona y a veces no.**

[Apkeep](https://github.com/EFForg/apkeephttps://github.com/EFForg/apkeep) es un programa hecho por la Electronic Frontier Foundation (EFF) que nos permite bajar archivos apk desde la propia PlayStore de Google, lo que implica que tendremos más seguridad y más variedad de aplicaciones. Es importante remarcar que, debido a las políticas de Google, si uno baja muchas aplicaciones, se puede suspender la cuenta desde donde se están bajando. Por lo mismo recomendamos crear una cuenta de gmail específica para bajar estos archivos. 

### Instalación y Uso
Podemos ejecutar apkeep de dos maneras, bajando un binario desde la página de github o instalándolo en nuestra computadora. Mostraremos las dos opciones.

1. **Bajar un binario.** 
    - Acceder a la página [https://github.com/EFForg/apkeep/releases](https://github.com/EFForg/apkeep/releases).
    - En la última versión (al día de hoy es la número 13) encontrar el binario que se corresponde con nuestro sistema. En el caso de Linux sería la versión **apkeep-x86_64-linux-android**
    - Después de descargado, mover el archivo al directorio de nuestra preferencia y cambiar el nombre a algo sencillo, puede ser simplemente apkeep.
    - Abrir una terminal en el directorio donde se encuentra el binario y ejecutar este comando:
    ```
    ./apkeep -a com.nombre.app /directorio/de/descarga
    ```
    *Como vimos anteriormente en el tutorial de "Permisos y rastreadores", el nombre de la app es el nombre que podemos extraer de la URL de la PlayStore después de id=com.ejemplo.app*   

    El comando anterior descargará por defecto la aplicación desde ApkPure. Si queremos que descargue desde la PlayStore, necesitamos agregar otros parámetros:
    ```
    ./apkeep -a com.nombre.app -d google-play -u 'ejemplo@gmail.com' -p password /directorio/de/descarga
    ```
    *Para que esto funcione sin problemas, se recomienda en la cuenta creada especialmente para bajar apk's, no activar la verificación en dos pasos. En caso de tenerla activada, será necesario crear una contraseña específica para apkeep. [Aquí](https://support.google.com/accounts/answer/185833) las instrucciones.*   
2.  **Instalar**
    - Apkeep está hecha con el lenguaje de programación llamado Rust, debido a esto tenemos que tenerlo instalado. Para esto ejecutamos este comando en Linux:

    ```
    curl https://sh.rustup.rs -sSf | sh
    ```
    *Esta es la manera indidcada en la página oficial de [Rust](https://forge.rust-lang.org/infra/other-installation-methods.html)*
    - Antes de poder instalar apkeep, necesitamos instalar "cargo" que es el package manager de Rust.
    ```
    sudo apt install cargo
    ```
    - Tenemos que instalar las librerías de OpenSSL si nos tenemos instaladas y pkg-config
    ```
    sudo apt install libssl-dev pkg-config
    ```
    - Con esto hecho podemos instalar apkeep simplemente con el siguiente comando
    ```
    sudo cargo apkeep
    ```
    - Al finalizar la instalación aparecerá una leyenda que dice:
    ```
    Warning: be sure to add /home/username/.cargo/bin to your PATH to be able to run the installed bianries
    ```
    
    Esto quiere decir que, para que nuestra terminal reconozca el comando apkeep, le tenemos que indicar la ruta donde se encuentra. Para ello haremos lo siguiente:

    - Abrimos el archivo profile:
        ``` 
        sudo nano ~/.profile
        ```
    - Nos vamos hasta la parte de abajo y agregamos la siguiente línea:
        ```
        export PATH=/home/username/.cargo/bin:$PATH
        ```

    Una vez hecho lo anterior, para usar apkeep simplemente usamos el comando apkeep seguido de las condiciones que nos interesan:
    ```
    apkeep -a com.nombre.app -d google-play -u ejemplo@gmail.com -p password /directorio/de/descarga
    ```


    

## Otros programas

- [Racoon](https://raccoon.onyxbits.de/)
- [APK Downloader](https://github.com/jayluxferro/APK-Downloader)
- [gplaydl](https://github.com/rehmatworks/gplaydl)


## Usando comandos en la terminal de Linux

Otra manera de tener acceso al archivo APK de una aplicación es instalándolo en el dispositivo móvil desde la PlayStore y luego extrayendo dicho archivo al conectarlo a una computadora. 

### Requerimientos

- Instalar android-tools en Ubuntu. Estas herramientas nos permitirá ejecutar un comando desde la consola: adb (Android Debug Bridge). Para instalar las Platform Tools, ejecutamos primero el comando para actualizar los repositorios, y luego el de instalación:
~~~
sudo apt update 
sudo apt install android-tools-adb
~~~
Si queremos revisar que adb funciona y averiguar su versión, podemos ejecutar el siguiente comando:
~~~
adb version
~~~
Debería responder algo similar a:
~~~
Android Debug Bridge version 1.0.32
~~~

- Activar USB Debbugin en el celular. Este modo permite acceder al celular desde una línea de comandos cuando lo conectamos a una computadora que tenga adb instalado. Para ello hacemos lo siguiente:
    - Ir a **Configuración**
    - Ir a **Acerca del teléfono**
    - Dar click 7 veces en **Número de compilación** (Esto va a habilitar las opciones de desarrollador en Android)
    - Regresar a **Configuración** e ir a **Sistema** 
    - Ir a **Desarrollador**
    - Activar **Depurador por USB**   

La próxima vez que conectemos nuestro celular por medio de un cable a la computadora, nos preguntará si queremos activar la depuración USB y si queremos confiar en el dispositivo al cual conectamos el celular. Le damos que sí. [Aquí](https://www.apowersoft.es/faq/usb-debugging.html) hay un tutorial que abarca diferentes versiones de Android. No recomendamos usar el segundo método (por medio de una APK) que proponen en ese tutorial. 

### Cómo extraer el archivo apk

- Conectar el celular a la computadora por medio de un cable y activar el modo **Depurador USB**
- Abrir una terminal y ejecutar el siguiente comando:
~~~
adb devices
~~~
La terminal responderá algo similar a:
~~~
List of devices attached
ZY227BGZP8
~~~
El código dependerá del celular conectado, pero lo importante es que reconoce que el celular está conectado.    

- Instalamos la aplicación desde la PlayStore como normalmente lo hacemos. OJO: No abrir la aplicación ni utilizarla, para así poder extraer una versión *limpia*. 

- Ejecutamos el siguiente comando, que nos permitirá listar todos los paquetes instalados en nuestro celular, incluida la aplicación que acabmos de instalar.
~~~
adb shell pm list packages
~~~
Se listarán todos los paquetes instalados. Tenemos que revisar la lista y encontrar el que se corresponde con nuestra aplicación. Por lo general el nombre es el mismo que aparece en la URL de la PlayStore:
~~~
https://play.google.com/store/apps/details?id=*com.kiloo.subwaysurf*
~~~
La sección que marcamos entre asteriscos es la que nos interesa. Algunas otras veces puede cambiar el nombre del paquete o se le agregan algunos datos, pero en general lo dicho anteriormenete debería funcionar. 

- Ejecutamos el siguiente comando para saber exactamente dónde está guardado dicho paquete:
~~~
adb shell pm path com.kiloo.subwaysurf
~~~
Tendremos como resultado algo similar esto:
~~~
package:/data/app/com.kiloo.subwaysurf-2622.apk
~~~
A veces, en vez del nombre de la apk, aparece algo similar  a esto:
~~~
package:/data/app/base.apk
~~~
La base apk es la que nos interesa.

- Una vez que identificamos la ruta donde encuentra el archivo que queremos, simplemente ejecutamos el siguiente comando que nos permitirá extraer el archivo apk y copiarlo a nuestra computadora:
~~~
adb pull /data/app/base.apk ruta/donde/se/copiará/el/archivo/en/la/computadora
~~~
Si no especificamos ninguna ruta a donde se deba copiar, el archivo se copiará automáticamente desde donde estamos ejecutando los comandos en la terminal. 
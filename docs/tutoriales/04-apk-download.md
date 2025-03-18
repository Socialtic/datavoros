# Tutorial: Descarga de archivos APK

Los archivos **APK** (**Android Package Kit**) son el formato utilizado por Android para distribuir e instalar aplicaciones. Su equivalente en Windows sería un archivo **.exe**. Contienen todos los elementos necesarios para instalar una aplicación en un dispositivo Android.

Para analizar aplicaciones con herramientas como **MobSF**, es necesario contar con los archivos APK. Existen varias maneras de obtenerlos, que se describen a continuación.


##  Métodos de descarga de APKs

### 1. Páginas web
Existen diversas plataformas en línea que permiten la descarga de archivos APK. Algunas de las más conocidas son:

- [APK Online](https://www.apkonline.net/apkdownloader.php)
- [APKPure](https://apkpure.com/)
- [APKMirror](https://www.apkmirror.com/)
- [APK DL](https://apk-dl.com/)
- [Aptoide](https://en.aptoide.com/)
- [APKMonk](https://www.apkmonk.com/)
- [F-Droid](https://f-droid.org/) (*Sólo aplicaciones FOSS*)

> **Nota:** Aunque estas páginas son conocidas y utilizadas, siempre existe el riesgo de que algunas aplicaciones contengan código malicioso. Se recomienda precaución al descargar APKs de fuentes externas.


## 2. Raccoon
[Raccoon](https://raccoon.onyxbits.de/apk-downloader/) es una herramienta que permite descargar aplicaciones desde Google Play de manera segura y eficiente.

### Instalación de Raccoon
1. Descargar el archivo **raccoon.jar** desde el sitio oficial:  
   [Raccoon APK Downloader](https://raccoon.onyxbits.de/apk-downloader/)
2. Abre una terminal y dirígetete a la ruta donde está el archivo raccoo.jar
3. Una vez que te encuentres en el directorio del archivo:
   - Da clic derecho a tu mouse y selecciona **"Abrir en terminal"**
   - Después, debes ejecutar el siguiente comando:
      ```
      java -jar raccoon.jar 
      ```
      - Este comando abrirá la interfaz gráfica de Raccoon para descargar APKs.

### Uso de Raccoon
1. Usa la barra de búsqueda para encontrar la aplicación que deseas descargar.
2. Haz clic en el botón de "Descargar" y espera a que el proceso finalice.
3. Verifica la ubicación del APK descargado:
   - Los archivos APK descargados se almacenan en la siguiente ubicación:
      ```
      /home/usuario/Raccoon/content/apps
      ```
      > **Nota:** *usuario* corresponde a tu nombre de usuario en el sistema.

## 3. Otros programas

Existen otras herramientas que permiten la descarga de APKs desde la Play Store:

-
-

## 4. Descarga usando la terminal de Linux
Otra manera de obtener un archivo APK es extrayéndolo desde un dispositivo Android en el que esté instalado.

### Requerimientos
1. Instalar android-tools-adb en Ubuntu:
   - Ejecuta los siguientes comandos en la terminal
      ```
      sudo apt update
      sudo apt install android-tools-adb
      ```
2. Verifica la versión de adb
   - Ejecuta el siguiente comando en la terminal
      ```
      adb version
      ```
   - La salida debería mostrar la siguiente información:
      ```
      Android Debug Bridge version 1.0.32
      ```
3. Activar la depuración USB en el dispositivo android:
   - Ve a Configuración > Acerca del teléfono.
   - Toca Número de compilación 7 veces para habilitar las opciones de desarrollador.
   - Ve a Configuración > Sistema > Opciones de desarrollador.
   - Activa la Depuración por USB.
   - Conecta el dispositivo a la computadora y acepta la solicitud de depuración USB.

4. Extraer el APK
   - Conecta el celular a la computadora y activa el modo Depuración USB.
   - Abre una terminal y ejecuta:
      ```
      adb devices
      ```
      - La salida debería mostrar algo como:
         ```
         List of devices attached
         ZY227BGZP8
         ```
   - Instala la aplicación desde la Play Store pero no la abras aún.
   - Obtén la lista de paquetes instalados en el dispositivo:
      ```
      adb shell pm list packages
      ```
   - Identifica el nombre del paquete de la aplicación (por ejemplo, com.kiloo.subwaysurf).
   - Obtén la ubicación del APK:
      ```
      adb shell pm path com.kiloo.subwaysurf
      ```
      Salida esperada:
         ```
         package:/data/app/com.kiloo.subwaysurf-2622.apk
         ```
   - Extraer el APK a la computadora:
      ```
      adb pull /data/app/base.apk /ruta/donde/copiar/el/apk
      ```
Si no se especifica una ruta, el APK se guardará en el directorio actual de la terminal.

## Conclusión
   Existen diversas maneras de obtener archivos APK. El método a elegir dependerá de la preferencia del usuario y la seguridad requerida. Para análisis de seguridad, se recomienda obtener los APKs directamente desde Google Play o extraerlos de un dispositivo físico con adb para asegurar su integridad.

   Con estas herramientas y técnicas, se pueden obtener APKs de manera eficiente y segura.
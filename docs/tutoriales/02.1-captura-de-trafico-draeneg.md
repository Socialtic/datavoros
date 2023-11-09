# Captura de tráfico a través de la aplicación Draeneg

- Instalar la aplicación que se quiere analizar.
- Instalar la aplicación [Draeneg](https://play.google.com/store/apps/details?id=com.orange.labs.draeneg)
- Abrir Draeneg y seleccionar **Traffic**
![traffic](./capturas_de_pantalla/draeneg/1.png)
- Seleccionar en la pestaña **All Applications** la aplicación que queremos analizar.
![applications](./capturas_de_pantalla/draeneg/2.png)
- En la sección **Stop Capturing After...** ponerlo en 0.
![traffic](./capturas_de_pantalla/draeneg/3.png)
- Dar click en **Start Capturing Traffic**
![capture](./capturas_de_pantalla/draeneg/4.png)
- Aparecerá la leyenda **Enable VPN**. Dar click en **Enable**. Y volver a  dar click en **Start Capturing Traffic**. Esto lo que hace es generar una VPN interna en el teléfono, de tal manera que puede filtrar y capturar los paquetes de datos.
![vpn](./capturas_de_pantalla/draeneg/5.png)
- Abrir la aplicación que se quiere analizar y utilizarla normalmente.
- Cuando se termine de utilizar, cerrar la aplicación que se quiere analizar, y en Draeneg, darle click a **Stop capturing traffic**
![stop](./capturas_de_pantalla/draeneg/6.png)
- Darle click al ícono de **Exportar base de datos**
![exportar](./capturas_de_pantalla/draeneg/7.png)
- Seleccionar **PCAP Format**
![pcap](./capturas_de_pantalla/draeneg/8.png)
- Seleccionar la carpeta donde guardarlo y el nombre de archivo y luego extraer el archivo del celular.

¡Listo! Este archivo es el que analizaremos más adelante en Wireshark!

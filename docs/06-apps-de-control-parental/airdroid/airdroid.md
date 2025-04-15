# AirDroid Parental Control

## Fechas de análisis

- **Análisis estático (mediante Exodus Privacy/MobFS):** 02 de abril 2025
- **Análisis dinámico (mediante análisis de tráfico de red):**  04 de abril 2025
- **Análisis Posteriores:** 
## Resumen de la aplicación

La aplicación que es presentada como una herramienta de acompañamiento digital para madres, padres o personas cuidadoras implementa un conjunto de prácticas que se aproximan peligrosamente a la vigilancia encubierta y el control excesivo sobre la infancia. Sus funcionalidades remotas avanzadas y un uso cuestionable de los datos personales, evidencia una desconexión entre lo que la aplicación declara y lo que efectivamente permite hacer.

El análisis técnico, revela múltiples inconsistencias que afectan tanto la experiencia de uso como el cumplimiento de estándares mínimos de privacidad y seguridad digital, especialmente cuando están involucradas personas menores de edad.
Entre los principales hallazgos encontramos que:
- **Falta de transparencia en el uso y activación del periodo de prueba**  
    Se detectó que la activación del periodo gratuito de uso **carece de claridad en su proceso**, lo que constituye una **mala práctica** desde los estándares internacionales de protección de datos y transparencia comercial.
- **Acceso remoto a funciones críticas del dispositivo de la infancia**
    La aplicación permite a la persona cuidadora **activar en tiempo real la cámara, el micrófono, leer notificaciones y ver la pantalla del dispositivo infantil**, sin necesidad de presencia física ni validación adicional. Esto **rompe con cualquier principio de proporcionalidad y consentimiento informado**, habilitando un escenario de **vigilancia constante** que excede ampliamente los márgenes éticos del acompañamiento digital.
- **Procesamiento de datos sensibles sin mecanismos robustos de consentimiento**  
    Si bien la política de privacidad menciona que los datos del menor son “controlados” por la cuenta del adulto responsable, **no se especifican ni los mecanismos de consentimiento informado ni las validaciones de edad exigidas por normativas internacionales**. Esto **pone en riesgo el cumplimiento legal y ético** del tratamiento de datos personales de menores.
- **Violación de principios de privacidad por diseño y minimización de datos**  
    La posibilidad de grabar audio, video y pantalla completa de manera remota **no guarda proporción con la finalidad declarada de seguridad o acompañamiento**. Estas funcionalidades, sin filtros ni restricciones claras, **evidencian un diseño centrado en el control total** del dispositivo infantil, más que en su protección.
## Archivos analizados

- [apk versión ###]()
- [pcap versión ###]()
- [Capturas de pantalla]()
- [Reporte MobSF]()

## Descripción de la aplicación
- **Tipo:**   Aplicación de control parental
- **Costo:**   Descarga gratuita con compras directas desde la aplicación
- **Enlace de descarga:** https://play.google.com/store/apps/details?id=com.sand.airdroidkidp&hl=es_MX
- **Descargas:** Más de 5 millones de descargas
- **Ultima fecha de actualización:** 02 de abril 2025
- **Versión:** 2.4.0.1
- **Desarrollador:** [Sand Studio](https://sandstudio.co/)
- **Firma:** [SAND STUDIO CORPORATION LIMITED](https://sandstudio.co/)
- **Contacto:** support@airdroid.com
- **Condiciones de uso y Política de privacidad:**
	- Términos de servicio: https://kids.airdroid.info/#/Terms
	- Política de privacidad: https://kids.airdroid.info/#/Privacy
    
- **Descripción en PlayStore:**
~~~
Descripción de la PlayStore
La aplicación AirDroid Parental Control está diseñada para que la seguridad de sus hijos sea una prioridad. Gracias a las funciones de alta seguridad que ofrece AirDroid Parental Control, podrá ponerse fácilmente en contacto con ellos cuando no estén cerca o no puedan responderle a tiempo. Localícelos en un toque, ¡es sumamente fácil!
~~~

## Rastreadores identificados (mediante MobSF)

| Rastreador                                                                     | Tipo              |
| ------------------------------------------------------------------------------ | ----------------- |
| [AutoNavi/Amap](https://reports.exodus-privacy.eu.org/trackers/361)            | Ubicación         |
| [Facebook Analytics](https://reports.exodus-privacy.eu.org/trackers/66)        | Analítica         |
| [Facebook Login](https://reports.exodus-privacy.eu.org/trackers/67)            | Identificación    |
| [Facebook Share](https://reports.exodus-privacy.eu.org/trackers/70)            |                   |
| [Google CrashLytics](https://reports.exodus-privacy.eu.org/trackers/27)        | Informe de fallas |
| [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/trackers/49) | Analítica         |

## Empresas relacionadas con esta aplicación:

| Empresa                                                | Servicios que ofrecen   |
| ------------------------------------------------------ | ----------------------- |
| [IENTC A DE RL DE CV](https://ientc.com/)              | Telecomunicaciones      |
| [Tencent](https://www.tencent.com/en-us/)              | Telecomunicaciones      |
| [Universidad Autónoma de México](https://www.unam.mx/) | Estudios universitarios |

### Empresas identificadas a través del Aviso de Privacidad con que se comparten datos:

- [Sand Studio](https://sandstudio.co/)

**Nota: No se mencionan explícitamente otras empresas como parte del procesamiento de datos, pero se hace alusión a terceros y proveedores de servicios.**

### Dominios integrados al código de la aplicación que no pertenecen directamente a los rastreadores

| Dominios                                |
| --------------------------------------- |
| https://airdroid-parent.firebaseio.com/ |
| https://firebase.google.com/            |
| https://issuetracker.google.com/        |

## Permisos   

- **Según Exodus Privacy/MobFS:** 30
- **Según prueba de uso:** 4

### Permisos según Exodus Privacy

- ACCESS
- ACCESS_ADSERVICES_AD_ID
- ACCESS_ADSERVICES_ATRIBUTION
- :exclamation: ACCESS_COARSE_LOCATION
- :exclamation: ACCESS_FINE_LOCATION
- ACCESS_WIFI_STATE
- BILLING
- :exclamation: CAMERA
- CHANGE_NETWORK_SATATE
- CHANGE_RECEIVER_NOT_EXPORTED_PERMISSION
- FOREGRAUND_SERVICE_MICROPHONE
- INTERNET
- MODIFY_AUIDIO_SETTINGS
- msa
- POST_NOTIFICATION
- :exclamation: READ_EXTERNAL_STORAGE
- READ_MEDIA_IMAGES
- READ_MEDIA_VIDEO
- READ_MEDIA_VISUAL_USER_SELECTED
- RECEIVE_BOOT_COMPLETED
- :exclamation: RECORD_AUDIO
- :exclamation: SYSTEM_ALERT_WINDOW
- VIBRATE
- WAKE_LOCK

El icono :exclamation: indica un nivel 'Peligroso' o 'Especial' de acuerdo a los [niveles de protección de Google](https://developer.android.com/guide/topics/permissions/overview). 

### Permisos solicitados durante el uso de la aplicación

- :red_circle: Ubicación
- :red_circle: Optimización de la batería
- :red_circle: Notificaciones
- :red_circle: Accesibilidad

:red_circle: Este ícono indica un permiso obligatorio   
:blue_circle: Este ícono indica un permiso opcional pero se pierde una funcionalidad particular

## Datos

### Datos solicitados al usuario 

#### Datos solicitados durante el registro

- :red_circle: Correo electrónico
- :blue_circle: Nombre de la persona adulta

### Datos solicitados al usuario durante el uso de la aplicación

La aplicación no solicita datos adicionales durante su uso.


:red_circle: Este ícono indica que se debe ingresar este dato de manera obligatoria.   
:blue_circle: Este ícono indica que estos datos son opcionales.


### Tabla de conexiones realizadas durante el uso de la aplicación

| Dirección IP    | Número de Paquetes | País          | Ciudad/Zona | Organización AS                       | Dominio |
| --------------- | ------------------ | ------------- | ----------- | ------------------------------------- | ------- |
| 38.194.232.102  | 909                | México        | Tizayaca    | IENTC S DE RL DE CV                   |         |
| 43.130.4.190    | 169                | United States | Santa Clara | Tencent Building, Khejizhingyi Avenue |         |
| 49.51.35.72     | 244                | United States | Santa Clara | Tencent Building, Khejizhongyi Avenue |         |
| 49.51.42.151    | 120                | United States | Santa Clara | Tencent Building, Khejizhongyi Avenue |         |
| 49.51.42.41     | 861                | United States | Santa Clara | Tencent Building, Khejizhongyi Avenue |         |
| 49.51.177.82    | 149                | United States | Santa Clara | Tencent Building, Khejizhongyi Avenue |         |
| 49.51.181.88    | 1,634              | United States | Santa Clara | Tencent Building, Khejizhongyi Avenue |         |
| 49.51.199.235   | 171                | United States | Santa Clara | Tencent Building, Khejizhongyi Avenue |         |
| 49.51.200.225   | 5,923              | United States | Santa Clara | Tencent Building, Khejizhongyi Avenue |         |
| 49.51.229.63    | 282                | United States | Santa Clara | Tencent Building, Khejizhongyi Avenue |         |
| 49.51.230.180   | 181                | United States | Santa Clara | Tencent Building, Khejizhongyi Avenue |         |
| 132.248.3.29    | 2                  | México        | Mexico City | Universidad Autónoma de México        |         |
| 170.106.112.204 | 73                 | United States | Santa Clara | Tencent Building, Khejizhongyi Avenue |         |
| 170.106.197.185 | 49                 | United States | Santa Clara | Tencent Building, Khejizhongyi Avenue |         |

### Mapa de conexiones realizadas durante el uso de la aplicación

![mapa](./mapa.png)
*Mediante Wireshark*

### Datos recopilados y uso según la PlayStore

| Datos                                                          | Uso                                                                                           |
| -------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| Registros de fallas                                            | Funciones de la aplicación y análisis                                                         |
| Diagnóstico                                                    | Funciones de la aplicación y análisis                                                         |
| Otros datos de rendimiento de la aplicación (no especificadas) | Funciones de la aplicación y análisis                                                         |
| Interacciones de la aplicación                                 | Funciones de la aplicación y análisis                                                         |
| Historial de búsqueda en la aplicación                         | Funciones de la aplicación y análisis                                                         |
| Otras acciones (no especificadas)                              | Funciones de la aplicación y análisis                                                         |
| Dirección de correo electrónico                                | Funciones de la aplicación, análisis, comunicaciones del desarrollador y gestión de la cuenta |
| ID de dispositivo u otros IDs (no especificados)               | Análisis                                                                                      |

### Prácticas de seguridad

- La aplicación indica que "*Cifrado de datos en tránsito:* La aplicación indica que cifra los datos durante su transmisión." lo cual según nuestro análisis es correcto.
- La aplicación indica que "*Mecanismo de eliminación de datos:* La aplicación señala que los datos no pueden ser borrados por el usuario." lo cual no fue posible de probar en este análisis y queda sin confirmar.

### Datos recopilados y uso según la Política de privacidad

| Datos                                                                                      |
| ------------------------------------------------------------------------------------------ |
| Información personal: Nombre, dirección de correo electrónico, información de la cuenta.   |
| Información del dispositivo: Modelo, sistema operativo, identificadores únicos, red móvil. |
| Datos de uso: Actividad en la aplicación, eventos, funciones utilizadas.                   |
| Datos de ubicación: GPS y señales para la ubicación de la infancia.                        |
| Información de diagnóstico: Registro de errores y rendimiento.                             |

### Uso general de la información según la Política de privacidad

- Proveer y operar los servicios de control parental.
- Monitorear la actividad de la infancia y el estado del dispositivo.
- Mejorar el rendimiento, calidad y funcionalidad del producto.
- Proveer soporte técnico y gestionar solicitudes de la persona usuaria.
- Cumplir con obligaciones legales y regulatorias.
- Detectar, prevenir y abordar incidentes de seguridad o fraude.

#### Información compartida con terceros

La aplicación declara que puede compartir la información de las personas usuarias con:
- Proveedores externos, como lo que ofrecen servicios de almacenamiento en la nube, análisis de datos, atención al cliente.
- Autoridades legales o reguladoras, cuando es requerido por la ley.
- Otras empresas del mismo grupos como, filiales o subsidiarias dentro del mismo grupo empresarial.
- Empresas externas en casi de que la aplicación sea vendida, se fusione o cambie de dueño.

## Funciones particulares de la aplicación:
- **Supervisión de aplicaciones espía ocultas**  
    AirDroid permite a las madres, padres y personas cuidadoras visualizar todas las aplicaciones instaladas en el dispositivo del menor, incluyendo aquellas que podrían estar ocultas o disfrazadas. Esta función ayuda a identificar y eliminar posibles aplicaciones espía que podrían comprometer la seguridad del menor.
- **Monitoreo de actividades en redes sociales sin acceso directo**  
    La aplicación ofrece la capacidad de supervisar la actividad del menor en plataformas como Snapchat sin necesidad de acceder directamente a sus cuentas. Esto permite a las madres, padres y personas cuidadoras mantenerse informados sobre las interacciones sociales de sus hijos sin invadir su privacidad.
- **Alertas instantáneas de contenido sensible**  
    AirDroid envía notificaciones en tiempo real cuando detecta palabras clave o contenidos específicos que podrían ser inapropiados o peligrosos, permitiendo a los padres actuar de manera oportuna.
- **Detección de rastreo y amenazas de seguridad**  
    La aplicación incluye herramientas para identificar si el dispositivo del menor está siendo rastreado o si hay intentos de acceso no autorizados, fortaleciendo así la seguridad digital del usuario.
- **Historial y seguimiento de ubicación en tiempo real**  
    AirDroid proporciona un historial detallado de las ubicaciones visitadas por el menor y permite a los padres rastrear su ubicación en tiempo real, ofreciendo una capa adicional de seguridad
## Notas

- La aplicación al momento de la descarga no notifica que tiene un periodo de prueba, al pasar 10 días, esta prueba termina y comienza a negar la posibilidad de uso de algunos servicios de la aplicación.
- La aplicación es muy intuitiva y fácil de usar para las personas cuidadoras, tiene una interfaz amigable y de sencillo uso.
- La aplicación de la persona cuidadora es la que mantiene el control de la aplicación de la infancia, en ella pueden acceder de manera remota servicios del dispositivo de la infancia como la cámara, el micrófono, la pantalla total del dispositivo así como recibir en tiempo real todas las notificaciones del dispositivo de la infancia.

## Conclusiones

- **Falta de trasparencia en la activación del periodo de prueba**: 
	- Hay una **falla de transparencia** que puede ser considerada una mala práctica según estándares de protección de datos.
- **Capacidades remotas intrusivas desde el dispositivo de la persona cuidadora**
	- Cámara, micrófono, pantalla, notificaciones: en tiempo real y sin presencia física.
	- Implicación directa: La aplicación permite una **vigilancia constante**, lo que la coloca peligrosamente cerca del territorio del **control excesivo o potencial vigilancia encubierta**.
	- Según su propia política de privacidad, **se recolectan datos sensibles**, incluyendo contenidos generados por la persona usuaria, datos de dispositivos y redes, y comportamientos de uso.
- **Uso de datos personales y consentimiento infantil**
	- La app recopila **información personal de menores**, lo cual **exige el consentimiento explícito de los tutores legales**.
	- Aunque en su política mencionan que **los datos del menor son controlados por la cuenta del padre, madre o persona cuidadora**, no queda claro cómo y cuándo se solicita ese consentimiento informado ni si se valida la edad.
	- Desde un enfoque de **privacidad por diseño**, esto es insuficiente y roza una **violación potencial de los derechos de la infancia** al no garantizar mecanismos claros de protección.
- **Compatibilidad entre funcionalidad y principios de minimización de datos**
	- El nivel de acceso remoto que se ofrece **no guarda proporción con la función declarada** de acompañamiento o seguridad infantil. Grabar audio, video y pantalla completa en tiempo real puede **exceder con lo necesario** para fines de supervisión legítimos.
	- El diseño actual de la aplicación parece estar **orientado al control total, no al acompañamiento respetuoso**.

### Conclusión especifica

La aplicación, aunque es funcional y aparentemente amigable para las personas cuidadoras,**transgrede los límites aceptables del acompañamiento parental digital**, al permitir prácticas que se asemejan a una vigilancia no consensuada, desproporcionada y opaca. Su modelo de funcionamiento **prioriza el control por sobre la confianza**, y su arquitectura **no incorpora principios básicos de protección de la infancia**, como la privacidad por diseño, la proporcionalidad en el tratamiento de datos o la claridad en el consentimiento.
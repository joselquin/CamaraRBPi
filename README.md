# CamaraRBPi
Con este proyecto se consigue controlar una cámara con una RaspberryPi con la 3 y Telegram.

Además, también se pueden recibir datos de la RBP en Telegram.

1.- Bot Telegram

El primer paso consiste en crear un bot de Telegram con el que se controlará las RBP (el proyecto está probado con una 3 model B, pero seguramente funcionará bien con otros).

Para crear el bot seguimos los siguientes pasos:

   1.1. Desde la app de Telegram (yo uso la app de Android, pero posiblemente se pueda hacer igual desde IOS o desde la webapp), buscamos BotFather y escribimos:

            /newbot

   1.2. BotFather nos pide el nombre, que es como aparecerá en tus chats de Telegram. En este caso lo he llamado "ControlRBP".

   1.3. Ahora nos pide el nombre de usuario para el bot. Tiene que terminar en "bot". En este caso, lo he llamado "ControlRBPbot".

   1.4. BotFather nos manda ahora un mensaje diciendo que ha creado ya el bot y una serie de instrucciones. Aquí es importante anotar el token para acceder a la HTTP API. Es un código largo, de 48 caractéres alfanuméricos.

   1.5. Ya podemos acceder al bot, a través de la dirección t.me/ControlRBPbot.

![Creación del bot](https://github.com/joselquin/CamaraRBPi/blob/main/imagenes/Imagen1.png)

2.- Programación del bot.

Este paso lo hacemos ya en la RBP. Metemos en un editor (yo uso XXXXXX) el programa bot_telegram.py que está en este repositorio. 

Es necesario cambiar las variables:

      tiroriro
      tiroriro2

La primera es el token que nos dió BotFather. EL segundo es el ID de usuario que podremos ver en la termnal de la RBP al ejecutar el programa. De momento puede ponerse un código cualquiera aleatorio. 

Ejecutamos el programa desde la terminal:

        python bot_telegram.py
        
3.- Control desde el bot.

Ahora ya podemos ir al bot de Telegram, desde la app o desde la webapp, y ejecutar los comandos, que viene como un mosaico debajo de la barra de entrada de texto. 

Dado que hasta ahora tenemnos programado un ID de usuario aleatorio, en la terminal de RBP veremos que nos sale un mensaje "Acceso denegado", pero también nos muestra el código que necesitamos. VOlvemos al programa en la RBP, modificamos el ID de usuario, grabamos y lo volvemos a ejecutar en la terminal. Ahora ya debería funcionar todo correctamente.

![Arranque del bot](https://github.com/joselquin/CamaraRBPi/blob/main/imagenes/Imagen2.png)

En este programa tenemos habilitados de momento los siguientes:

    
![Sacar una foto con el bot](https://github.com/joselquin/CamaraRBPi/blob/main/imagenes/Imagen3.png)


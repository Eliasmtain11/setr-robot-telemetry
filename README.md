# SETR-Robot-Telemetry

## Descripcion
Este repositorio contiene la configuración y las instrucciones necesarias para desplegar un sistema de telemetría de robots utilizando Node-RED. El proyecto permite la recepción de datos en tiempo real mediante MQTT, su procesamiento mediante flujos visuales y su visualización a través de una interfaz gráfica (Dashboard) accesible desde un navegador web.

<img width="946" height="368" alt="image" src="https://github.com/user-attachments/assets/7dccb37e-587d-4679-b01f-2ed0cc767d8d" />

## Instalación
1. Instalamos `Node.js` y `npm`
```bash
$ sudo apt update
$ sudo apt install nodejs npm
```
Para comprobar que estan instalados 
```bash
$ node -v
$ npm -v
```

2. Instalamos `Node-RED`
```bash
$ sudo npm install -g --unsafe-perm node-red
```

## Uso
1. Arrancamos `Node-RED` ejecutando el comando
```bash
$ node-red
```
Una vez arrancado nos saldrá el mensaje `Server now running at http://127.0.0.1:1880/` entonces copiaremos esa `ip` en nuestro buscador y se abrirá la interfaz de **node-red**.  

### Acceso desde otro ordenador
En caso de querer acceder desde otro ordenador ejecutaremos el comando
```bash
$ ifconfig
```
Buscaremos la interfaz `wlo1` y tomaremos la IP que aparece en el campo `inet`, a continuación, la introducimos en el navegador con el puerto correspondiente
```bash
http://<IP>:1880
```

## Cargar SETR-telemetry
Para cargar la interfaz del coche pulsaremos al icono de las **3 rayitas**, después **importar** y buscaremos el archivo `SETR-telemetry.json`, despues le daremos a **instalar todo**.
<img width="1914" height="600" alt="image" src="https://github.com/user-attachments/assets/5acf0543-3c91-44f5-ab82-744c25c36e26" />

Una vez cargado el archivo pulsaremos al boton de **Instanciar/Deploy**
<img width="1632" height="682" alt="image" src="https://github.com/user-attachments/assets/69f8e1c0-2ea9-4484-bdb8-019c2d943c95" />

## Uso de la interfaz
Para hacer uso de la interfaz, cambiaremos `http://127.0.0.1:1880/#flow/91d8e7385a2e2b66` por `http://127.0.0.1:1880/ui`, en la sección de grupo, introduciremos el grupo correspondiente para visualizar únicamente los mensajes de ese grupo.
<img width="1111" height="434" alt="image" src="https://github.com/user-attachments/assets/a655e51a-86a0-496c-b58f-b71921569854" />

---------------------------------
### Autor
Elías Muñoz Tain - Grado en Ingeniería Robótica - URJC

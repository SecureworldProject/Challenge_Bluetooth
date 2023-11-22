# Challenge_Bluetooth

Este challenge comprueba si hay un dispositivo cerca del PC. El challenge devuelve la dirección 'name+MAC' del dispositivo objetivo si está cerca y 0000 en caso contrario. Se considera parental porque comprueba la condición de la existencia o no de un determinado dispositivo con un nombre determinado

Esto permite controlar si el PC está cerca de un dispositivo específico por motivos de seguridad.
Por ejemplo, podría controlar si un empleado está junto a un dispositivo fijo en la oficina o en cualquier otro lugar específico, o si lleva consigo un dispositivo de seguridad.
Usa bluetooth, en particular la librería`pybluez`.

## Install pybluez in Windows 10

Primero instala [Windows SDK](https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/)

Segundo, descarga e instala las builds de Windows 10 [build tools](https://www.microsoft.com/es-ES/download/confirmation.aspx?id=48159)

Tercer, clona [pybluez](https://github.com/pybluez/pybluez)

Cuarto, como administrador, dentro del repositorio: `python setup.py install`

## Funcionamiento

Todas las funciones y la lógica del challenge se encuentran en el fichero bluetooth_challenge.py, el cual es un programa en python que contiene toda la lógica del challenge. La función principal dentro del fichero que gestiona toda la lógica del challenge es bluetooth.discover_devices(), la cual devuelve la lista de dispositivos que se encuentran dentro del rango del ordenador y tienen el Bluetooth activado. Asimismo, toda la lógica del challenge se ejecuta dentro de la función executeChallenge( ).

Primero se llama a bluetooth.discover_devices(), mediante la cual se obtiene la lista de dispositivos cercanos que tienen el Bluetooth activado. A la hora de llamar al método, es importante especificar como parámetro de la función: lookup_names=True, ya que esto hace que se devuelvan los nombres de los dispositivos. En base a esa lista se genera un array que contiene todos los dispositivos. Se comprueba si el dispositivo objetivo se encuentra en ese array y en función de eso se genera la clave.

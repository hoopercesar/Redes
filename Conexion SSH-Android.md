# Ingresar por ssh al Android
Vamos a revisar los comandos básicos para poder acceder desde tu consola Linux a tu teléfono Android

## Instalar emulador de consola en Android
1. Primero debes instalar un emulador de consola. Termux es la más recomendada.
Lo importante es instalar una versión actualizada. 
Te recomiendo usar F-Droid para ése ojetivo. 
También lo puedes hacer con play-store, pero la versión que descargué estaba obsoleta.

2. Una vez instalado termux verifica si tienes ifconfig, escribiendo en la consola termux
```
ifconfig
```
Si no, debes instalarlo con
```
pkg install ifconfig
```
4. Si lo tienes instalado, debería retornar información de tu conexión a la red, local o móvil.
La información importante está, en conexión local, en _inet_
```
wlan0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
inet _IP_DE_TU_ANDROID_  netmask 255.255.255.0  broadcast _Otro_valor_
unspec 00-00-00-00-00-00-00-00-00-00-00-00-00-00-00-00  txqueuelen 1000  (UNSPEC)
```
### Instalar ssh en android y configuración
```
pkg install openssh
```








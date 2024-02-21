# Ingresar por ssh al Android
Vamos a revisar los comandos básicos para poder acceder desde tu consola Linux a tu teléfono Android

### Instalar emulador de consola en Android: Termux
1. Primero debes instalar en tu android un emulador de consola. Termux es la más recomendada.
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
1. Instalar ssh
```
pkg update
pkg upgrade
pkg install openssh
```
2. Para iniciar el demonio ejecutamos el siguiente comando
```
sshd
```
3. Para configurar el password
```
passwd usuario
```
Nos pedirá la contraseña para configurar.
Si no sabes cuál es el nombre de usuario, simplemente ejecuta este comando
```
whoami
```
retorna el nombre de usuario.
Bien, con el usuario y el password para el ssh de tu android, puedes conectarte via ssh.

### Establecer conexión
Normalmente, el servidor ssh corre por el puerto 22. Sin embargo, en termux corre por el 8022.
Así, para que se estrablezca la conexión debes ejecutar este comando
```
ssh usuario@IP_DE_TU_ANDROID -p 8022
```
Te pedirá la contraseña. 
La conexión se ha producido. 







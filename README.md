# Redes
Estudio de auditoria y gestión de redes

# Install wireshark ubuntu 22.04
sudo apt update && sudo apt upgrade
sudo apt install wireshark

# configurar super usuario para permisos
su
# si olvidaste tu password de super usuario
# o si nunca lo configuraste
sudo passwd root
# te pide que escribas el nuevo password 

# tus atribuciones como 'su' no son las mismas 
# que las atribuciones y permisos de usuario normal

# en modo 'su' puedes ingresar al grupo de wireshark con los permisos pertinentes
usermod -a -G wireshark _tu_nombre_usuario_
# en mi caso 
usermod -a -G wireshark cesar

# regresar a su cuenta de usuario
su _tu_nombre_usuario_

# iniciar wireshark
wireshark




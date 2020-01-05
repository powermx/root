#!/bin/bash
echo "Este sencillo script te permitirá habilitar tu cuenta root"
echo "Iniciando"
sed -i '/PasswordAuthentication/d' /etc/ssh/sshd_config
sed -i '/PermitRootLogin/d' /etc/ssh/sshd_config
echo '
Port 22
PermitRootLogin yes
PubkeyAuthentication yes
PasswordAuthentication yes
' >> /etc/ssh/sshd_config
service ssh restart
echo "Ahora agregaremos un password a tu cuenta root"
passwd root
echo "Listo!!"
rm root

# Samba-Share-Folder
sudo apt-get install samba
sudo useradd reboot
sudo smbpasswd -a reboot
mkdir RebootScripts
chmod 777 RebootScripts/
sudo nano /etc/samba/smb.conf
Al final del fichero
[RebootScripts]

path = /home/adrian/RebootScripts
valid users = reboot
read only = no

sudo service smbd restart

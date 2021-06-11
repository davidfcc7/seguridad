# instalacion de paquetes
sudo apt install build-essential libgd-dev openssl libssl-dev unzip apache2 php gcc libdbi-perl libdbd-mysql-perl

# descargar nagios
wget https://assets.nagios.com/downloads/nagioscore/releases/nagios-4.4.4.tar.gz -O nagioscore.tar.gz

# descomprimir
tar xvzf nagioscore.tar.gz

# configurar nagios
sudo ./configure --with-https-conf=/etc/apache2/sites-enabled
sudo make all
sudo make install 
#  en caso de error al instalar ejecutar antes del install 
{sudo make install-groups-users
sudo usermod -a -G nagios www-data}

#Aporte del usuario @diegohernanvillalobos
#Si no les funciona "sudo make install" continuar con los siguientes comandos y ejecutar luego "sudo make install"
sudo make install-groups-users
sudo usermod -a -G nagios www-data
#Hasta aquí

sudo make install-init
sudo make install-commandmode
sudo make install-config
sudo make install-webconf

# activar nagios
sudo systemctl start nagios

# instalar plugins de nagios
wget https://nagios-plugins.org/download/nagios-plugins-2.2.1.tar.gz -O nagios-plugins.tar.gz
tar xzvf nagios-plugins.tar.gz
# cd nagios-plugins-2.2.1
sudo ./configure
sudo make all
sudo make install
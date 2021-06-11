
Actualizador de paquetes APT (Debian, Ubuntu y derivados)





Ver el contenido de un fichero
cat file1: ver los contenidos de un fichero comenzando desde la primera hilera.
tac file1: ver los contenidos de un fichero comenzando desde la última línea.
more file1: ver el contenido a lo largo de un fichero.
less file1: parecido al commando ‘more’ pero permite salvar el movimiento en el fichero así como el movimiento hacia atrás.
head -2 file1: ver las dos primeras líneas de un fichero.
tail -2 file1: ver las dos últimas líneas de un fichero.
tail -f /var/log/messages: ver en tiempo real qué ha sido añadido al fichero.
cat file1 file2 .. | command <> file1_in.txt_or_file1_out.txt: sintaxis general para la manipulación de texto utilizando PIPE, STDIN y STDOUT.
cat file1 | command( sed, grep, awk, grep, etc…) > result.txt: sintaxis general para manipular un texto de un fichero y escribir el resultado en un fichero nuevo.
cat file1 | command( sed, grep, awk, grep, etc…) » result.txt: sintaxis general para manipular un texto de un fichero y añadir resultado en un fichero existente.
grep Aug /var/log/messages: buscar palabras “Aug” en el fichero ‘/var/log/messages’.
grep ^Aug /var/log/messages: buscar palabras que comienzan con “Aug” en fichero ‘/var/log/messages’
grep [0-9] /var/log/messages: seleccionar todas las líneas del fichero ‘/var/log/messages’ que contienen números.
grep Aug -R /var/log/*: buscar la cadena “Aug” en el directorio ‘/var/log’ y debajo.
sed ‘s/stringa1/stringa2/g’ example.txt: reubicar “string1” con “string2” en ejemplo.txt
sed ‘/^$/d’ example.txt: eliminar todas las líneas en blanco desde el ejemplo.txt
sed ‘/ *#/d; /^$/d’ example.txt: eliminar comentarios y líneas en blanco de ejemplo.txt
echo ‘esempio’ | tr ‘[:lower:]’ ‘[:upper:]’: convertir minúsculas en mayúsculas.
sed -e ‘1d’ result.txt: elimina la primera línea del fichero ejemplo.txt
sed -n ‘/stringa1/p’: visualizar solamente las líneas que contienen la palabra “string1”.


Establecer caracter y conversión de ficheros
dos2unix filedos.txt fileunix.txt: convertir un formato de fichero texto desde MSDOS a UNIX.
unix2dos fileunix.txt filedos.txt: convertir un formato de fichero de texto desde UNIX a MSDOS.
recode ..HTML < page.txt > page.html: convertir un fichero de texto en html.
recode -l | more: mostrar todas las conversiones de formato disponibles.
Análisis del sistema de ficheros
badblocks -v /dev/hda1: Chequear los bloques defectuosos en el disco hda1.
fsck /dev/hda1: reparar / chequear la integridad del fichero del sistema Linux en el disco hda1.
fsck.ext2 /dev/hda1: reparar / chequear la integridad del fichero del sistema ext 2 en el disco hda1.
e2fsck /dev/hda1: reparar / chequear la integridad del fichero del sistema ext 2 en el disco hda1.
e2fsck -j /dev/hda1: reparar / chequear la integridad del fichero del sistema ext 3 en el disco hda1.
fsck.ext3 /dev/hda1: reparar / chequear la integridad del fichero del sistema ext 3 en el disco hda1.
fsck.vfat /dev/hda1: reparar / chequear la integridad del fichero sistema fat en el disco hda1.
fsck.msdos /dev/hda1: reparar / chequear la integridad de un fichero del sistema dos en el disco hda1.
dosfsck /dev/hda1: reparar / chequear la integridad de un fichero del sistema dos en el disco hda1.
Formatear un sistema de ficheros
mkfs /dev/hda1: crear un fichero de sistema tipo Linux en la partición hda1.
mke2fs /dev/hda1: crear un fichero de sistema tipo Linux ext 2 en hda1.
mke2fs -j /dev/hda1: crear un fichero de sistema tipo Linux ext3 (periódico) en la partición hda1.
mkfs -t vfat 32 -F /dev/hda1: crear un fichero de sistema FAT32 en hda1.
fdformat -n /dev/fd0: formatear un disco flooply.
mkswap /dev/hda3: crear un fichero de sistema swap.
Trabajo con la SWAP
mkswap /dev/hda3: crear fichero de sistema swap.
swapon /dev/hda3: activando una nueva partición swap.
swapon /dev/hda2 /dev/hdb3: activar dos particiones swap.
Salvas (Backup)
dump -0aj -f /tmp/home0.bak /home: hacer una salva completa del directorio ‘/home’.
dump -1aj -f /tmp/home0.bak /home: hacer una salva incremental del directorio ‘/home’.
restore -if /tmp/home0.bak: restaurando una salva interactivamente.
rsync -rogpav –delete /home /tmp: sincronización entre directorios.
rsync -rogpav -e ssh –delete /home ip_address:/tmp: rsync a través del túnel SSH.
rsync -az -e ssh –delete ip_addr:/home/public /home/local: sincronizar un directorio local con un directorio remoto a través de ssh y de compresión.
rsync -az -e ssh –delete /home/local ip_addr:/home/public: sincronizar un directorio remoto con un directorio local a través de ssh y de compresión.
dd bs=1M if=/dev/hda | gzip | ssh user@ip_addr ‘dd of=hda.gz’: hacer una salva de un disco duro en un host remoto a través de ssh.
dd if=/dev/sda of=/tmp/file1: salvar el contenido de un disco duro a un fichero. (En este caso el disco duro es “sda” y el fichero “file1”).
tar -Puf backup.tar /home/user: hacer una salva incremental del directorio ‘/home/user’.
( cd /tmp/local/ && tar c . ) | ssh -C user@ip_addr ‘cd /home/share/ && tar x -p’: copiar el contenido de un directorio en un directorio remoto a través de ssh.
( tar c /home ) | ssh -C user@ip_addr ‘cd /home/backup-home && tar x -p’: copiar un directorio local en un directorio remoto a través de ssh.
tar cf – . | (cd /tmp/backup ; tar xf – ): copia local conservando las licencias y enlaces desde un directorio a otro.
find /home/user1 -name ‘*.txt’ | xargs cp -av –target-directory=/home/backup/ –parents: encontrar y copiar todos los ficheros con extensión ‘.txt’ de un directorio a otro.
find /var/log -name ‘*.log’ | tar cv –files-from=- | bzip2 > log.tar.bz2: encontrar todos los ficheros con extensión ‘.log’ y hacer un archivo bzip.
dd if=/dev/hda of=/dev/fd0 bs=512 count=1: hacer una copia del MRB (Master Boot Record) a un disco floppy.
dd if=/dev/fd0 of=/dev/hda bs=512 count=1: restaurar la copia del MBR (Master Boot Record) salvada en un floppy.
CD-ROM
cdrecord -v gracetime=2 dev=/dev/cdrom -eject blank=fast -force: limpiar o borrar un cd regrabable.
mkisofs /dev/cdrom > cd.iso: crear una imagen iso de cdrom en disco.
mkisofs /dev/cdrom | gzip > cd_iso.gz: crear una imagen comprimida iso de cdrom en disco.
mkisofs -J -allow-leading-dots -R -V “Label CD” -iso-level 4 -o ./cd.iso data_cd: crear una imagen iso de un directorio.
cdrecord -v dev=/dev/cdrom cd.iso: quemar una imagen iso.
gzip -dc cd_iso.gz | cdrecord dev=/dev/cdrom –: quemar una imagen iso comprimida.
mount -o loop cd.iso /mnt/iso: montar una imagen iso.
cd-paranoia -B: llevar canciones de un cd a ficheros wav.
cd-paranoia – ”-3”: llevar las 3 primeras canciones de un cd a ficheros wav.
cdrecord –scanbus: escanear bus para identificar el canal scsi.
dd if=/dev/hdc | md5sum: hacer funcionar un md5sum en un dispositivo, como un CD.
Trabajo con la RED ( LAN y Wi-Fi)
ifconfig eth0: mostrar la configuración de una tarjeta de red Ethernet.
ifup eth0: activar una interface ‘eth0’.
ifdown eth0: deshabilitar una interface ‘eth0’.
ifconfig eth0 192.168.1.1 netmask 255.255.255.0: configurar una dirección IP.
ifconfig eth0 promisc: configurar ‘eth0’en modo común para obtener los paquetes (sniffing).
dhclient eth0: activar la interface ‘eth0’ en modo dhcp.
route -n: mostrar mesa de recorrido.
route add -net 0/0 gw IP_Gateway: configurar entrada predeterminada.
route add -net 192.168.0.0 netmask 255.255.0.0 gw 192.168.1.1: configurar ruta estática para buscar la red ‘192.168.0.0/16’.
route del 0/0 gw IP_gateway: eliminar la ruta estática.
echo “1” > /proc/sys/net/ipv4/ip_forward: activar el recorrido ip.
hostname: mostrar el nombre del host del sistema.
host www.example.com: buscar el nombre del host para resolver el nombre a una dirección ip(1).
nslookup www.example.com: buscar el nombre del host para resolver el nombre a una direccióm ip y viceversa(2).
ip link show: mostar el estado de enlace de todas las interfaces.
mii-tool eth0: mostar el estado de enlace de ‘eth0’.
ethtool eth0: mostrar las estadísticas de tarjeta de red ‘eth0’.
netstat -tup: mostrar todas las conexiones de red activas y sus PID.
netstat -tupl: mostrar todos los servicios de escucha de red en el sistema y sus PID.
tcpdump tcp port 80: mostrar todo el tráfico HTTP.
iwlist scan: mostrar las redes inalámbricas.
iwconfig eth1: mostrar la configuración de una tarjeta de red inalámbrica.
whois www.example.com: buscar en base de datos Whois.
Redes de Microsoft Windows (SAMBA)
nbtscan ip_addr: resolución de nombre de red bios.
nmblookup -A ip_addr: resolución de nombre de red bios.
smbclient -L ip_addr/hostname: mostrar acciones remotas de un host en windows.
Tablas IP (CORTAFUEGOS)
iptables -t filter -L: mostrar todas las cadenas de la tabla de filtro.
iptables -t nat -L: mostrar todas las cadenas de la tabla nat.
iptables -t filter -F: limpiar todas las reglas de la tabla de filtro.
iptables -t nat -F: limpiar todas las reglas de la tabla nat.
iptables -t filter -X: borrar cualquier cadena creada por el usuario.
iptables -t filter -A INPUT -p tcp –dport telnet -j ACCEPT: permitir las conexiones telnet para entar.
iptables -t filter -A OUTPUT -p tcp –dport http -j DROP: bloquear las conexiones HTTP para salir.
iptables -t filter -A FORWARD -p tcp –dport pop3 -j ACCEPT: permitir las conexiones POP a una cadena delantera.
iptables -t filter -A INPUT -j LOG –log-prefix “DROP INPUT”: registrando una cadena de entrada.
iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE: configurar un PAT (Puerto de traducción de dirección) en eth0, ocultando los paquetes de salida forzada.
iptables -t nat -A PREROUTING -d 192.168.0.1 -p tcp -m tcp –dport 22 -j DNAT –to-destination 10.0.0.2:22: redireccionar los paquetes diriguidos de un host a otro.
Monitoreando y depurando
top: mostrar las tareas de linux usando la mayoría cpu.
ps -eafw: muestra las tareas Linux.
ps -e -o pid,args –forest: muestra las tareas Linux en un modo jerárquico.
pstree: mostrar un árbol sistema de procesos.
kill -9 ID_Processo: forzar el cierre de un proceso y terminarlo.
kill -1 ID_Processo: forzar un proceso para recargar la configuración.
lsof -p $$: mostrar una lista de ficheros abiertos por procesos.
lsof /home/user1: muestra una lista de ficheros abiertos en un camino dado del sistema.
strace -c ls >/dev/null: mostrar las llamadas del sistema hechas y recibidas por un proceso.
strace -f -e open ls >/dev/null: mostrar las llamadas a la biblioteca.
watch -n1 ‘cat /proc/interrupts’: mostrar interrupciones en tiempo real.
last reboot: mostrar historial de reinicio.
lsmod: mostrar el kernel cargado.
free -m: muestra el estado de la RAM en megabytes.
smartctl -A /dev/hda: monitorear la fiabilidad de un disco duro a través de SMART.
smartctl -i /dev/hda: chequear si SMART está activado en un disco duro.
tail /var/log/dmesg: mostrar eventos inherentes al proceso de carga del kernel.
tail /var/log/messages: mostrar los eventos del sistema.
Otros comandos útiles
apropos …keyword: mostrar una lista de comandos que pertenecen a las palabras claves de un programa; son útiles cuando tú sabes qué hace tu programa, pero de sconoces el nombre del comando.
man ping: mostrar las páginas del manual on-line; por ejemplo, en un comando ping, usar la opción ‘-k’ para encontrar cualquier comando relacionado.
whatis …keyword: muestra la descripción de lo que hace el programa.
mkbootdisk –device /dev/fd0 `uname -r`: crear un floppy boteable.
gpg -c file1: codificar un fichero con guardia de seguridad GNU.
gpg file1.gpg: decodificar un fichero con Guardia de seguridad GNU.
wget -r www.example.com: descargar un sitio web completo.
wget -c www.example.com/file.iso: descargar un fichero con la posibilidad de parar la descargar y reanudar más tarde.
echo ‘wget -c www.example.com/files.iso‘ | at 09:00: Comenzar una descarga a cualquier hora. En este caso empezaría a las 9 horas.
ldd /usr/bin/ssh: mostrar las bibliotecas compartidas requeridas por el programa ssh.
alias hh=’history’: colocar un alias para un commando –hh= Historial.
chsh: cambiar el comando Shell.
chsh –list-shells: es un comando adecuado para saber si tienes que hacer remoto en otra terminal.
who -a: mostrar quien está registrado, e imprimir hora del último sistema de importación, procesos muertos, procesos de registro de sistema, procesos activos producidos por init, funcionamiento actual y últimos cambios del reloj del sistema.
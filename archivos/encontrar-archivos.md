# find / -name file1: 
    buscar fichero y directorio a partir de la raíz del sistema.
# find / -user user1: 
    buscar ficheros y directorios pertenecientes al usuario ‘user1’.
# find /home/user1 -name \*.bin: 
    buscar ficheros con extensión ‘. bin’ dentro del directorio ‘/ home/user1’.
# find /usr/bin -type f -atime +100: 
    buscar ficheros binarios no usados en los últimos 100 días.
# find /usr/bin -type f -mtime -10: 
    buscar ficheros creados o cambiados dentro de los últimos 10 días.
# find / -name \*.rpm -exec chmod 755 ‘{}’ \;: 
    buscar ficheros con extensión ‘.rpm’ y modificar permisos.
# find / -xdev -name \*.rpm: 
    Buscar ficheros con extensión ‘.rpm’ ignorando los dispositivos removibles como cdrom, pen-drive, etc.…
# locate \*.ps: 
    encuentra ficheros con extensión ‘.ps’ ejecutados primeramente con el command ‘updatedb’.
# whereis halt: 
    mostrar la ubicación de un fichero binario, de ayuda o fuente. En este caso pregunta dónde está el comando ‘halt’.
# which halt: 
    mostrar la senda completa (el camino completo) a un binario / ejecutable.
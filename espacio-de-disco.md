# df -h: 
    mostrar una lista de las particiones montadas.
# ls -lSr |more: 
    mostrar el tamaño de los ficheros y directorios ordenados por tamaño.
# du -sh dir1: 
    Estimar el espacio usado por el directorio ‘dir1’.
# du -sk * | sort -rn: 
    mostrar el tamaño de los ficheros y directorios ordenados por tamaño.
# rpm -q -a –qf ‘%10{SIZE}t%{NAME}n’ | sort -k1,1n: 
    mostrar el espacio usado por los paquetes rpm instalados organizados por tamaño (Fedora, Redhat y otros).
# dpkg-query -W -f=’${Installed-Size;10}t${Package}n’ | sort -k1,1n: 
    mostrar el espacio usado por los paquetes instalados, organizados por tamaño (Ubuntu, Debian y otros).
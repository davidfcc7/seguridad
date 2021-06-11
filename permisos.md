# dueño         |
    rwx (111)   |
# grupo         |
    r-x (101)   | 755
# publico       |
    r-x (101)   |

    r => 4
    w => 2
    x => 1

    -rwxr-xr-x = > 755

# modo simbolico
u ---> solo para el usuario
g ---> solo para el grupo
o ---> solo para otros (publico)
a ---> aplica para todos

# ls -l
    ver permisos de un archivo y otras caracteristicas

# chmod 755 archivo
    permisos de lectura y ejecucion
# chmod u-r archivo
    quitar permisos de lectura
# chmod u+r archivo
    colocar permisos de lectura
# chmod u-x,go=w archivo
    quitar permisos de ejecucion al usario y colocar permisos de escritura para grupos y publicos

# whoami
    cual es mi nombre de usuario
# su root
    cambiar al usuario de root

# printenv
    Variables de entorno

# chmod u+x ejemplo.txt
    asigna solamente al usuario el permiso de ejecucion

# ls -lh: 
Mostrar permisos.
# ls /tmp | pr -T5 -W$COLUMNS: 
dividir la terminal en 5 columnas.
# chmod ugo+rwx directory1: 
colocar permisos de lectura ®, escritura (w) y ejecución(x) al propietario (u), al grupo (g) y a otros (o) sobre el directorio ‘directory1’.
# chmod go-rwx directory1: 
quitar permiso de lectura ®, escritura (w) y (x) ejecución al grupo (g) y otros (o) sobre el directorio ‘directory1’.
# chown user1 file1: 
cambiar el dueño de un fichero.
# chown -R user1 directory1: 
cambiar el propietario de un directorio y de todos los ficheros y directorios contenidos dentro.
# chgrp group1 file1: 
cambiar grupo de ficheros.
# chown user1:group1 file1: 
cambiar usuario y el grupo propietario de un fichero.
# find / -perm -u+s: 
visualizar todos los ficheros del sistema con SUID configurado.
# chmod u+s /bin/file1: 
colocar el bit SUID en un fichero binario. El usuario que corriendo ese fichero adquiere los mismos privilegios como dueño.
# chmod u-s /bin/file1: 
deshabilitar el bit SUID en un fichero binario.
# chmod g+s /home/public: 
colocar un bit SGID en un directorio –similar al SUID pero por directorio.
# chmod g-s /home/public: 
desabilitar un bit SGID en un directorio.
# chmod o+t /home/public: 
colocar un bit STIKY en un directorio. Permite el borrado de ficheros solamente a los dueños legítimos.
# chmod o-t /home/public: 
desabilitar un bit STIKY en un directorio.
# chattr +a file1: 
permite escribir abriendo un fichero solamente modo append.
# chattr +c file1: 
permite que un fichero sea comprimido / descomprimido automaticamente.
# chattr +d file1: 
asegura que el programa ignore borrar los ficheros durante la copia de seguridad.
# chattr +i file1: 
convierte el fichero en invariable, por lo que no puede ser eliminado, alterado, renombrado, ni enlazado.
# chattr +s file1: 
permite que un fichero sea borrado de forma segura.
# chattr +S file1: 
asegura que un fichero sea modificado, los cambios son escritos en modo synchronous como con sync.
# chattr +u file1: 
te permite recuperar el contenido de un fichero aún si este está cancelado.
# lsattr: 
mostrar atributos especiales.
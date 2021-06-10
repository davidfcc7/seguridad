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
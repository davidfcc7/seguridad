# sistema de archivos
/
    etc
    dev
    home
        jono
            work
            photos
        mako
        cory
    usr
        lib
    var

# ls
listar la carpeta donde estamos ubicados
   # ls -l
   linstarlos archivos con informacion de tammaño en bits y creacion
   # ls -lh
   listar archivos con informacion de tamaño detallada
   # ls -la
   muestra todos los archivos ocultos
   # ls -lS
   organizar todos los documentos por tamaño
   # ls -lr
   mostrar los archivos ordenados de atras en adelante

# tree
ordenar todos los archivos existentes en un arbol
   # tree -L 2
   ordenar los archivos en arbol por niveles (2)

# clear o ctrl + L
limpiar la pantalla de la terminal

# pwd
ver en que direccion estoy

# ctrl + shift + c / click derecho
copiar o pegar texto dentro de la terminal 

# ./directorio/archivo
el . nos permite movernos mas rapido entre directorios sin necesidad de escribir toda la ruta
   # ..
   devolverme un directorio

# file 
conocer el detalles del archivo

# mkdir
crear un directorio

# touch
crear un archivo

# cp file file_copia
copia el archivo file y lo pega con el nompre file_copia (los nombres son de ejemplo)

# mv file_copia ../directorio
mueve un archivo a otro directorio 
   # mv file_copia fileCopy
   reenombra el archivo o directorio

# rm
remover un archivo
   # rm -i 
   muestra alerta para estar seguro de querer borrar
   # rm -r
   remover un directorio
   # rm -ri
   muestra una alerta antes de remover
   # rm -rf
   remover un directorio a la fuerza

# head archivo
muestra las primeras 10 lineas de un archivo
   # head archivo -n 15
   muestra las primeras 15 lineas del archivo

# tail archivo
muestra las ultimas 10 lineas de un archivo
   # tail archivo -n 15
   muestra las ultimas 15 lineas de un archivo

# alias
se utiliza para crear comandos (alias l="ls -lh") y son temporales

# man / info
manual de usuario de un comando

# ls *.js / mv *.js / cp *.js / rm *.js
muestra/mueve/copia o remueve todos los archivos de esta extencion  

# echo mensaje
    muestra el mensaje almacenado

# cat 
    concatenar dos archivos

#### -------------------    OPERADORES DE CONTROL   ------------------------------

# ls; mkdir hola; cal
    ejecutar comandos de forma sincrona (;)
# ls & date & cal
    ejecutar de manera asincrona (&)
# mkdir test && cd test 
    (si la carpeta test se crea dirijame directamente a ella)
    ejecutar comandos condicionales
# mkdir test || cd test
    comendos condicionales (o se cumple una condicion o la otra)
    
#### -------------------    PERMISOS     ------------------------------

# dueño         |
    rwx (111)   |
# grupo         |
    r-x (101)   | 755
# publico       |
    r-x (101)   |

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

#### -------------------    COMANDOS DE BUSQUEDA     ------------------------------

# which archivo
    busca un archivo y muestra donde está alojado
# find ./ -name archivo
    busca un archivo desde una ruta especifica
# find ./ -name *.txt
    busca tosdos los archivo segun la extencion y la ruta 
# find ./ -size 20M
    busca todos los archivos que sean mayores a 20 mb
# grep
    buscar una palabra en un archivo
# wc
    ver la cantidad de palabras que tiene el archivo
    

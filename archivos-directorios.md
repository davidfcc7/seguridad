# cd /home: 
    entrar en el directorio “home”.
# cd ..: 
    retroceder un nivel.
# cd ../..: 
    retroceder 2 niveles.
# cd: 
    ir al directorio raíz.
# cd ~user1: 
    ir al directorio user1.
# cd –: 
    ir (regresar) al directorio anterior.
# pwd: 
    mostrar el camino del directorio de trabajo.
# ls: 
    ver los ficheros de un directorio.
# ls -F: 
    ver los ficheros de un directorio.
# ls -l: 
    mostrar los detalles de ficheros y carpetas de un directorio.
# ls -a: 
    mostrar los ficheros ocultos.
# ls *[0-9]*: 
    mostrar los ficheros y carpetas que contienen números.
# tree: 
    mostrar los ficheros y carpetas en forma de árbol comenzando por la raíz.(1)
# lstree: 
    mostrar los ficheros y carpetas en forma de árbol comenzando por la raíz.(2)
# mkdir dir1: 
    crear una carpeta o directorio con nombre ‘dir1’.
# mkdir dir1 dir2: 
    crear dos carpetas o directorios simultáneamente (Crear dos directorios a la vez).
# mkdir -p /tmp/dir1/dir2: 
    crear un árbol de directorios.
# rm -f file1: 
    borrar el fichero llamado ‘file1’.
# rmdir dir1: 
    borrar la carpeta llamada ‘dir1’.
# rm -rf dir1: 
    eliminar una carpeta llamada ‘dir1’ con su contenido de forma recursiva. (Si lo borro recursivo estoy diciendo que es con su contenido).
# rm -rf dir1 dir2: 
    borrar dos carpetas (directorios) con su contenido de forma recursiva.
# mv dir1 new_dir: 
    renombrar o mover un fichero o carpeta (directorio).
# cp file1: 
    copiar un fichero.
# cp file1 file2: 
    copiar dos ficheros al unísono.
# cp dir /* .: 
    copiar todos los ficheros de un directorio dentro del directorio de trabajo actual.
# cp -a /tmp/dir1 .: 
    copiar un directorio dentro del directorio actual de trabajo.
# cp -a dir1: 
    copiar un directorio.
# cp -a dir1 dir2: 
    copiar dos directorio al unísono.
# ln -s file1 lnk1: 
    crear un enlace simbólico al fichero o directorio.
# ln file1 lnk1: 
    crear un enlace físico al fichero o directorio.
# touch -t 0712250000 file1: 
    modificar el tiempo real (tiempo de creación) de un fichero o directorio.
# file file1: 
    salida (volcado en pantalla) del tipo mime de un fichero texto.
# iconv -l: 
    listas de cifrados conocidos.
# iconv -f fromEncoding -t toEncoding inputFile > outputFile: 
    crea una nueva forma del fichero de entrada asumiendo que está codificado en fromEncoding y convirtiéndolo a ToEncoding.
# find . -maxdepth 1 -name *.jpg -print -exec convert ”{}” -resize 80×60 “thumbs/{}” \;: 
    agrupar ficheros redimensionados en el directorio actual y enviarlos a directorios en vistas de miniaturas (requiere convertir desde ImagemagicK).


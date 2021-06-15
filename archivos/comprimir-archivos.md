# tar -cvf ejemplo.tar ejemplo/
    comprimir un archivo a .tar
# tar -cvzf ejemplo.tar.gz ejemplo/ / tar -xzvf ejemplo.tar.gz
    comprimir un archivo a .tar y convertirlo en gzip / descomprimir un archivo gzip
# zip -r ejemplo.zip ejemplo/ unzip ejemplo.zip
    comprimir archivo en gzip / descomprimir

# bunzip2 file1.bz2: 
descomprime in fichero llamado ‘file1.bz2’.
# bzip2 file1: 
comprime un fichero llamado ‘file1’.
# gunzip file1.gz: 
descomprime un fichero llamado ‘file1.gz’.
# gzip file1: 
comprime un fichero llamado ‘file1’.
# gzip -9 file1: 
comprime con compresión máxima.
# rar a file1.rar test_file: 
crear un fichero rar llamado ‘file1.rar’.
# rar a file1.rar file1 file2 dir1: 
comprimir ‘file1’, ‘file2’ y ‘dir1’ simultáneamente.
# rar x file1.rar: 
descomprimir archivo rar.
# unrar x file1.rar: 
descomprimir archivo rar.
# tar -cvf archive.tar file1: 
crear un tarball descomprimido.
# tar -cvf archive.tar file1 file2 dir1: 
crear un archivo conteniendo ‘file1’, ‘file2′ y’dir1’.
# tar -tf archive.tar: 
mostrar los contenidos de un archivo.
# tar -xvf archive.tar: 
extraer un tarball.
# tar -xvf archive.tar -C /tmp: 
extraer un tarball en / tmp.
# tar -cvfj archive.tar.bz2 dir1: 
crear un tarball comprimido dentro de bzip2.
# tar -xvfj archive.tar.bz2: 
descomprimir un archivo tar comprimido en bzip2
# tar -cvfz archive.tar.gz dir1: 
crear un tarball comprimido en gzip.
# tar -xvfz archive.tar.gz: 
descomprimir un archive tar comprimido en gzip.
# zip file1.zip file1: 
crear un archivo comprimido en zip.
# zip -r file1.zip file1 file2 dir1: 
comprimir, en zip, varios archivos y directorios de forma simultánea.
# unzip file1.zip: 
descomprimir un archivo zip.
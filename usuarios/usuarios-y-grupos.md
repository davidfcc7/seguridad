# groupadd nombre_del_grupo: 
    crear un nuevo grupo.
# groupdel nombre_del_grupo: 
    borrar un grupo.
# groupmod -n nuevo_nombre_del_grupo viejo_nombre_del_grupo: 
    renombrar un grupo.
# useradd -c “Name Surname ” -g admin -d /home/user1 -s /bin/bash user1: 
    Crear un nuevo usuario perteneciente al grupo “admin”.
# useradd user1: 
    crear un nuevo usuario.
# userdel -r user1: 
    borrar un usuario (‘-r’ elimina el directorio Home).
# usermod -c “User FTP” -g system -d /ftp/user1 -s /bin/nologin user1: 
    cambiar los atributos del usuario.
# passwd: 
    cambiar contraseña.
# passwd user1: 
    cambiar la contraseña de un usuario (solamente por root).
# chage -E 2011-12-31 user1: 
    colocar un plazo para la contraseña del usuario. En este caso dice que la clave expira el 31 de diciembre de 2011.
# pwck: 
    chequear la sintaxis correcta el formato de fichero de ‘/etc/passwd’ y la existencia de usuarios.
# grpck: 
    chequear la sintaxis correcta y el formato del fichero ‘/etc/group’ y la existencia de grupos.
# newgrp group_name: 
    registra a un nuevo grupo para cambiar el grupo predeterminado de los ficheros creados recientemente.
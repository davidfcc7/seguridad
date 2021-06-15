# whoami
quien soy 
# cat /etc/passwd
ver todos los usuarios del sistemas
# cat /etc/shadow
ver contraseñas de los usuarios encriptadas
# passwd 
cambiar contraseña de algun usuario
# adduser usuario
crear usuario / solicita password / nombre / datos personales
# userdel usuario
borrar usuarios
# su - usuario
para cambiarme a un usuario
# groups 
ver los grupos a los que pertenecen los usuarios
# gpasswd -a usuario grupo
agregar un usuario a un grupo
# gpasswd -d usuario grupo
eliminar un usuario de un grupo
# usermod -aG grupo usuario
Agregar a un usuario en un grupo secundario sin darle todos los permisos como administrador
# pwscore
verificar si una contraseña es segura o no
# ulimit -a
ver el maximo de procesos que puede realizar un usuario
# ulimit -u 10 
restringir la cantidad de procesos



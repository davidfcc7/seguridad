# dpkg -i package.deb: 
instalar / actualizar un paquete deb.
# dpkg -r package_name: 
eliminar un paquete deb del sistema.
# dpkg -l: 
mostrar todos los paquetes deb instalados en el sistema.
# dpkg -l | grep httpd: 
mostrar todos los paquetes deb con el nombre “httpd”
# dpkg -s package_name: 
obtener información en un paquete específico instalado en el sistema.
# dpkg -L package_name: 
mostar lista de ficheros dados por un paquete instalado en el sistema.
# dpkg –contents package.deb: 
mostrar lista de ficheros dados por un paquete no instalado todavía.
# dpkg -S /bin/ping: 
verificar cuál paquete pertenece a un fichero dado.
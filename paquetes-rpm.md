# rpm -ivh package.rpm: 
instalar un paquete rpm.
# rpm -ivh –nodeeps package.rpm: 
instalar un paquete rpm ignorando las peticiones de dependencias.
# rpm -U package.rpm: 
actualizar un paquete rpm sin cambiar la configuración de los ficheros.
# rpm -F package.rpm: 
actualizar un paquete rpm solamente si este está instalado.
# rpm -e package_name.rpm: 
eliminar un paquete rpm.
# rpm -qa: 
mostrar todos los paquetes rpm instalados en el sistema.
# rpm -qa | grep httpd: 
mostrar todos los paquetes rpm con el nombre “httpd”.
# rpm -qi package_name: 
obtener información en un paquete específico instalado.
# rpm -qg “System Environment/Daemons”: 
mostar los paquetes rpm de un grupo software.
# rpm -ql package_name: 
mostrar lista de ficheros dados por un paquete rpm instalado.
# rpm -qc package_name: 
mostrar lista de configuración de ficheros dados por un paquete rpm instalado.
# rpm -q package_name –whatrequires: 
mostrar lista de dependencias solicitada para un paquete rpm.
# rpm -q package_name –whatprovides: 
mostar la capacidad dada por un paquete rpm.
# rpm -q package_name –scripts: 
mostrar los scripts comenzados durante la instalación /eliminación.
# rpm -q package_name –changelog: 
mostar el historial de revisions de un paquete rpm.
# rpm -qf /etc/httpd/conf/httpd.conf: 
verificar cuál paquete rpm pertenece a un fichero dado.
# rpm -qp package.rpm -l: 
mostrar lista de ficheros dados por un paquete rpm que aún no ha sido instalado.
# rpm –import /media/cdrom/RPM-GPG-KEY: 
importar la firma digital de la llave pública.
# rpm –checksig package.rpm: 
verificar la integridad de un paquete rpm.
# rpm -qa gpg-pubkey: 
verificar la integridad de todos los paquetes rpm instalados.
# rpm -V package_name: 
chequear el tamaño del fichero, licencias, tipos, dueño, grupo, chequeo de resumen de MD5 y última modificación.
# rpm -Va: 
chequear todos los paquetes rpm instalados en el sistema. Usar con cuidado.
# rpm -Vp package.rpm: 
verificar un paquete rpm no instalado todavía.
# rpm2cpio package.rpm | cpio –extract –make-directories *bin*: 
extraer fichero ejecutable desde un paquete rpm.
# rpm -ivh /usr/src/redhat/RPMS/`arch`/package.rpm: 
instalar un paquete construido desde una fuente rpm.
# rpmbuild –rebuild package_name.src.rpm: 
construir un paquete rpm desde una fuente rpm.
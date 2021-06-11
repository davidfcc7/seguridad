# yum install package_name: 
descargar e instalar un paquete rpm.
# yum localinstall package_name.rpm: 
este instalará un RPM y tratará de resolver todas las dependencies para ti, usando tus repositorios.
# yum update package_name.rpm: 
actualizar todos los paquetes rpm instalados en el sistema.
# yum update package_name: 
modernizar / actualizar un paquete rpm.
# yum remove package_name: 
eliminar un paquete rpm.
# yum list: 
listar todos los paquetes instalados en el sistema.
# yum search package_name: 
Encontrar un paquete en repositorio rpm.
# yum clean packages: 
limpiar un caché rpm borrando los paquetes descargados.
# yum clean headers: 
eliminar todos los ficheros de encabezamiento que el sistema usa para resolver la dependencia.
# yum clean all: 
eliminar desde los paquetes caché y ficheros de encabezado.
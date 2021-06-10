# mount /dev/hda2 /mnt/hda2: 
    montar un disco llamado hda2. Verifique primero la existencia del directorio ‘/ mnt/hda2’; si no está, debe crearlo.
# umount /dev/hda2: 
    desmontar un disco llamado hda2. Salir primero desde el punto ‘/ mnt/hda2.
# fuser -km /mnt/hda2: 
    forzar el desmontaje cuando el dispositivo está ocupado.
# umount -n /mnt/hda2: 
    correr el desmontaje sin leer el fichero /etc/mtab. Útil cuando el fichero es de solo lectura o el disco duro está lleno.
# mount /dev/fd0 /mnt/floppy: 
    montar un disco flexible (floppy).
# mount /dev/cdrom /mnt/cdrom: 
   montar un cdrom / dvdrom.
# mount /dev/hdc /mnt/cdrecorder: 
    montar un cd regrabable o un dvdrom.
# mount /dev/hdb /mnt/cdrecorder: 
    montar un cd regrabable / dvdrom (un dvd).
# mount -o loop file.iso /mnt/cdrom: 
    montar un fichero o una imagen iso.
# mount -t vfat /dev/hda5 /mnt/hda5: 
    montar un sistema de ficheros FAT32.
# mount /dev/sda1 /mnt/usbdisk: 
    montar un usb pen-drive o una memoria (sin especificar el tipo de sistema de ficheros).
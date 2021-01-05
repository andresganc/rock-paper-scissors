
## MOUNT DISC AUTOMATIC

### Paso 1: Listar Disks

    $ sudo fdisk –l

### Paso 2: CONOCER EL UUID DESDE EL TERMINAL

    $ sudo blkid

### Paso 3: Editar el archivo FSTAB

    $ sudo xed /etc/fstab

### Paso 4: Agregar linea de codigo

    $ UUID=5bbbb412-a591-4a0e-a5af-912dde65d645  /media/NC-MULTIMEDIA  ext4  user,errors=remount-ro,auto,exec,rw  0  0


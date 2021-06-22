
# USERS SAMBA


## Ver users & groups

    - Ver los usuarios del sistema
        $ cat /etc/passwd


    - Ver los grupos del sistema
        $ cat /etc/group


## Crear user samba

    - Crear user samba en ubuntu server 20.04LTS

        Nota importante: Para crear un usuario samba este debe de estar creado previamente en el sistema linux


    - Create user en ubuntu server 20.04LTS

        $ sudo useradd usuarionuevo

    - Si queremos que se nos creen las carpetas automáticamente en el directorio /home debemos hacerlo con la opción -m

        $ sudo sueradd -m usuarionuevo

    - En ambos casos si queremos definir una contraseña usaremos el siguiente comando

        $ sudo passwd usuarionuevo



        -a : Esto agrega al usuario al servidor Samba sin habilitarlo.
        -e : Esto habilita un usuario agregado previamente.

        sudo smbpasswd -a andres
        sudo smbpasswd -e andres

        $ sudo smbpasswd -a mi-user
        New SMB password:
        Retype new SMB password:
        Added user linuxconfig.


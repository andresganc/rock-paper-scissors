
### SMB.CONF 

    - Archivo samba para crear los puntos de conexion 

        - Copia de seguridad del archivo smb.config
            $ sudo mv /etc/samba/smb.conf /etc/samba/smb.conf.orig

        - Editar el archivo
            $ sudo vim /etc/samba/smb.conf


        - Reiniciar Samba (Despues de editar el archivo smb.conf) 
            $ sudo systemctl restart smbd

        

### PUNTOS DE CONEXION

    - Ejemplos

    # NC-SERVER-SAMBA01 - NC-SERVER-SAMBA01
        [nc-server-smb-01]
            comment = NC-SERVER-SAMBA01
            path= /home/andres
            read only = no
            public = yes
            guest ok = yes
            browseable = yes
            create mode = 0777
                directory mode = 0777
                #write list = andres
                valid users = andres, alejandragomez, danielagiraldo


    # NC-SERVER-SAMBA01 - NC-ADMIN
        [nc-admin]
                comment = NC-ADMIN
                path= /home/andres/NC-ADMIN
                read only = no
                public = yes
                guest ok = yes
                browseable = yes
                create mode = 0777
                directory mode = 0777
                #write list = @root
                valid users = andres, danielagiraldo
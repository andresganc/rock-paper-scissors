
# ERROR VARIOS DOMINIOS

    - Suceso: Este error se produce cuando se agrega un dominio nuevo

    - Error: Al agregar el dominio nuevo los otros dominios quedan con la web igual.

    - Motivo: Esto se produce porque ISPConfig no tiene definido los VirtualHost correctamente.
        esta preparado solo para tener un solo dominio

    - Documentacion del error

        - https://forum.ovh.es/showthread.php/7576-problemas-con-ispconfig-3

        - https://www.howtoforge.com/community/threads/ispconfig3-multiple-sites-domains-in-one-server.32443/


    - Solucion: Configurar la opcion NameVirtualHost para que haya virtualizacion los

        En ubuntu 20.04LTS

            Validarse en el server y navegar por consola a: 
            
            $ /etc/apache2/sites-available

            $ sudo vim ispconfig.conf

                - agregar la linea al inicio si no existe o si esta comentada descomentarla

                    NameVirtualHost *:80

                - Automaticamente se agregara al resto de archivos necesarios

                - Reiniciar apache con privilegios para que se realicen los cambios

                    $ /etc/init.d/apache2 restart
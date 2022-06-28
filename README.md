

## REQUISITOS 4 EN LINEA (REQUISITOS)
Para la instalacion del juego debera tener instalado :

Composer : https://getcomposer.org/download/

Docker Desktop : https://docs.docker.com/desktop/windows/install/ç

DDEV : https://ddev.readthedocs.io/en/stable/ 

## PASOS A SEGUIR PARA LA INSTALACION 
Una vez intalado de manera correcta lo nombrado comenzamos :

1- Lo primero es clonar el repositorio en el directorio (con git hub).

2- Ahora tenemos que configurar DDEV :  Abrimos la consola, una vez hecho esto entramos al directorio creado anteriormente con este comando (la direccion del directorio cambiara en su caso) : 
                
     cd C:\Users\AMD Ryzen 5\OneDrive\Escritorio\cuatroenlinea
                                            
3- ingresamos :

     ddev config
     
Nos va a pedir el nombre que le queremos dar al proyecto, donde queremos guardarlo, y tipo de proyecto, ponemos laravel.

seguimos poniendo este comando : 

    ddev start

4- Tenemos que verificar el Composer.

Nos conectamos al servidor local con:

    ddev ssh

y actuaizamos Composer : 

    composer update

5- Creamos un archivo de ambiente y escribimos el sighiente comando : 

    ls -la cp .env.example .env echo "WWWGROUP=1000" >> .env echo "WWWUSER=1000" >> .env
    
6- Generamos una clave
    
    php artisan key:generate
    
7- Ahora podemos correr la aplicacion, salimos al servidor local y reinicamos el proyecto con los comandos : 
    
    exit
    
   y

    ddev restart
    
   
Una vez hecho eso, en la consola nos va a dar la direccion en la cual esta alojada nuestra pagina web, para entrar  agregamos /jugar/1 a la direccion y ya estariamos el juego.

8- Para cerrar la aplicacion solo tenemos que usar el comando 
    
    ddev poweroff

y para volver a jugar 
    
    ddev start

-----------------------------------



                                       
                                       



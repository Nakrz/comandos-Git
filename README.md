# **Taller Git**     

**[git config --get (Nombre del alias) ]**



1. Esta trabajando en un proyecto Git colaborativo con varias ramas y commits. Tu tarea es utilizar el comando git log con algunas opciones específicas para obtener un resumen gráfico de los últimos 5 commits en todas las ramas.
   - **git config --global alias.trabajo "log --graph --decorate --all -n 5"**
   
     

- **git config --global**: Este comando es utilizado para configurar opciones de git, la opcion --global indica que el cambio se aplicara a nivel global osea para todos los repositorios

- **alias.trabajo**: Establece un alias llamado trabajo en la configuracion de Git
- **--graph**: Este comando permite visualizar de manera grafica la estructura del historial  de commits, algo asi como si fuera una linea del tiempo.
- **--decorate**: Muestra las referencias (ramas o tags)  junto a los commits, por ejemplo  (HEAD -> main)
- **--all**: Esto muestra todas las ramas
- **-n 5**: Esto especifica o limita la salida de las ultimos 5 commits 



 

2. Esta trabajando en un proyecto Git colaborativo y necesitas obtener una visión gráfica y detallada del historial de commits. Tu tarea es utilizar el comando git log con opciones específicas para personalizar el formato y presentación de la salida. La salida debe tener las siguientes especificaciones:

   •Muestra una representación gráfica del historial de commits

   •Muestra el hash corto del commit en color rojo

   •Muestra las referencias (ramas o tags) en las que está involucrado el commit en color amarillo

   •Muestra el mensaje del commit.

   •Muestra la fecha relativa del commit en color verde.

   •Muestra el hash del commit como un identificador abreviado.

   •Muestra las fechas de los commits de forma relativa

   

   - **git log --graph --abbrev-commit --format=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr)%Creset' **

     

     - **git log**: este es un comando en git que se utiliza para ver el historial de commits de un repositorio.
     - **--graph**: Este comando permite visualizar de manera grafica la estructura del historial  de commits, algo asi como si fuera una linea del tiempo.
     - **--abbrev-commit**: Este comando muestra los hashes de commit abreviados para una lectura mas facil
     - **--format=format**: Esto define un formato personalizado de salida del log. La cadena entre comillas simples ' ' especifica como formatear la entrada de cada blog
     - **%Cred** Esto indica que el siguiente texto sera mostrado en rojo
     - **%Creset**: Esto restablece el color al valor normal
     - **C(yellow)**: Esto indica que el siguiente texto va a salir en amarillo
     - **%Cgreen**: Esto indica que el siguiente texto se mostrara en verde

     

​	

3. Tu tarea es utilizar el comando git config para crear un alias llamado last que represente el comando git log -1 HEAD.

- **git config --global alias.detalles "log  -1 HEAD"**



- **git config --global**: Este comando es utilizado para configurar opciones de git, la opcion --global indica que el cambio se aplicara a nivel global osea para todos los repositorios
- **alias.detalles**: Con este comando especificamos el nombre de alias que queremos crear.
- **"log -1 HEAD"**: Este comando es la cadena de comandos que el alias va a representar, asi que la proxima vez que escriba git detalles se ejecutara log -1 HEAD



4. Tu tarea es utilizar el comando git config para crear un alias que te permita abrir fácilmente la configuración global en tu editor de texto preferido. Ejecuta el comando para crear un alias llamado ec que cumpla con la especificación dada.

   

- **git config --global alias.ec "config --global e-"**



- **git config --global**: Este comando es utilizado para configurar opciones de git, la opcion --global indica que el cambio se aplicara a nivel global osea para todos los repositorios

- **alias.ec**: Con este comando especificamos el nombre de alias que queremos crear.

- **"config --global -e"**: Este es el comando que se quiere ejecutar cuando escribimos git ec, config --global -e abre el archivo de configuracion global de git en el editor de texto del sistema.

  

5. Imagina que estás trabajando en un proyecto Git colaborativo con múltiples colaboradores y ramas. Tu tarea es utilizar el comando git log con opciones específicas para personalizar la salida del historial de commits y resaltar información clave. 

   

   * **git log --graph --format=format:"%C(yellow)%h%Creset - %s (%C(blue)%an%Creset)" --decorate**



- **git log**: este es un comando en git que se utiliza para ver el historial de commits de un repositorio.
- **--graph**: Este comando permite visualizar de manera grafica la estructura del historial  de commits.
- **--format=format: "%C(yellow)%h%Creset - %s (%C(blue)%an%Creset)"**: Esto define un formato personalizado de salida del log, en este caso usamos %C(yellow) color amarillo para los hash y %C/blue) color azul para el nombre del autor
- **-%s**: Este comando sirve para mostrar el mensaje del commit
- **--decorate**: Muestra las referencias (ramas o tags)  junto a los commits.
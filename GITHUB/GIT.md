# COMANDOS
    Ir a programas/git y ejecutar git-bash
   
## CONFIGURACION INICIAL
    git config --global user.name "gonzaloH8" -- tiene que ser el mismo que el de GitHub
    git config --global user.name -- confirmar el nombre a usar

    git config --global user.email gonzalo.saa8@gmail -- tiene que ser el mismo que el de GitHub
    git config --global user.email -- confirmar el email a usar

    git config --global core.editor "code --wait" -- configura el editor de texto que vamos a usar

    git config --global -e -- nor permite ver el fichero donde se guardo nuestra configuracion

    git clone https://github.com/gonzaloH8/nombre_repositorio.git -- clonamos el archivo creado en GitHub y lo guardamos en local

    git branch -- nos indica en una pantalla nueva el usuario en el que estamos
    git branch -M Usuario -- permite cambiar el usuario de ejecucion
    git checkout -b Usuario -- permite cambiar el usuario de ejecucion
    git checkout Usuario -- nos permite cambiar de Usuario
    git merge Usuario_Personal -- desde el usuario main traemos los cambios hechos en nuestro usuario personal

    git status -- nos permite ver el estado de nuestros ficheros(Computador,Stage,Commit,Server)
        Computador: estado incial de un fichero. Aparece señalizado con el color rojo
        Stage: estado de envio de un fichero. Aparece sañalizado con el color verde
        Commit: estado de guardado de un fichero
        Server: estado de envio al server de un fichero
    git status -s -- version de listado de archivos mas limpio
        M - Modificacion. Si esta en rojo(esta en primera fase add) si esta en verde(necesita guardarse commit)
        ?? - Añadir. Si esta en rojo(esta en primera fase add) si esta en verde-A(necesita guardarse commit)

    git remote remove origin -- nos permite eliminar el repositorio

    git diff -- nos muestra visualmente el antes y despues del archivo con el que estamos trabajando. Pulsar q para salir de esta pantalla
    git diff --staged -- nos permite ver el historial de cambios del repositorio en fase staged
    git log --oneline -- nos permite ver el historial de cambios del repositorio en fase staged con hash y sus repectivos mensajes de guardado
    
## PROCESO DE SUBIDA DE ARCHIVOS
    Me situo en mi carpeta de repositorios /d/FPS/FP/LenguajedeMarcas/GitHub
    git init -- nos inicia un repositorio oculto .git en la carptea que estemos situados NUEVO
    git remote add origin https://github.com/gonzaloH8/Prueba.git - si ya tengo un repositorio creado, enlazo mi repositorio de GitHub con Git
    git clone https://github.com/gonzaloH8/Prueba.git
    echo "# Prueba" >> ARCHIVO.md -- guarda un texto en el archivo
    git add FICHERO.md -- añadimos los archivos creados en local
    git commit -m "first commit" -- guardamos los archivos en su lugar de creacion   
    git push -u origin Usuario -- sube los cambios hechos al repositorio de la nube(GitHub)
     
## PROCESO DE ELIMINACION DE ARCHIVOS
    rm fichero.md -- eliminacion de un fichero
    git add FICHERO.md -- añadimos los archivos creados en local
    git commit -m "first commit" -- guardamos los archivos en su lugar de creacion   
    git restore --staged fichero.md -- retrocede una posicion de estado el archivo seleccionado
    git restore fichero.md -- restaura un fichero en fase Staged a Computacion

## PROCESO DE CAMBIAR EL NOMBRE DE ARCHIVOS
     mv archivo1.md archivo -- cambia el nombre del archivo
     git mv archivo1.md archivo.md -- version corta de cambio de nombre. Nos permite saltar el paso de add
     git add archivo1.md archivo.md -- añadimos los archivos modificados tanto el de eliminacion como el de agregacion   
     git commit -m "first commit" -- guardamos los archivos en su lugar de creacion

# VARIABLES RESERVADAS
    .env -- permite guardar variables importantes que no queremos subir al repositorio
        password=123456789
        usuario:gonzaloH8
    .gitignore -- permite ignorar archivos y carpetas, que no sean subidas al repositorio, haciendo que no aparezcan al ejecutar git status
    

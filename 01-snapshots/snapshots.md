/---------- AGREGANDO A STAGING ----------/

git status                                                  muestra el estado de archivos con o sin seguimiento

git add [name_archivo]                                      agrega el archivo al staging area

git add .                                                   agrega todos los archivos del directorio actual, no debe usarse


/---------- CREANDO COMMITS ----------/

git commit -m "[description]"                               agregamos todos los cambios (git add) anteriores a nuestro commit

git commit -a -m "saltando el area de staging"              con el comando -a nos saltamos el area de staging


/---------- ELIMINANDO ARCHIVOS ----------/

git rm archivo2.txt                                         elimina el archivo y tambien lo elimina del area de staging


/---------- MOVIENDO ARCHIVOS ----------/

git mv archivo1.txt app.py                                  renombra el archivo original, es decir tiene el mismo contenido


/---------- VIENDO EL HISTORIAL ----------/

git log                                                     muestra un listado detallado de todos los commits

git log --oneline                                           muestra el listado pero de forma resumida

git log --oneline --reverse                                 muestra el listado de forma resumida y al revés


/---------- VER EL CONTENIDO DE COMMITS ----------/

git show [id]                                               muestra el detalle de un commit en especifico por el id

git show [id]:[archivo.test]                                muestra el contenido de un archivo en especifico de un determinado commit

git show HEAD~[number]:[archivo.test]                       muestra el contenido referenciando la cabecera y contando los commits hacia atrás

git ls-tree [id]                                            mostrar los archivos de un commit en especifico

git show [codigo_archivo]                                   muestra el contenido de un archivo en especifico

NOTA: Con el comando de SHOW podemos visualizar el contenido de:
- commits
- blob (archivos)
- tree (directorios)
- tags


/---------- QUITAR ARCHIVOS DE STAGING ----------/

git restore --staged [archivo.test]                         retira los archivos del staging area


/---------- IGNORANDO ARCHIVOS Y DIRECTORIOS ----------/

touch .gitignore                                            creamos un archivo donde en el podemos listar archivos y directorios donde git los ignorara automaticamente


/---------- IGNORANDO ARCHIVOS YA AGREGADOS ----------/

git rm --cached [archivo.test]                              ignora el seguimiento del archivo desde ese momento


/---------- VIENDO NUESTROS CAMBIOS ----------/

git diff                                                    visualizar hasta ahora los cambios en nuestro directorio de trabajo

git diff --cached                                           visualizar las diferencias que se encuentran dentro de nuestra area de staging


/---------- DIFFTOOL VISUAL ----------/

git config --global diff.tool vscode                                            configuracion global de difftool

git config --global difftool.vscode.cmd 'code --wait --diff $LOCAL $REMOTE'     agregamos las variables LOCAL y REMOTE a nuestra configuración

git config --global -e                                                          visualizamos las configuraciones realizadas

git difftool                                                                    compara los cambios que se encuentran en nuestro directorio de trabajo

git difftool --stagen                                                           visualiza los cambios del area de staging


/---------- DESCARTANDO LOS CAMBIOS ----------/

git restore --staged [archivo.test]                                             quita el archivo de nuestra area de staging y lo coloca en nuestra area de trabajo

git restore [archivo.test]                                                      los cambios en nuestra area de trabajo fueron descartados

git restore --staged .                                                          restaura todos los archivos de nuestra area de staging y los coloca en nuestra area de trabajo

git restore .                                                                   quita todos los cambios de nuestra area de trabajo

git clean -f                                                                    limpiar nuestra area de trabajo

git clean -f [archivo.test]                                                     limpiar un archivo en especifico


/---------- RESTAURANDO ARCHIVOS A VERSIONES ----------/

git restore --source=HEAD~1 [archivo.test]                                      restaura un archivo a 1 version anterior

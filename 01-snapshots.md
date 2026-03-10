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







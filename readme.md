- Sitúese en la carpeta en la que desee crear el repositorio.

```	
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~
	$ cd Desktop/awakelab/
```

- Cree una carpeta, y dentro de la misma un repositorio, ambos con el nombre
fullstackjava

```
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab (master)
	$ mkdir fullstackjava
```
```
    eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab (master)
	$ cd fullstackjava/
```
```
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ git init
	Initialized empty Git repository in C:/Users/eldelchivo/Desktop/awakelab/fullstackjava/.git/
```
- Genere una consulta que permite verificar el estado del repositorio
```
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ git status
	On branch master

	No commits yet

	nothing to commit (create/copy files and use "git add" to track)
```
- Cree un documento de texto de nombre contenidos.txt, que posea el siguiente
contenido:
Módulo 1: Programación en Java
Módulo 2: Lenguaje de Consultas a una Base de Datos
Módulo 3: Fundamentos de Desarrollo Web

```	
	// Creacion de archivo
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ touch contenido.txt
```
```
	// Agregando contenido
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ echo "Módulo 1: Programación en Java">> contenido.txt
```
```
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ echo "Módulo 2: Lenguaje de Consultas a una Base de Datos">> contenido.txt
```
```
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ echo "Módulo 3: Fundamentos de Desarrollo Web">> contenido.txt
```
	

- Validar que el contenido ingresado esté efectivamente cargado. Verifique
además el tamaño del archivo y sus permisos de acceso.

	// Verificar contenido
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ cat contenido.txt
	Módulo 1: Programación en Java
	Módulo 2: Lenguaje de Consultas a una Base de Datos
	Módulo 3: Fundamentos de Desarrollo Web

	
	// verificar estado
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ git status
	On branch master

	No commits yet

	Untracked files:
  	(use "git add <file>..." to include in what will be committed)
          	contenido.txt

	othing added to commit but untracked files present (use "git add" to track)

	// verifica tamaño del archivo y sus permisos de acceso
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ ls -l
	total 1
	-rw-r--r-- 1 eldelchivo 197121 127 abr.  9 21:00 contenido.txt

- Añada el archivo al repositorio

	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ git add contenido.txt
	warning: in the working copy of 'contenido.txt', LF will be replaced by CRLF the next time Git touches it

- Aplique los cambios realizados sobre el repositorio, usando como mensaje
“Primera versión del temario subida a repositorio”

	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ git commit contenido.txt -m "Primera versión del temario subida a repositorio"
	warning: in the working copy of 'contenido.txt', LF will be replaced by CRLF the next time Git touches it
	[master (root-commit) 3dd68fb] Primera versión del temario subida a repositorio
 	1 file changed, 3 insertions(+)
 	create mode 100644 contenido.txt	


- Añada una nueva línea al final del archivo, con el contenido “Módulo 4:
Desarrollo de aplicaciones web dinámicas con Java”.
	
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ echo "Módulo 4:Desarrollo de aplicaciones web dinámicas con Java">> contenido.txt

- Verificar qué cambios existen en el repositorio que deban ser almacenados
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ git status
	On branch master
	Changes not staged for commit:
  	(use "git add <file>..." to update what will be committed)
  	(use "git restore <file>..." to discard changes in working directory)
        	modified:   contenido.txt

	no changes added to commit (use "git add" and/or "git commit -a")


- Aplicar nuevamente los cambios en el repositorio, esta vez con el mensaje
“Versión actualizada del contenido”

	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
```
	$ git add contenido.txt
	warning: in the working copy of 'contenido.txt', LF will be replaced by CRLF the next time Git touches it

	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
```
```
	$ git commit contenido.txt -m "Versión actualizada del contenido"
	warning: in the working copy of 'contenido.txt', LF will be replaced by CRLF the next time Git touches it
	[master 95a2eed] Versión actualizada del contenido
 	1 file changed, 1 insertion(+)
```
- Ver el registro de cambios creados sobre el repositorio
```
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ git log
```
```
	commit 95a2eed54c954372c6c14b5a4f88a03ca6a74e29 (HEAD -> master)
	Author: boanguibe <borisandres.guinez@gmail.com>
	Date:   Sun Apr 9 21:15:53 2023 -0400

    	Versión actualizada del contenido
```
```
	commit 3dd68fba5a20f06890d40216ddbe023846713d23
	Author: boanguibe <borisandres.guinez@gmail.com>
	Date:   Sun Apr 9 21:08:50 2023 -0400

    	Primera versión del temario subida a repositorio
```
- Finalmente, validar el estado del repositorio
```
	eldelchivo@DESKTOP-7OTNRKQ MINGW64 ~/Desktop/awakelab/fullstackjava (master)
	$ git status
	On branch master
	nothing to commit, working tree clean
```
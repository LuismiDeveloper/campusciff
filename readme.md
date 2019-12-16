# Ejercicios GitHub

## Ejercicio Básico

1. Creación del repositorio campusciff

	![img1](http://imgfz.com/i/vOiHbA3.png)


2. Clonación del repositorio a local

	![img2](http://imgfz.com/i/ZBlDOwK.png)


3. Creación de README.md y commit con el mensaje "Commit inicial"

	![img](https://imgur.com/UqyjgNx.png)


4. Subir los cambios al repositorio remoto

		git push
        
	(Nos pedirá nuestras credenciales de GitHub).
    
	![img](https://imgur.com/5JSjvR9.png)
    ![img](https://imgur.com/mRcWpQF.png)
    
5. Creación de privado.txt y la carpeta privada

		touch privado.txt
        mkdir privada

	![img](https://imgur.com/ACLjG5Y.png)
    
6. Creación de .gitignore para que el archivo y la carpeta sean ignorados

	![img](https://imgur.com/h63Ft79.png)
    
7. Añadir el fichero 1.txt y hacer un tag v0.1

		touch 1.txt
        git add 1.txt
        git commit -m "subida 1.txt"
        git tag v0.1 -m "Primera versión"
		
        
	No puedo mostrar la captura de la ejecución de dichos comandos, pero demuestro que lo he he hecho con git log:
    
    ![img](https://imgur.com/LVFQQxV.png)
    
8. Subir los cambios al repositorio remoto

		git push
        git push origin master --tags //Para subir el tag creado
   	
    Comprobamos que se ha subido correctamente:
        
	![img](https://imgur.com/Qnj7uA3.png)
    ![img](https://imgur.com/uAVR7cs.png)

9. Crea una tabla con la información de varios compañeros de tu clase

Nombre | Enlace
--|--
Miriam | [Perfil de GitHub](github.com/MIRIAM-GIT)
David | [Perfil de GitHub](github.com/davidfuentes2755)

## Ejercicio avanzado

1. Crear una rama v0.2 y posicionar la carpeta de trabajo en esta rama

		git branch v0.2 //Para crear la rama
        git checkout v0.2 //Para posicionarnos en la rama
        
	![img](https://imgur.com/RsghD7V.png)

2. Añadir fichero 2.txt a la rama v0.2
		
	Estando posicionados en la rama previamente:
    
		git add 2.txt
        git commit -m "Añadido 2.txt a la rama v0.2"

	![img](https://imgur.com/qW2S9uL.png)

3. Subir los cambios al repositorio remoto

	Para subir la rama usaremos:
    	
        git push origin v0.2
        
	![img](https://imgur.com/pGzEWFo.png)
    
    Comprobamos que se ha subido:
    
    ![img](https://imgur.com/RiRYQU5.png)
    
4. Hacer merge de la rama v0.2 en la rama master

	Nos posicionamos en la rama master con:
    	
        git checkout master
        
	A continuación hacemos el merge con:
    
    	git merge v0.2
        
	![img](https://imgur.com/iA4lssO.png)
    
5. Merge con conflicto

	5.1. En la rama master poner Hola en el fichero 1.txt y hacer commit.

	![img](https://imgur.com/UvS8hfr.png)
    
    5.2. Posicionarse en la rama v0.2 y poner Adios en 2.txt y hacer commit.

		git checkout v0.2
        nano 1.txt
    ![img](https://imgur.com/rJX1k7C.png)
    ![img](https://imgur.com/GRk8nwW.png)
    
    5.3. Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2
	
    	git checkout master
        git merge v0.2
	Podemos observar que hay conflicto con el fichero 1.txt:
    
	![img](https://imgur.com/ndUQMpV.png)
    
    5.4. Listar ramas con merge y sin merge

		git branch
	![img](https://imgur.com/cLY8fg0.png)
    
    5.5. Arreglar el conflicto y hacer commit
    
    Si abrimos el fichero con nano observamos que tiene tanto la versión de master como la de v0.2:
    
	![img](https://imgur.com/AYgxTQZ.png)
    
    Para arreglar el conflicto lo único que tenemos que hacer es dejar el fichero con el contenido de la versión que deseemos, en mi caso voy a dejar la versión de master (Hola).
	
    ![img](https://imgur.com/60hMjzs.png)
    
    Hacemos el commit y listo.
    
    ![img](https://imgur.com/AARMFLH.png)
    
6. Borrar rama v0.2 y crear tag v0.2

		git branch -d v0.2 //Para borrar la rama
        git tag v0.2 -m "Segunda versión" //Para crear el tag
        
	![img](https://imgur.com/8Or2N8B.png)
    
7. Listar los distintos commits con sus ramas y sus tags
		
        git log --oneline
	![img](https://imgur.com/uze443V.png)


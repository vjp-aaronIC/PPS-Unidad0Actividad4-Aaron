# PPS-Unidad0Actividad4-Aaron

En esta actividad voy a guardar fichero en **.gitignore** para que no se suban al repositorio (que no se rastreen).
Podemos ignorar ficheros por su extensión, por ejemplo **txt**. También podemos directamente ignorar directorios completos.

También vamos a publicar en local una pequeña web mediante un *servidor web* alojado en local bajo el puerto **8080**.

## Ignorar ficheros (.gitignore)

1. El primer paso para ignorar ficheros es crear un fichero que se llama **.gitignore** dentro de la carpeta local de nuestro proyecto.
Podemos usar el comando **touch .gitignore** para su creación. Si mostramos el directorio *local* con **ls -la** debe contener el fichero **.gitignore** de la siguiente manera.

```bash 
cd ruta_del_proyecto
touch .gitignore
nano .gitignore
 
```

2. El siguiente paso para ignorar los ficheros o directorios, es agregar dentro del fichero que hemos *creado anteriormente* las reglas que queremos que cumplan los ficheros que no queremos subir.
En mi caso por ejemplo, si no quiero que se suban fichero con extensión *.txt* tengo que agregar _*.txt_.

![](images/ignore_txt.png)

## Crear web local

1. Crear un fichero html
He creado un fichero **index.html** que contiene *"Hola mundo Aarón"*.

```bash
echo "<H1>Hola mundo Aarón</H1>" > index.html

```
Una vez creado el fichero, he comprobado el estado de git con *git status* y he agregado el **index.html** para subirlo a un commit y luego a la rama **main**.

```bash
git status
git add index.html
git commit -m "creacion del index"
git push origin main

```
![](images/creacion_index.png)

2. Arrancar un servidor web
El servidor que arrancamos en local coge por defecto el fichero **index.html** que haya en la ruta donde se arranque el servidor **PHP**.

```bash
php -S 0:8080

```

Si accedemos desde el navegador al puerto donde hemos levantado el servidor veremos el contenido del **HTML interpretado**.

![](images/php_index.png)


## Comparar ficheros modificados



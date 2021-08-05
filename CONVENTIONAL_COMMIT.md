## Pero, ¿Qué rayos es un commit convencional?

Es una especificación que nos permite generar commits coherentes y significativos los cuales pueden ser entendidos por.

* 💻 Maquinas
* 👨🏻‍💻Humanos

> **🔖 Nota:** es necesario contar con la versión de node 12.*.* lts o 14.*.* lts.


## ¿Por qué usarlos?

* Permiten generar CHANGELOG automáticamente
* Facilita la creación de versiones de manera semántica
* Comunicación fluida sobre la naturaleza de los cambios a los miembros del equipo
* Facilita un historial de cambios más estructurado.

## Como se construye un commit convencional

Al igual que todo commit estos son conformados por un header, body y footer

![Commit](https://raw.githubusercontent.com/OrcaPracticas/happy-shell/master/testing/Commit.png)


### 📝 Header:

Este contiene un type el cual indicara el tipo de commit que estamos por crear, también puede contar con un scope el cual es opcional este puede ser el nombre de algún archivo o un tag o nombre, seguido se coloca una descripción corta con la cual se indica de manera muy breve el cambio realizado.

### 📝 Body:

en este caso se tiene que dejar un salto de línea antes para así después introducir una descripción larga, el body también puede llevar una opcion nombrada(esta tiene que estar seguida de un salto de line en blanco) **BREAKING CHANGE** la cual es seguida de una descripción donde se detalla por que se genera el breaking change


### Footer: 

Al igual que el body se deja un espacio en blanco para este caso se listan los tickets o issues con los que tiene relación el commit.


## Pero, ¿Qué tipos existen?

![tipos](https://raw.githubusercontent.com/OrcaPracticas/happy-shell/master/testing/Captura%20de%20Pantalla%202020-12-01%20a%20la(s)%2011.59.07.png)

los tipos mostrados son los que estaremos utilizando para identificar los commits que generemos dentro de nuestros proyectos.

## ¿Como se implementa esta magia negra?

Para poder usar **conventional commit** es necesario tomar en cuenta los siguientes puntos.

1. Teneos que contar con Node 14lts o 12lts
2. El repositorio con el que estaremos trabajando tiene que contar con el soporte para conventional-commits (esto es si utilizamos un alias de git)
3. Tenemos que instalar de manera global la siguiente dependencia

```
npm i -g commitizen o yarn global add commitizen
```

4. Para agregar un alias en git utilizaremos el comando siguiente 

```
git config —global alias.cz git-cz
```

De esta forma estamos listos para utilizar conventional-commits.

> **🔖 Nota:** si surgiera un error al momento de tratar de utilizar el alias de git se recomienda utilizar el siguiente comando.

```
commitizen init cz-conventional-changelog --save-dev --save-exact --force
```


Para mayor información sobre commits convencionales puedes consultar la siguiente pagina
https://www.conventionalcommits.org/en/v1.0.0/
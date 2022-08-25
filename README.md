# Git Course

¿Que es git?

Git es un software de control de versiones distribuido y descentralizado que permite a un equipo de desarrolladores trabajar sobre el mismo código.

Se denomina "distribuido" porque cada miembro del equipo dispone de una copia completa del código.

## Instalación

Linux y Mac Os

Generalmente viene pre-instalado con el sistema operativo, en caso que no este en el sistema ejecutar en la terminal:

```
Sudo (instalador de paquetes del Os) Install Git
```

Windows

Descargar el instalador portable de la pagina oficial de Git:

```
https://git-scm.com/downloads
```

## Configuración Inicial

Verificar la version de Git

```
git --version
```

Configurar el nombre del usuario

```
git config --global user.name "Nombre User"
```

Configurar el correo del usuario

```
git config --global user.email user@mail.com
```

Ver la configuración de Git

```
git config --list
```

ver todas las opciones de la configuración en la terminal

```
git config -h
```

ver todas las opciones de la configuración en el navegador

```
git help config
```

## Git en Acción

# Inicializar Git en local

```
git init
```

Agregar los cambios de un archivo al staged

```
git add archivo/directorio
```

Agregar todos los cambios de todos los archivos al staged

```
git add .
```

Agregar un comentario con los cambios realizados

```
git commit
```

Agregar el origen remoto de tu repositorio de GitHub

```
git remote add origin https://github.com/usuario/repositorio.git
```

Enviar o subir los cambios en Git para las ramas

```
git push -u origin Main/feature
```

Para las subsecuentes actualizaciones, sino cambias de rama

```
git push
```

Para descargar los cambios del repositorio remoto al local

```
git pull
```

## Cambiar de master a main

```
git branch -M main
```

## Ignorar Archivos

En el archivo .gitignore incluimos todo lo que NO queramos incluir en nuestro repositorio.
Lo podemos crear manualmente o con gitignore.io.

## Clonar repositorios

```
git clone https://github.com/usuario/repositorio.git
```

## Ramas

Crear rama

```
git branch nombre-rama
```

Cambiar de rama

```
git checkout nombre-rama
```

Crear una rama y cambiarte a ella

```
git checkout -b rama
```

Eliminar rama

```
git branch -d nombre-rama
```

Eliminar rama (forzado)

```
git branch -D nombre-rama
```

Listar todas las ramas del repositorio

```
git branch
```

Lista ramas no fusionadas a la rama actual

```
git branch --no-merged
```

Lista ramas fusionadas a la rama actual

```
git branch --merged
```

Rebasar ramas

```
git checkout rama-secundaria
git rebase rama-principal
```

## Fusiones

Une dos ramas. Para hacer una fusión necesitamos:

Situarnos en la rama que se quedará con el contenido fusionado.
Fusionar.
Cuando se fusionan ramas se pueden dar 2 resultados diferentes:

- Fast-Forward: La fusión se hace automática, no hay conflictos por resolver.
- Manual Merge: La fusión hay que hacerla manual, para resolver conflictos de duplicación de contenido.

Nos cambiamos a la rama principal que quedará de la fusión

```
git checkout rama-principal
```

Ejecutamos el comando merge con la rama secundaria a fusionar

```
git merge rama-secundaria
```

## Cambios

Puedes agregar modificaciones al último cambio

Sin editar el mensaje del último commit

```
git commit --amend --no-edit
```

Editando el mensaje del último commit

```
git commit --amend -m "nuevo mensaje para el último commit"
```

Eliminar el último commit

```
git reset --hard HEAD~1
```

Podemos desplazarnos en el historial del repositorio hacia atrás o adelante en cambios o ramas , sin afectar el repositorio como tal.

Cambiar a un commit en particular

```
git checkout id-commit
```

## Registro del historial

git log nos permite conocer todo el historial de un proyecto, con la información de la fecha, el autor y id de cada cambio.

```
git log
```

Diferencias entre el Working Directory y el Staging Area

```
git diff
```

Muestra el listado de archivos nuevos (untracked), borrados o editados

```
git status
```

Borra HEAD

```
git reset --soft
```

Borra HEAD y Staging

```
git reset --mixed
```

Borra todo: HEAD, Staging y Working Directory

```
git reset --hard
```

Deshace todos los cambios después del commit indicado, preservando los cambios localmente

```
git reset id-commit
```

Desecha todo el historial y regresa al commit especificado

```
git reset --hard id-commit
```

## Resetear un repositorio

Si en algún momento tienes la necesidad de resetear el historial de cambios de un repositorio
para que quede como si lo acabarás de crear ejecuta esta serie de comandos:

```
cd carpeta-repositorio
mv .git/config ~/saved_git_config
rm -rf .git
git init
git branch -M main
git add .
git commit -m "Commit inicial"
mv ~/saved_git_config .git/config
git push --force origin main
```

## Remotos

Muestra los orígenes remotos del repositorio

```
git remote
```

Muestra los orígenes remotos con detalle

```
git remote -v
```

Renombrar un orígen remoto

```
git remote rename nombre-viejo nombre-nuevo
```

Eliminar un orígen remoto

```
git remote remove nombre-orígen
```

Descargar una rama remota a local diferente a la principal

```
git checkout --track -b rama-remota origin/rama-remota
```

## Etiquetas

Listar etiquetas

```
git tag
```

Mostrar información de una etiqueta

```
git show numero-versión
```

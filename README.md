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
git config --global user.name "Jonathan MirCha"
```

Configurar el correo del usuario

```
git config --global user.email jonmircha@gmail.com
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

para descargar los cambios del repositorio remoto al local

```
git pull
```

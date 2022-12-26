---
title: "GIT"
description: 'Short cuts and guide'
type: application
created: 04-03-2022
tags:
- git
---
	
	# GIT

## COMMANDS

* `git branch` - List all local branches.
* `git branch -a` - List remote and local branches.
* `git checkout -b branch_name` - Create a local branch and switch to it.
* `git checkout branch_name` - Switch to an existing branch.
* `git push origin branch_name`\- Push branch to remote.
* `git branch -m new_name` - Rename current branch.
* `git branch -d branch_name` - Delete a local branch.
* `git push origin :branch_name` - Delete a remote branch.
* `git config --global user.name "Antonio Robles"`
* `git config --global user.mail antjrobles@gmail.com`
* `git config --global core.editor "code --wait"`
* `git config --global -e`
* `git config --global core.autocrlf input (SI ESTOY EN MAC) true (SI ESTOY EN WINDOWS)`
* `git diff`
* `git diff --staged`
* `git log`
* `git log --all --graph` - ver el historial de commits locales
* `git log --oneline` - display logs in one line
* `git checkout`
* `git commit -am "Mensaje" (añade todos los archivos y los cambios)` - Salta el paso de git add .
* `git reset --hard (commit hash)` - Revertir a un commit especifico.
* `git reset --hard origin/master` - (revertir a la version que está en Github en ese momento).
* `git checkout -b (nombre del branch)` - Crear un branch nuevo
* `git checkout master (cambiar a master)`
* `git merge (nombre del branch)` - Unir un branch con master.
* `fork` (crear una copia de un repositorio).
* `git reset --hard` (Para eliminar este mensaje de error: Los cambios locales de los siguientes archivos serán sobrescritos al fusionar:). Seguidamente `git pull` para actualizar el repositorio local con los cambios del remoto.

## NEW COMMANDS

* `git remote remove origin `\- Disconnect a local repository from the remote
* `rm -rf path/to/local_repo/.git` - Also disconnect form remote
* `git reflog` - shows you a list of all the things you've done. It then allows you to use Git's magical time-traveling skills to go back to any point in the past

# Create a new repository on the command line

```
touch README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/Antjrobles/repository-name.git
git push -u origin main
 
# Push an existing repository from the command line
 
git remote add origin https://github.com/Antjrobles/repository-name.git
git push -u origin main (If we get:  ! [rejected] main -> main (non-fast-forward) - Then type this: git push -u origin main --force )
```

- example: 
``` bash 
sudo git clone https://antjrobles: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@github.com/antjrobles/Portfolio.git` - Añadir/crear un repositorio.
```

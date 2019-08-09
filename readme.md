# Git

## Config inicial

Cambia la configuración global del usuario de git, para que queden registrados sus datos en los commits.
```
git config --global user.email "tu@email.com"
git config --global user.name "Tu Nombre"
```

```
git init
git status: muestra el estado de los archivos.
git show: muestra todos los cambios históricos hechos, junto con las líneas que hayan cambiado.
git log: muestra todos los commits realizados junto con su mensaje.
```

Un archivo recién creado se encuentra sin rastrear o `untracked`

Stage: espacio en memoria ram donde se van guardando todos los cambios que realizamos luego de ejecutar `git add`

Una vez en el stage, un archivo queda esperando que lo agregues al repositorio con `git commit` o lo quites del stage con `git rm`

## Ramas o Branches
Ramas comunes o estándar: Master(donde vivirá la base del proyecto), experimental(rama para desarrollo de nuevas funcionalidades), hotfix(rama para corrección de bugs).

Se cambia entre ramas utilizando el comando `git checkout nombreRama`.
Se pueden pasar los cambios de una rama a otra utilizando `git merge`.

## Comandos

git diff hash1 hash2: imprime la diferencia de dos commits.





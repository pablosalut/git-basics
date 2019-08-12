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

**git branch nombre**: crea una nueva rama

**git checkout nombre**: cambiar a otra rama

La **cabecera o HEAD** representan la rama y el commit de esa rama donde estamos trabajando. Por defecto, esta cabecera aparecerá en el último commit de nuestra rama principal. Pero podemos cambiarlo al crear una rama (git branch rama, git checkout -b rama) o movernos en el tiempo a cualquier otro commit de cualquier otra rama.


## Comandos

**git diff hash1 hash2**: imprime la diferencia de dos commits. 

**git diff**: imprime la diferencia entre lo que tenemos en stage y lo que no guardamos todavía. (Es el equivalente a ir a la seccion de git de visual studio code y hacer click en alguno de los archivos que cambió)

**git reset hash --hard**: vuelve todo al commit indicado.Borra todos los commits después del elegido.

**git reset hash --soft**: vuelve al commit indicado manteniendo los archivos que tengamos en stage (para lo que hayamos hecho git add).

**git checkout hash nombreArchivo**: volvemos al commit indicado pero no se guardan los cambios hasta que no se commitea nuevamente los cambios.(El nombre del archivo es opcional, si no se escribe trae todos los cambios de ese commit.)

## Repositorio Remoto

**git clone url**: trae una copia del repositorio remoto en el directorio de trabajo y crea la base de datos de todo el histórico de git en el repositorio local.

**git push**: envío el head de todos mis commits al repositorio remoto.

**git fetch**: trae todo el historial de cambio al repositorio local pero no cambia el directorio de trabajo. Se debería hacer **git merge** para traer los cambios al directorio de trabajo, pero hacer solo **git pull** resume los dos comandos.

**git commit -am "Mensaje"**: atajo para realizar git add y git commit en un solo comando.

## Fusion de dos ramas con contenido distinto en una sola rama final

Teniendo cambios en dos ramas distintas con cambios, una vez agregados al stage y hechos los commits.

Estando en la rama que yo quiero que se conserven los cambios de las dos ramas (por ejemplo master) debo realizar: 

**git merge rama1**: Se debe colocar un mensaje de por que se realizó el merge.

La "rama1" puede borrarse despues de aplicar sus cambios a master, o conservarse para seguir siendo utilizada posteriormente.

### Solución de conflictos.

Cuando en las dos ramas se modifican las mismas lineas, se producirá un conflicto al intentar realizar el merge.
Lo único que debemos hacer es ir a ese archivo, a esa linea y borrar el código que queremos que se elimine y dejar lo que queremos que se mantenga.
(Visual studio añade botones para aceptar los cambios entrantes o dejar los originales)

Luego de resolver los conflictos se debe hacer add y commit de los cambios.


 










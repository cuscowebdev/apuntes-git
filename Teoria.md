# Git desde cero
`git commit -m ""`

`git diff`: Compara lo que tenemos en el directorio del trabajo con lo que esta en el area de preparacion

Para hacer un commit desde mi editor podemos usar solo `git commit` y automaticamente se abrira nuestro editor con el que configuramos nuestro git.

## Configurando Git por primera vez
```terminal
git config --global user.name "jdpoccorie"
git config --global user.email juandiego.poccori@gmail.com
git config --global core.editor nano
git config --list
```

## .gitignore
Patrones de archivos que git ignorará

### Saltar el area de preparación
`git commit -a -m` para saltar el area de preparación, tener en cuenta que solo funciona para archivos que ya estamos siguiendo.

### git rm
`git rm` Elimina archivos rastreados del repositorio y de nuestro directorio de trabajo de manera que no aparezcan la próxima vez como archivos no rastreados.

si nosotros eliminamos el archivo, haciendo anticlick y mandar a la papelera como una simple eliminacion y ponemos `git status` en consola nos aparecera un mensaje que diga deleted y que si vamos a querer continuar con eso usemos `git add/rm ` o que si queremos descartar esa eliminacion del archivo tenemos que usar `git checkout -- nombre-archivo` y todo regresa a la normalidad.

## Renombrar archivos
`git mv` Renombrar archivos `git mv file_from file_to`
su equivalente seria:
1. git rm file_from
2. git add file_to

## git log
Muestra el historial de confirmaciones

Entre las opciones del comando pordemos encontrar:
* `--oneline` nos muestra el historial abreviado
* `--graph` añade un pequeño ASCII mostrando el historial de ramificaciones y uniones. Podemos conbinarlo

Para ver los ultimos dos log
* `git log -2` Para ver los dos ultimos commit
* `git log -3` Para ver los tres ultimos commit
* `git log --pretty=format:"%h - %an, %ar : %s"` Nos resultará algo así
```
8162bfe - JDiegoP, 9 minutes ago : agregando la parte para configurar nuestro git de manera global
df533c9 - JDiegoP, 17 minutes ago : Agregando los equivalentes para git mv
a2bb140 - JDiegoP, 20 minutes ago : Renombrando por el camino largo
a7dab93 - JDiegoP, 23 minutes ago : Se coloco en may<C3><BA>scula el archivo teoria.md a Teoria.md
a51237b - JDiegoP, 40 minutes ago : Eliminando el 01.mp4 y ademas aumente info a la teoria
eed3109 - JDiegoP, 47 minutes ago : archivos para que lo podamos eliminar
```
### ¿Cuales son los commit del dia de ayer?
* `git log --after="YYYY-MM-dd"` para ver los commit despues de la fecha qe le demos
* `git log --after="YYYY-MM-dd 00:00:00"` para ver los commit despues de la fecha qe le demos ademas de la hora claro.
* `git log --before="YYYY-MM-dd"` para ver los commit antes de la fecha qe le demos.
* `git log --after="YYYY-MM-dd" --before="YYYY-MM-dd"` para ver los commit antes de la fecha qe le demos.
# Git desde cero
`git commit -m ""`

`git diff`: Compara lo que tenemos en el directorio del trabajo con lo que esta en el area de preparacion

Para hacer un commit desde mi editor podemos usar solo `git commit` y automaticamente se abrira nuestro editor con el que configuramos nuestro git.

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

# **Ingeniería del Software**
## 1. Introducción a Git, Markdown y Eclipse


Antonio Manuel Durán Rosal


**Asignatura "Ingeniería del Software"**



*2º Curso Grado en Ingeniería Informática*



*Escuela Politécnica Superior*



*(Universidad de Córdoba)*



*aduran@uco.es*


**18 de septiembre de 2018**

# Contenidos |

1.Git.

	1.1. Introducción.

	1.2 Instalación y configuración.

	1.3. Uso Básico.

	1.4. Ramas.

	1.5. Github.

2.Markdown.

	2.1. Introducción.

	2.2. Código.

3.Eclipse.

	3.1. Introducción.
	3.2. Instalación.

4.Recursos.

# Evaluación.
* Las entregas en moodle se realizarán por medio del representate o líder de cada grupo.
* Se debe entregar en moodle la dirección del repositorio de Github.
* Se evaluará la realización de un pequeño tutorial de Github con los contenidos aprendidos durante las dos primeras sesiones prácticas. El lenguaje de formateado será *Markdown*.

# Motivación
* Código efímero.
* Necesidad de mantener todas las versiones del código fuente.
* Problemas en organizaciones para mantener el código actualizado.
* Coherencia de versiones.
* Conocimiento del cambio que ha provocado que el sistema no funcione.
* Fallos en el disco duro que suponen riesgo de información desactualizada.
* Satisfacer el compromiso de entrega.

# Git y GitHub
![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSa-c1NtMrCDPse9KTv8qfJil6PYbcmlCXargG42OIgUPF6qlV25Q) : sistema para el control distribuido de versiones de código. Fundamentalmente permite:
* Dar seguimiento a los cambios realizados sobre un archivo.
* Almacenar una copia de los cambios.


![](https://studyguide.itu.dk/~/media/studyguide/student-life/facilities-at-itu/it-facilities/github/github_logo.png?h=248&w=573&la=en) : sitio web dónde podemos subir una copia de nuestro repositorio *Git*.

# Ventajas
## Git
* Habilidad de deshacer cambios.
* Historial y documentación de cambios.
* Múltiples versiones de código.
* Habilidad de resolver conflictos entre versiones de distintos programadores.
* Copias independientes.
### GitHub
* Documentación de requerimientos.
* Ver el avance del desarrollo.

# Instalación
* Para instalar Git: *https://git-scm.com*
* En el curso se utilizará *Git* a través de líneas de comandos.
* Para *eclipse* existen *plugins* integrados: *https://www.eclipse.org/egit*

# Configuración básica
Nombre del administrador:

`git config --global user.name "Antonio M. Durán Rosal"`

Correo electrónico:

`git config --global user.email aduran@uco.es`

Editor de texto:

`git config --global core.editor "gedit"`

Color de la interfaz:

`git config --global color.ui true`

Listado de la configuración:

`git config --list`

# Los tres estados de *Git*
![](https://i.stack.imgur.com/zLTpo.png)

# Comandos básicos I

Iniciar repositorio en un directorio:

`git init`

Agregar cambios al area de *staging*:

`git add`

Validar cambios en el repositorio:

`git commit -m "Mensaje"`

Hacer los dos pasos anteriores en uno:

`git commit -am "Mensaje"`

Historial de *commits*:

`git log`
# Comandos básicos II

Ayuda del listado anterior:

`git help log`

Listas los 5 *commits* más recientes:

`git log -n 5`

Listar los *commits* desde una fecha:

`git log --since=2018-09-18`

Listar los *commits* por autor:

`git log --author="Antonio"`

Ver cambios en el directorio:

`git status`

# Comandos básicos III

Ver diferencia entre ficheros en el directorio y el repositorio de git:

`git diff`

Ver diferencia entre ficheros en el *staging* y el repositorio:

`git diff --staged`

Eliminar archivos:

`git log --since=2018-09-18`


`git log --author="Antonio"`

Mover o renombrar archivos:

`git mv antiguo nuevo`


`git commit -m "Mensaje

# Comandos básicos III

Ver diferencia entre ficheros en el directorio y el repositorio de git:

`git diff`

Ver diferencia entre ficheros en el *staging* y el repositorio:

`git diff --staged`

Eliminar archivos:

`git log --since=2018-09-18`


`git log --author="Antonio"`

Mover o renombrar archivos:

`git mv antiguo nuevo`


`git commit -m "Mensaje

# Comandos básicos III

Ver diferencia entre ficheros en el directorio y el repositorio de git:

`git diff`

Ver diferencia entre ficheros en el *staging* y el repositorio:

`git diff --staged`

Eliminar archivos:

`git log --since=2018-09-18`


`git log --author="Antonio"`

Mover o renombrar archivos:

`git mv antiguo nuevo`


`git commit -m "Mensaje`

# Comandos básicos IV

Deshacer cambios con git:

`git checkout --nombre_fichero`

Retirar archivos del *staging*:

`git reset HEAD nombre_fichero`

Completar último commit:

`git commit --amend -m "Mensaje"`

Recuperar versión de un fichero de *commit* antiguo:

`git checkout <id_commit> -- nombre_archivo`

Revertir un *commit*:

`git revert <id_commit>`

# Comandos básicos V

Deshacer multiples cambios en repositorio:

`git reset --soft <id_commit>`


`git reset --mixed <id_commit>`


`git reset --hard <id_commit>`

Listar archivos que git no controla:

`git clean -n`

Eliminar arvhicos que git no controla:

`git clean -f`

Ignorar archivos en el repositorio: .gitignore

# Comandos básicos VI

Listar el contenido del repositorio de git:

`git ls-tree master`


`git ls-tree master^^^`


`git rls-tree master~3`

Log en una línea:

`git log --oneline`

Log con los tres últimos commit en una línea:

`git log --oneline -3`

Para más opciones consultar documentación de git.

# Comandos básicos VII

Examinar el contenido de un *commit*:

`git show <id>`

Comparar un *commit* con el actual:

`git diff <id> nombre_archivo`

Comparar dos *commits*:

`git diff id..id nombre_archivo`

# Ramas o Branches

Es la forma para separar la línea actual de desarrollo con respecto a la principal. Normalmente representan versiones del software que posteriormente son integradas a la línea principal.

![](https://i.stack.imgur.com/mvLUy.png)

# Comandos Ramas I

Ver listado de ramas:

`git branch`

Crear una rama:

`git branch nombre_rama`

Cambiarnos a una rama:

`git checkout nombre_rama`

Crear una rama y moverse en un paso:

`git checkout -b nombre_rama`

Comparar ramas:

`git diff nombre_rama..nombre_rama`

# Comandos Ramas II

Ver ramas idénticas a la actual:

`git branch --merged`

Renombrar ramas:

`git branch -m nombre_antiguo nombre_nuevo`

Eliminar ramas:

`git branch -d nombre_rama`


`git branch -D nombre_rama`

Integrar ramas a la actual:

`git merge nombre_rama`

Resolver conflictos (se suele hacer manualmente):

`git merge --abort`

# Comandos Ramas III

Almacenar cambios temporales:

`git stash save "Mensaje"`

Lista cambios:

`git stash list`

Ver contenido de un cambio temporal:

`git stash show -p nombre_stash`

Eliminar un cambio temporal:

`git stash drop nombre_stash`

Aplicar cambio del *stash*:

`git stash apply nombre_stash`


`git stash pop nombre_stash`
# GitHub no es Git
![](https://solanch96.files.wordpress.com/2017/06/github.gif?w=500&h=236&crop=1)

# Comandos GitHub |
Añadir repositorio remoto:

`git remote add origin url`

Ver repositorios remotos:

`git remote -v`

Eliminar repositorio remoto:

`git remote rm origin`

Añadir cambios del repositorio local al remoto:

`git push -u origin master`

Añadir cambios del repositorio remoto al local:

`git pull`

# Comandos GitHub ||
Ver *branches* remotos:

`git branch -r`

Ver todos los *branches*:

`git branch -a`

Clonar un repositorio remoto:

`git clone url`

# Dar seguimiento a *branches* remotos
* LOCAL --> REMOTO
1. Cambios en el repositorio local.
2. *Commit* de los cambios.
3. Añadir cambios a repositorio remoto:

`git push`

* REMOTO --> LOCAL
1. Sincronización y unión:

`git fetch origin`

`git merge origin/master`

2. En un solo paso:

`git pull`

# Operaciones con *branches* remotos
* Creación

1. Crear *branch* local.
2. Hacer cambios en dicho *branch*.
3. Hacer *commit*.
4. Copiar el *branch* al repositorio remoto:

`git push -u origin branch_remoto`

* Copia

`git checkout -b local remoto`

* Eliminación

`git push origin --delete branch_remoto`

# Lenguaje de *Markdown*
* Markdown es un lenguaje de etiquetado ligero que simplifica la elaboracion de documentos.
* Se ideó pensando en una herramienta para escribir paginas web en un texto simple facil de leer.
* Actualmente, se utiliza para documentar software ya que al ser texto plano puede entrar dentro de cualquier sistema de control de versiones e incluye muchas extensiones para colorear código fuente en distintos lenguajes.

# Sintaxis |

|Formato  |Sintaxis  |
|----------|----------|
|Negrita|**Texto en negrita**|
|Cursiva|*Texto en cursiva*|
|Lista con viñetas|1. Primera línea 2. Segunda línea|
|Lista anidada|	* Primer nivel * Segundo nivel|
|Encabezados (hasta 6 niveles)|# Encabezado primer nivel ## Encabezado segundo nivel ### Encabezado nivel tres|
|Citas en bloque|> Las citas en bloque deben comenzar y terminar con una línea en blanco|

# Sintaxis ||

|Formato  |Sintaxis  |
|----------|----------|
|Código en línea|`Esto es código de línea`|
|Bloques de código|~~~ Ejemplo de bloque ~~~|
|Imágenes|![Texto alternativo](url/imagen.png)|
|Vínculos|[Texto del vínculo](url)|
|Imágenes con vínculos|[![Texto alternativo](imagen)](url)|
|Línea horizontal|- - - (Salto de línea antes y después)|
|Salto de línea|&nbsp (Dos saltos de línea antes)|

# Eclipse

Eclipse es un entorno integrado de desarrollo (IDE).
* Se diseñó inicialmente como IDE para Java, sin embargo ahora soporta otros lenguajes como C++.
* Ayuda a escribir código más rápido y libre de algunos errores sintácticos, y ayuda a mantener un estilo de programación homogéneo.
* Facilita la depuración de código.
* Hay una gran documentación.

# Instalación
* Utilizaremos eclipse para C++.

[Eclipse para C++](https://www.eclipse.org/downloads/packages/release/photon/r/eclipse-ide-cc-developers)

* Para eclipse existen *puglins* integrados con git

[https://www.eclipse.org/egit](https://www.eclipse.org/egit/)

 # Recursos
Recursos Git:
* [Guía sencilla de Git](http://rogerdudler.github.io/git-guide/index.es.html)
* [Pro Git book](https://git-scm.com/book/en/v2)

Recursos Markdown:
* [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* [Guía en castellano extendida](https://joedicastro.com/pages/markdown.html)

Recursos Eclipse:
* En las aulas se puede cargar con la orden eclipse3.3
* [Eclipse para C++](https://www.eclipse.org/downloads/packages/release/photon/r/eclipse-ide-cc-developers)

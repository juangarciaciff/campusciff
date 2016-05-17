Ejercicio práctico sobre la utilización avanzada de Git, GitHub y Markdown
==================================================

- Alumno: **Juan Antonio García Cuevas**
- Fecha.: 16/05/2016

Notas
==================================================

>1. Este ejercicio es continuación del anterior por lo que tendréis que seguir trabajando en el repositorio campusciff.
>2. También tendreís que ir poniendo los comandos que habéis tenido que utilizar durante todos los ejercicios y las explicaciones y capturas de pantalla que consideréis necesarias al fichero README.md del citado repositorio.

Crear una rama v0.2
==================================================

#### 1. Crear una rama **v0.2**.

```bash
    git branch v0.2
```

#### 2. Posiciona tu carpeta de trabajo en esta rama.

```bash
    git checkout v0.2
```

Añadir fichero 2.txt
==================================================

#### 1. Añadir un fichero **2.txt** en la rama **v0.2**.

```bash
    echo "Fichero 2" > 2.txt
```

Crear rama remota v0.2
==================================================

#### 1. Subir los cambios al reposiorio remoto.

```bash
    git add -A
    git commit -m "Se añade el fichero 2.txt a la rama v2.0"
    git push
```

Merge directo
==================================================

#### 1. Posicionarse en la rama **master**.

```bash
    git checkout master
```

#### 2. Hacer un merge de la rama **v0.2** en la rama **master**.

```bash
    git merge v0.2 -m "Se hace merge de la rama v0.2 en master"
```

Merge con conflicto
==================================================

#### 1. En la rama **master** poner **Hola** en el fichero **1.txt** y hacer commit.

```bash
    git checkout master
    echo "Hola" >> 1.txt
	git add -A
	git commit -m "Se añade 'Hola' al fichero 1.txt desde la rama master"
```

#### 2. Posicionarse en la rama **v0.2** y poner **Adios** en el fichero "1.txt" y hacer commit.

```bash
    git checkout v0.2
    echo "Adios" >> 1.txt
	git add -A
	git commit -m "Se añade 'Adios' al fichero 1.txt desde la rama v0.2"
```

#### 3. Posicionarse de nuevo en la rama **master** y hacer un merge con la rama **v0.2**

```bash
    git checkout master
    git merge v0.2 -m "Se hace un nuevo merge de la rama v0.2 en master, con errores"
```

![Merge con conflicto](images/MergeConflicto.PNG)

Listado de ramas
==================================================

#### 1. Listar las ramas con merge y las ramas sin merge.

```bash
    git branch --merged
    git branch --no-merged
```

![Ramas con merge y sin merge](images/MergeRamas.PNG)

Arreglar conflicto
==================================================

#### 1. Arreglar el conflicto anterior y hacer un commit.

```bash
    git add -A
    git commit -m "Subimos las correcciones al merge fallido"
```

![Merge corregido](images/MergeCorregido-01.PNG)

Borrar rama
==================================================

#### 1. Crear un tag **v0.2**

```bash
    git tag v0.2 -m "Asignando versión v0.2 a la rama rincipal"
```

#### 2. Borrar la rama **v0.2**

```bash
    git branch -d v0.2
```

Listado de cambios
==================================================

#### 1. Listar los distintos commits con sus ramas y sus tags.

```bash
    git list
```

![List](images/MergeCorregido-02.PNG)

Crear una organización
==================================================

#### 1. Crear una organización llamada **campusciff-tunombredeusuariodegithub**

Crear equipos
==================================================

#### 1. Crear 2 equipos en la organización **campusciff-tunombredeusuariodegithub**, uno llamado **administradores** con más permisos y otro **colaboradores** con menos permisos.

1. Pulsar en el icono "**+**" en el lado superior derecho y seleccionar "**New organization**".
1. Introducir **campusciff-juangarciaciff** en el cuadro de texto "**Organization name**"
1. Introducir **juangarcia@campusciff.net** en el cuadro de texto "**Billing email**"
1. Pulsar sobrre el botón "**Create organization**"

![Crear organizacion](images/CrearOrganizacion-01.PNG)

#### 2. Meter a github.com/asanzdiego y a 2 de vuestros compañeros de clase en el equipo **administradores**.

1. Desde la página de Perfil de usuario acceder a la organización recién creada.
1. En la pantalla que se abre pulsar en el Tab "**Teams**" y luego en el botón "**Create a new team**".
1. En el formulario que se abre escribir "**Administradores**" en el cuadro de texto "**Team name**" y pulsar el botón "**Create team**".

#### 3. Meter a github.com/asanzdiego y a otros 2 de vuestros compañeros de clase en el equipo **colaboradores**.

1. Desde la página de Perfil de usuario acceder a la organización recién creada.
1. En la pantalla que se abre pulsar en el Tab "**Teams**" y luego en el botón "**Create a new team**".
1. En el formulario que se abre escribir "**Colaboradores**" en el cuadro de texto "**Team name**" y pulsar el botón "**Create team**".

Crear un index.html
==================================================

#### 1. Crear un index.html que se pueda ver como página web en la organización.

Crear Pull-requests
==================================================

#### 1. Hacer 2 forks de 2 repositorios **campusciff-tunombredeusuariodegithub.github.io** de 2 organizaciones de las que no seais ni administradiores ni colaboradores.

#### 2. Crearos una rama en cada fork.

#### 3. En cada rama modificar el fichero **index.html** añadiendo vuestro nombre.

#### 4. Con cada rama hacer un pull-request.

Gestionar Pull-requests
==================================================

#### 1. Aceptar los pull-request que lleguen a los repositorios de tu organización.

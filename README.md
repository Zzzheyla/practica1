# Universidad [Nombre de la Universidad]  
## Facultad de [Nombre de la Facultad]  
### Carrera de Ingeniería en Software  

**Asignatura:** Manejo y Configuración de Software  
**Nombre del Estudiante:** Sheyla Eliana Pacha Lucintuña 
**Fecha:** 07/04/2026

---

# Evaluación Práctica de Git y GitHub

## Instrucciones Generales

- Cada pregunta debe ser respondida directamente en este archivo **(README.md)** debajo del enunciado correspondiente.
- Cada respuesta debe ir acompañada de uno o más **commits**, según se indique en cada pregunta.
- Cuando se indique, deberán realizarse acciones prácticas dentro del repositorio (como creación de archivos, ramas, resolución de conflictos, etc.).
- Cada pregunta debe estar **etiquetada con un tag**, únicamente en el commit final correspondiente, con el formato: `"Pregunta 1"`, `"Pregunta 2"`, etc.

---

## Pregunta 1 (1 punto)

**Explicar la diferencia entre los siguientes conceptos/comandos en Git y GitHub:**

- `git clone`  
- `fork`  
- `git pull`

### Parte práctica:

- Realizar un **fork** de este repositorio en la cuenta personal de GitHub del estudiante.
- Luego, realizar un **clone** del fork en el equipo local.
- En este README, describir el proceso seguido:
  - ¿Cómo se realizó el fork?
  - ¿Cómo se realizó el clone del fork?
  - ¿Cómo se verificó que se estaba trabajando sobre el fork y no sobre el repositorio original
**📝 Respuesta:**



### Diferencias entre git clone, fork y git pull

- **git clone**: Es un comando de Git que permite copiar un repositorio remoto a la máquina local, incluyendo todos los archivos, ramas e historial de commits.

- **fork**: Es una funcionalidad de GitHub que permite crear una copia de un repositorio en la cuenta personal del usuario, manteniendo una relación con el repositorio original.

- **git pull**: Es un comando que permite actualizar el repositorio local con los últimos cambios del repositorio remoto, combinando `git fetch` y `git merge`.



### Proceso realizado

El fork del repositorio se realizó mediante la opción "Fork" disponible en GitHub, lo que permitió crear una copia del repositorio original en mi cuenta personal.

Posteriormente, se utilizó el comando `git clone` para descargar el repositorio fork a mi equipo local, permitiendo trabajar de manera independiente.

Finalmente, se verificó que el repositorio clonado correspondía al fork mediante el comando `git remote -v`, confirmando que la URL remota pertenecía a mi cuenta de GitHub y no al repositorio original.

![Fork](imagenes/p1.png)

![Clone](imagenes/p2.png)



## Pregunta 2 (1 punto)

**Configurar un archivo `.gitignore` para que ignore:**

- Todos los archivos con extensión `.log`.
- Una carpeta llamada `temp/`.
- Todos los archivos `.md` y `.txt`de la carpeta `doc/`. (Probar agregando un archivo `prueba.md` y un archivo `prueba.txt` dentro de la carpeta y fuera de la carpeta.)

### Requisitos:

1. Realizar un **primer commit** que incluya únicamente el archivo `.gitignore` con las reglas de exclusión definidas.
2. Realizar un **segundo commit** donde se explique en este README la función del archivo `.gitignore` y se muestre evidencia de que los archivos y carpetas indicadas no están siendo rastreadas por Git.

**Importante:**  
- Solo el **segundo commit** debe llevar el **tag `"Pregunta 2"`**.

**📝 Respuesta:**

### Función del archivo .gitignore

El archivo `.gitignore` permite definir qué archivos o carpetas deben ser ignorados por Git, evitando que sean rastreados o incluidos en los commits.

En este caso, se configuró para ignorar:
- Archivos con extensión `.log`
- La carpeta `temp/`
- Archivos `.md` y `.txt` dentro de `doc/`

Se realizó una prueba creando archivos dentro y fuera de las rutas indicadas, verificando mediante `git status` que los archivos configurados no son rastreados por Git.

![gitignore](imagenes/p3.png)




---

## Pregunta 3 (2 puntos)

**Utilizar Git Flow para desarrollar una nueva funcionalidad llamada `ingresar-encabezado`.**

### Requisitos:

- Inicializar el repositorio con Git Flow, utilizando las ramas por defecto: `main` y `develop`.
- Crear una rama de tipo `hotfix` con el nombre `ingresar-encabezado`.
- En dicha rama, **completar con los datos personales del estudiante** el encabezado que ya se encuentra al inicio de este archivo `README.md`.
- Realizar al menos un commit durante el desarrollo.
- Finalizar el hotfix siguiendo el flujo de trabajo establecido por Git Flow.

### En este README, se debe incluir:

- Los **comandos exactos** utilizados desde la inicialización de Git Flow hasta el cierre del hotfix.
- Una descripción del **proceso seguido**, indicando el propósito de cada paso.
- Una reflexión sobre las **ventajas de aplicar Git Flow**, especialmente en contextos colaborativos o proyectos de larga duración.

**Importante:**

- Deben realizarse varios commits durante esta pregunta.
- **Solo el commit final** debe llevar el **tag `"Pregunta 3"`**.
- El flujo debe respetar la estructura de Git Flow con las ramas `develop` y `main`.

**📝 Respuesta:**

## Pregunta 3

### Comandos utilizados

Se utilizaron los siguientes comandos para aplicar Git Flow:

- git flow init
- git flow hotfix start ingresar-encabezado
- git add README.md
- git commit -m "Agrega encabezado"
- git flow hotfix finish ingresar-encabezado

### Descripción del proceso

Primero, se inicializó Git Flow en el repositorio, lo que permitió estructurar el flujo de trabajo con las ramas principales `main` y `develop`.

Posteriormente, se creó una rama de tipo hotfix denominada `ingresar-encabezado`, con el objetivo de realizar una modificación urgente en el archivo README.md.

Dentro de esta rama, se completó el encabezado con los datos personales del estudiante y se registraron los cambios mediante un commit.

Finalmente, se finalizó el hotfix, lo que permitió integrar automáticamente los cambios tanto en la rama `main` como en `develop`, manteniendo la coherencia del proyecto.

##-Inicialización de Git flow
![gitflowinit](imagenes/p5.png)

##-Modificacion del encabezado en README.md
![encabezado1](imagenes/p6.png)

### Reflexión

El uso de Git Flow permite organizar el desarrollo del software mediante el uso de ramas específicas para cada tipo de tarea. Esto facilita el trabajo colaborativo, reduce errores y permite mantener un control más claro sobre las versiones del proyecto, especialmente en proyectos grandes o de larga duración.


---

## Pregunta 4 (2 puntos)

**Trabajo con Issues y Pull Requests**

### Parte teórica:

- Explicar qué es un **issue** en GitHub.
- Explicar qué es un **pull request** y cuál es su finalidad.
- Indicar la diferencia entre ambos y cómo se relacionan en un entorno de trabajo colaborativo.

### Parte práctica:

- Trabajar en la rama `develop`, ya existente desde la configuración de Git Flow.
- Crear un **issue** titulado `"Respuesta a la Pregunta 4"`, en el que se indique que su objetivo es documentar esta pregunta.
- Realizar los cambios necesarios en este archivo `README.md` para responder esta pregunta.
- Realizar un **commit** con los cambios y subirlo a la rama `develop` del repositorio remoto.
- Crear un **pull request** desde `develop` hacia `main` en GitHub.
- **Vincular el pull request con el issue creado**, de manera que al ser aprobado y fusionado, el issue se cierre automáticamente.
- **Aprobar** el pull request para que se haga el merge respectivo hacia `main`.

### En este README, se debe incluir:

- Un resumen del procedimiento realizado.
- El número y enlace del issue creado.
- El número y enlace al pull request.

**📝 Respuesta:**

## Pregunta 4

### ¿Qué es un Issue?

Un issue en GitHub es una herramienta utilizada para registrar tareas, errores, mejoras o cualquier aspecto pendiente dentro de un proyecto. Permite organizar el trabajo, asignar responsables y dar seguimiento al progreso.

### ¿Qué es un Pull Request?

Un pull request es una solicitud para integrar cambios realizados en una rama hacia otra rama del repositorio. Su finalidad es revisar, discutir y aprobar modificaciones antes de incorporarlas al proyecto principal.

### Diferencia y relación

La principal diferencia es que el issue describe un problema o tarea, mientras que el pull request contiene la solución a ese problema.

Ambos se relacionan en entornos colaborativos, ya que un pull request puede estar vinculado a un issue, permitiendo cerrar automáticamente el issue una vez que los cambios son aprobados e integrados.

  Evidencia de la creacion del ISSUE
  ![ISSUE](imagenes/p7.png)


### Procedimiento realizado

Se creó un issue en GitHub con el título "Respuesta a la Pregunta 4", con el objetivo de documentar esta sección del examen.

Posteriormente, se trabajó en la rama develop, donde se realizaron los cambios en el archivo README.md para responder la pregunta.

Se realizó un commit con los cambios y se subieron al repositorio remoto.

Luego, se creó un pull request desde la rama develop hacia main, vinculándolo con el issue mediante la palabra clave "Closes", permitiendo que el issue se cierre automáticamente al realizar el merge.

Finalmente, el pull request fue aprobado y fusionado correctamente.

### Evidencia

Issue: https://github.com/Zzzheyla/comandos_basicos/issues/2#issue-4223200859
Pull R: https://github.com/Zzzheyla/practica1/pull/1#issue-4223343401

![ISSUE](imagenes/p7.png)


---

## Pregunta 5 (2 puntos)

**Resolver conflictos entre ramas y realizar un Pull Request**

### Requisitos:

- Crear dos ramas llamadas `ramaA` y `ramaB`, ambas a partir de la rama `develop`.
- En `ramaA`, crear un archivo llamado `archivoA.txt` con el contenido:  
  `Contenido A`
- En `ramaB`, crear un archivo con el mismo nombre (`archivoA.txt`), pero con el contenido:  
  `Contenido B`
- Intentar fusionar `ramaB` sobre `ramaA`, lo cual debe generar un conflicto.
- Resolver el conflicto combinando ambos contenidos.
- Realizar el merge de `ramaA` hacia `develop`.
- Crear un **pull request** desde `develop` hacia `main`.
- Una vez completado lo anterior, eliminar las ramas `ramaA` y `ramaB` tanto local como remotamente.

### En este README, se debe incluir:

- El procedimiento completo:
  - Cómo se crearon las ramas.
  - Cómo se generó y resolvió el conflicto.
  - Cómo se realizó el merge hacia `develop`.
  - Cómo se eliminaron las ramas al finalizar.
- El enlace al pull request.
- Una breve explicación de qué es un conflicto en Git y por qué ocurrió en este caso.

**📝 Respuesta:**

<!-- Escribe aquí tu respuesta completa a la Pregunta 5 -->

---

## Pregunta 6 (2 puntos)

**Realizar limpieza, explicar versionamiento semántico y enviar cambios al repositorio original**

### Requisitos:

- Trabajar en la rama `develop` del fork del repositorio.
- Eliminar los archivos `archivoA.txt` y `archivoB.txt` creados en preguntas anteriores.
- Realizar un merge desde `develop` hacia `main` en el repositorio local.
- Enviar los cambios de la rama `main` local a la rama `develop` del repositorio remoto (fork). Recuerde incluir todos los tags creados (6 tags).
- Finalmente, crear un **pull request** desde la rama `develop` del fork hacia la rama `main` del repositorio original (del cual se realizó el fork en la Pregunta 1). El titulo del pull request debe ser "NOMBRE APELLIDOS", en la descripción colocar el link de su repositorio de GitHub.

### En este README, se debe incluir:

- Una explicación del proceso realizado paso a paso.
- Una explicación del **versionamiento semántico**, indicando:
  - En qué consiste.
  - Sus tres componentes (MAJOR, MINOR, PATCH).
- El enlace al pull request creado hacia el repositorio original.
- Si hace falta agregar alguna evidencia adicional, agregue un tag adicional que sea `Version Final`.

**📝 Respuesta:**

 1. Proceso realizado paso a paso

1. **Trabajo en la rama `develop` del fork**
   Se hizo checkout a la rama `develop` en el repositorio local:

   ```bash
   git checkout develop
   ```

2. **Realizar cambios y commit**
   Se hicieron los cambios necesarios y se realizó un commit:

   ```bash
   git commit -m "Cambios aplicados en develop"
   ```

3. **Merge de `develop` a `main` en el repositorio local**
   Se cambió a la rama `main` y se hizo el merge de `develop`:

   ```bash
   git checkout main
   git merge develop
   ```

4. **Enviar los cambios de `main` local a `develop` del fork remoto**
   Se enviaron los cambios a la rama `develop` del repositorio remoto, incluyendo todos los tags (6 en total):

   ```bash
   git push origin main:develop --tags
   ```

5. **Creación del Pull Request hacia el repositorio original**

   * Se creó un PR desde la rama `develop` del fork hacia la rama `main` del repositorio original.
   * Título del PR: `"NOMBRE APELLIDOS"`
   * Descripción del PR: Se colocó el link del repositorio del fork en GitHub.

---

2. Versionamiento semántico (SemVer)

El **versionamiento semántico** es un estándar para asignar números de versión a los releases de software de forma que reflejen la naturaleza de los cambios realizados.

Componentes

1. **MAJOR (Mayor)**
   Incrementa cuando se realizan cambios incompatibles con versiones anteriores (breaking changes).
   Ejemplo: `v2.0.0` → cambio que rompe compatibilidad con `v1.x.x`.

2. **MINOR (Menor)**
   Incrementa cuando se añaden nuevas funcionalidades de manera compatible con versiones anteriores.
   Ejemplo: `v1.2.0` → se agregan nuevas funciones sin romper lo existente.

3. **PATCH (Parche)**
   Incrementa cuando se realizan correcciones de errores sin agregar nuevas funcionalidades ni romper compatibilidad.
   Ejemplo: `v1.2.1` → se corrigen bugs menores.


3. Tag adicional

Se agregó un tag adicional para evidenciar la versión final:

```bash
git tag -a "Version Final" -m "Entrega final del proyecto con todos los cambios"
git push origin "Version Final"
```

---

<!-- Escribe aquí tu respuesta completa a la Pregunta 6 -->

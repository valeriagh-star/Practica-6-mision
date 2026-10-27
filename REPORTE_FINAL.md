# Práctica 6

## Misión: ¡rescate del repositorio!

> ### Integrantes del Equipo Aurora:
> * García Herrera Valeria
> * Grajeda Palacios Dulce Abril
> * Pérez Megchun Pablo de Jesús

> ### Integrantes del Equipo Órbita:
> * Torres Trejo Abraham
> * 
> * 

> ### Breve descripción de la práctica:
> <p align="justify">
> En esta práctica aplicamos un flujo de trabajo colaborativo basado en **Git Flow** y la gestión de **Pull Requests** para coordinar el desarrollo entre los equipos **Aurora** y **Órbita**. A lo largo de la actividad gestionamos la bifurcación de ramas independientes (`feature/*`) para el desarrollo de misiones específicas, practicamos la integración continua sobre la rama `develop`, resolvimos de manera manual y directa conflictos de fusión en la terminal causados por modificaciones paralelas, y realizamos revisiones cruzadas de código antes de consolidar la publicación final y estable del repositorio en la rama principal (`main`).
> </p>

---

### 1. Uso de ramas
- **`main`**: Contiene la versión estable, limpia y lista para producción de todo el proyecto.
- **`develop`**: Sirvió como el entorno principal de integración continua donde ambos equipos unimos nuestros avances antes de la publicación final.
- **`feature/*`**: Ramas independientes (`feature/aurora-lanzamiento` y `feature/orbita-aterrizaje`) utilizadas por cada equipo para avanzar sin interferir con el trabajo del otro.
- 
---

### 2. Creación de ramas, commits y Pull Requests
Cada equipo creamos nuestra respectiva rama de características a partir de `develop` mediante la terminal. Tras realizar las modificaciones correspondientes en los archivos `misiones/aurora.md`, `misiones/orbita.md` y `panel/estado.md`, guardamos los cambios mediante `git commit` y los publicamos en GitHub con `git push`. Luego abrimos los Pull Requests hacia `develop`, llenando en la descripción la plantilla proporcionada para explicar con detalle los cambios realizados en cada pull.
---

### 3. Revisión de código y resolución de conflictos
En los Pull Requests nos dejamos un comentario tanto para el de Aurora como para Órbita, en el cual dimos respuesta a las preguntas que nos hicieron. Durante el proceso de integración surgió un conflicto de fusión en el archivo `panel/estado.md` debido a modificaciones simultáneas en las mismas líneas. Para resolverlo:
1. Sincronizamos localmente ejecutando `git merge origin/develop`.
2. Editamos el conflicto con el editor `nano` para unificar los datos de ambos equipos.
3. Guardamos los cambios y completamos el merge con un nuevo commit.

---

### 4. Publicación final en `main`
Una vez que la rama `develop` contenía la versión completa e integrada de ambos equipos, se abrió el Pull Request final hacia `main` (`base: main` ← `compare: develop`). Tras la verificación final, se aprobó y realizó el merge a la rama principal.

---

## Comandos de Git utilizados

1. **`git checkout -b <nombre-rama>`**  
   * **Utilidad:** Nos permitió crear una nueva rama y cambiarnos a ella en un solo paso para trabajar en nuestras misiones sin modificar la rama principal.

2. **`git add <archivo>`**  
   * **Utilidad:** Nos sirvió para preparar los archivos que habíamos modificado y dejar los cambios listos para empaquetarse en el próximo commit.

3. **`git fetch`**  
   * **Utilidad:** Nos permitió consultar y traer las novedades de GitHub sin alterar ni sobreescribir nuestro código local.

4. **`git switch -`**  
   * **Utilidad:** Nos ayudó a saltar rápidamente a la rama en la que habíamos estado trabajando justo antes.

5. **`git diff --staged`**  
* **Utilidad:** Nos permitió revisar exactamente qué líneas y modificaciones ya habíamos preparado con `git add` antes de confirmarlas en el commit.

6. **`git merge origin/develop`**  
   * **Utilidad:** Nos permitió traer la versión integrada de `develop` a nuestra rama local para identificar y corregir las diferencias de texto en el editor.

7. **`git log --oneline --graph --decorate --all`**  
   * **Utilidad:** Nos desplegó el mapa visual completo del historial para confirmar que todas las ramas y fusiones se habían unido correctamente.

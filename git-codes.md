# Comandos Git Útiles para Tu Repositorio

## 0. `git init`

El comando `git init` se utiliza para iniciar un nuevo repositorio Git en un directorio existente. Cuando ejecutas `git init`, Git crea una nueva subcarpeta oculta llamada `.git` en el directorio actual. Esta subcarpeta contiene todos los archivos necesarios para el funcionamiento interno de Git y controla el repositorio.

```bash
git init
```

## 1. `git config --global user.name "<Tu Nombre>"`

Configura tu nombre de usuario globalmente en Git para asociar tus commits con tu nombre.

**Ejemplo:**

```bash
$ git config --global user.name "Tu Nombre"
```

## 2. `git config --global user.email "<tu@email.com>"`

Configura tu dirección de correo electrónico globalmente en Git para asociar tus commits con tu dirección de correo electrónico.

**Ejemplo:**

```bash
$ git config --global user.email "tu@email.com"
```

## 3. `git log`

Muestra el historial de confirmaciones en la rama actual.

**Salida de Consola:**

```bash
$ git log
commit abcdef1234567890
Author: Tu Nombre <tu@email.com>
Date:   Mié Oct 20 14:47:23 2023 -0400

    Mensaje de la confirmación anterior

commit 1234567890abcdef
Author: Tu Nombre <tu@email.com>
Date:   Mié Oct 19 10:15:42 2023 -0400

    Mensaje de otra confirmación

```

## 4. `git status`

Muestra el estado actual de los archivos en el repositorio.

**Salida de Consola:**

```bash
$ git status
On branch main
Your branch is up-to-date with 'origin/main'.

Changes not staged for commit:
  (use "git add <archivo>..." to update what will be committed)
  (use "git checkout -- <archivo>..." to discard changes in working directory)

        modified:   archivo-modificado.js

no changes added to commit (use "git add" and/or "git commit -a")

```

## 5. `git add <archivo>`

Prepara un archivo específico para ser confirmado.

**Salida de Consola:**

```bash
$ git add archivo-modificado.js
```

## 6. `git commit -m "<mensaje del commit>"`

Confirma los cambios para ser enviado.

**Salida de Consola:**

```bash
$ git commit -m "Descripción concisa del cambio que has hecho"
[luisRiofrio/temp-1 22c340b] Descripción concisa del cambio que has hecho
 1 file changed, 215 insertions(+)
 create mode 100644 git-codes.md
```

## 7. `git push origin <nombre-de-la-rama>`

Sube los cambios confirmados a la rama correspondiente en el repositorio remoto.

**Salida de Consola:**

```bash
$ git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 291 bytes | 291.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/tu-usuario/tu-repositorio.git
   abcdef1..1234567  main -> main

```

## 8. `git branch <nombre-de-la-rama>`

Crea una nueva rama en el repositorio local.

**Salida de Consola:**

```bash
$ git branch nueva-caracteristica
```

## 9. `git checkout <nombre-de-la-rama`>

Este comando te cambia a la rama especificada para que puedas empezar a trabajar en ella.

**Salida de Consola:**

```bash
$ git checkout nombre-de-la-rama
Switched to branch 'nombre-de-la-rama'
```

## 10. `git checkout -b <nombre-de-la-rama`>

Este comando crea una nueva rama con el nombre especificado y automáticamente te cambia a esa rama para que puedas empezar a trabajar en ella.

**Salida de Consola:**

```bash
$ git checkout -b nombre-de-la-rama
Switched to a new branch 'nombre-de-la-rama'
```

## 11. `git pull origin <nombre-de-la-rama>`

Obtiene los cambios del repositorio remoto y los fusiona con la rama actual en tu repositorio local.

**Salida de Consola:**

```bash
$ git pull origin main
From https://github.com/tu-usuario/tu-repositorio
 * branch            main     -> FETCH_HEAD
Already up to date.

```

## 12. `git clone <url-del-repositorio>`

Clona un repositorio remoto en tu máquina local.

**Salida de Consola:**

```bash
$ git clone https://github.com/tu-usuario/tu-repositorio.git
Cloning into 'tu-repositorio'...
remote: Enumerating objects: 100, done.
remote: Counting objects: 100% (100/100), done.
remote: Compressing objects: 100% (75/75), done.
Receiving objects: 100% (100/100), 10.00 KiB | 1.14 MiB/s, done.
Resolving deltas: 100% (25/25), done.

```

## 13. `git merge <nombre-de-la-rama>`

Fusiona una rama específica en la rama actual.

**Salida de Consola:**

```bash
$ git merge nueva-caracteristica
Updating abc1234..def5678
Fast-forward
 archivo-modificado.js | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
```

## 14. `git branch -D <rama-que-desea-borrar>`

Elimina una rama específica sin importar si los cambios se fusionaron o no a otra rama.

**Salida de Consola:**

```bash
$ git branch -D rama-que-desea-borrar
Deleted branch rama-que-desea-borrar (was 22c340b)
```

## 15. `git remote add origin <url-del-repositorio-remoto>`

Agrega un repositorio remoto a tu repositorio local.

**Salida de Consola:**

```bash
$ git remote add origin https://github.com/tu-usuario/tu-repositorio.git
```

## 16. `git remote -v`

Muestra las URLs de los repositorios remotos vinculados.

**Salida de Consola:**

```bash
$ git remote -v
origin  https://github.com/tu-usuario/tu-repositorio.git (fetch)
origin  https://github.com/tu-usuario/tu-repositorio.git (push)
```

## Tags en Git

Los tags en Git son referencias fijas a puntos específicos en la historia del repositorio. Se utilizan comúnmente para marcar versiones específicas del software.

## 17. `git tag <nombre-del-tag>`

Crea un nuevo tag para marcar una versión específica en tu repositorio.

**Salida de Consola:**

```bash
$ git tag v1.0.0
```

## 18. `git tag`

Ver la lista de todas las etiquetas existentes en el repositorio.

**Salida de Consola:**

```bash
$ git tag
v1.0.0
```

## 19. `git tag -d <nombre-de-la-etiqueta>`

Eliminar una etiqueta.

**Salida de Consola:**

```bash
$ git tag -d <nombre-de-la-etiqueta>
Deleted tag 'nombre-de-la-etiqueta' (was 4033653)
```

## 20. `git show <nombre-del-tag>`

Muestra información detallada sobre un tag específico, incluyendo los cambios asociados a ese tag.

**Salida de Consola:**

```bash
$ git show v1.0.0
commit abcdef1234567890
Author: Tu Nombre <tu@email.com>
Date: Mié Oct 20 14:47:23 2023 -0400

    Mensaje del commit

diff --git a/archivo-modificado.js b/archivo-modificado.js
index 1234567..89abcdef 100644
--- a/archivo-modificado.js
+++ b/archivo-modificado.js
@@ -1,5 +1,5 @@
// Código anterior
console.log("Hola, mundo!");
+console.log("Nueva línea agregada en v1.0.0");
// Más código aquí
```

## 21. `git reverse`

Se utiliza para combinar una rama con otra, generalmente para integrar cambios de una rama en otra. A diferencia de `git merge`, que crea un nuevo commit de fusión, `git rebase` reescribe el historial del proyecto.

1. **Cómo Funciona:** Antes de realizar un rebase, asegúrate de tener la última versión de la rama en la que estás trabajando.

   ```bash
   git pull origin <tu-rama>
   ```

   Iniciar el Rebase: Ve a la rama en la que deseas aplicar los cambios y ejecuta el comando git rebase.

   ```bash
   git checkout <rama-destino>
   git rebase <tu-rama>
   git rebase --continue
   ```

   **Salida de Consola:**

   ```bash
   Applying: tu-último-commit
   ...
   Successfully rebased and updated refs/heads/rama-destino.
   ```

## 22. `git stash`

Se utiliza para guardar temporalmente los cambios en un directorio de trabajo sin hacer commit. Esto es útil cuando necesitas cambiar de rama o hacer otras operaciones y deseas guardar tus cambios actuales en un estado intermedio.

1. **Cómo Funciona:** Para guardar los cambios actuales en un stash, utiliza el siguiente comando:

   ```bash
   git stash save "Descripción del Stash"
   ```

## 23. `git stash list`

Puedes ver una lista de todos los stashes creados en tu repositorio usando:

**Cómo Funciona**

```bash
git stash list
```

## 24. `git stash pop`

Se utiliza para aplicar el último stash guardado y eliminarlo de la lista de stashes. Esto es útil cuando deseas recuperar tus cambios guardados en un stash y aplicarlos a tu rama de trabajo actual en un solo paso.

**Cómo Funciona**

```bash
git stash pop
```

## 25. `git stash apply`

Cuando estés listo para aplicar un stash, puedes hacerlo con el comando de abajo y recuerda reemplazar el numero-del-stash con el indice del stash que deseas aplicar.

**Cómo Funciona**

```bash
git stash apply stash@{número-del-stash}

```

## 26. `git stash drop`

Se utiliza para eliminar un stash específico en caso de ya no necesitarlo.

**Cómo Funciona**

```bash
git stash drop stash@{número-del-stash}
```

## 27. `git cherry-pick`

Se utiliza para aplicar un commit específico desde una rama a otra. Esto es útil cuando deseas llevar cambios específicos de una rama a otra sin tener que fusionar toda la rama.

**Cómo Funciona**

1. **Encuentra el ID del Commit:**
   Antes de realizar un `cherry-pick`, necesitas conocer el ID del commit que deseas aplicar. Puedes encontrar el ID del commit usando `git log`:

   ```bash
   git log
   ```

2. **Aplicar el commit en otra rama:**

   ```bash
     git cherry-pick <ID-del-Commit>
     [cherry-pick ID-del-Commit] Descripción del Commit
   ```

## 28. `git revert`

se utiliza para deshacer un commit existente creando un nuevo commit. A diferencia de `git reset`, que modifica el historial y puede ser peligroso si los commits ya se han compartido con otros, `git revert` es seguro para deshacer cambios en commits públicos.

**Cómo Funciona**

1. **Aplicar el revert:**

   ```bash
     git revert <ID-del-Commit>
     Revert "<Descripción del Commit Original>"
     This reverts commit <ID-del-Commit>.
   ```

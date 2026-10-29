# Tema 1: Git

## Ejercicio 4 — Tienda Online
**Enlace al repositorio:** [https://github.com/dv-coding/DAM_CD_Tema1_Ejercicio4](https://github.com/dv-coding/DAM_CD_Tema1_Ejercicio4)

**Salida del terminal:**

```bash
dev@VM-W11DEV UCRT64 /c/DAM/ED
$ mkdir CD_Tema1_tienda-online

dev@VM-W11DEV UCRT64 /c/DAM/ED
$ cd CD_Tema1_tienda-online/

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online
$ git init -b main
Initialized empty Git repository in C:/DAM/ED/CD_Tema1_tienda-online/.git/

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (main)
$ echo 'Tema 1 - Ejercicio 4: Mi Tienda Online' > README.md

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (main)
$ git add README.md
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (main)
$ git commit -m 'Se inicializa el proyecto de la tienda online'
[main (root-commit) 6b3c625] Se inicializa el proyecto de la tienda online
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (main)
$ git branch develop

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (main)
$ git switch develop
Switched to branch 'develop'

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (develop)
$ git switch -c feature/carrito-compra
Switched to a new branch 'feature/carrito-compra'

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (feature/carrito-compra)
$ printf 'Teclado\nRatón\n' > carrito.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (feature/carrito-compra)
$ git add carrito.txt
warning: in the working copy of 'carrito.txt', LF will be replaced by CRLF the next time Git touches it

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (feature/carrito-compra)
$ git commit -m 'Se crea el carrito con los primeros productos'
[feature/carrito-compra daa964f] Se crea el carrito con los primeros productos
 1 file changed, 2 insertions(+)
 create mode 100644 carrito.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (feature/carrito-compra)
$ echo 'Monitor de 27 pulgadas' >> carrito.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (feature/carrito-compra)
$ git commit -am 'Se añade un monitor al carrito de compra'
warning: in the working copy of 'carrito.txt', LF will be replaced by CRLF the next time Git touches it
[feature/carrito-compra 48fda5f] Se añade un monitor al carrito de compra
 1 file changed, 1 insertion(+)

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (feature/carrito-compra)
$ git switch develop
Switched to branch 'develop'

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (develop)
$ git merge --no-ff feature/carrito-compra -m 'Se integra la funcioanlidad del carrito de compra'
Merge made by the 'ort' strategy.
 carrito.txt | 3 +++
 1 file changed, 3 insertions(+)
 create mode 100644 carrito.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (develop)
$ git switch -c release/1.0
Switched to a new branch 'release/1.0'

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (release/1.0)
$ echo 'Version 1.0 lista para producción' >> README.md

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (release/1.0)
$ git commit -am 'Se actualiza el fichero README.md indicando la versión 1.0'
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it
[release/1.0 f275718] Se actualiza el fichero README.md indicando la versión 1.0
 1 file changed, 1 insertion(+)

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (release/1.0)
$ git switch main
Switched to branch 'main'

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (main)
$ git merge --no-ff release/1.0
Merge made by the 'ort' strategy.
 README.md   | 1 +
 carrito.txt | 3 +++
 2 files changed, 4 insertions(+)
 create mode 100644 carrito.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (main)
$ git commit --amend -m 'Se integra la release 1.0 en main'
[main 2259721] Se integra la release 1.0 en main
 Date: Thu Oct 29 15:13:01 2026 +0100

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (main)
$ git tag v1.0

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (main)
$ git switch develop
Switched to branch 'develop'

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (develop)
$ git merge --no-ff release/1.0 -m 'se integra la release 1.0 en develop'
Merge made by the 'ort' strategy.
 README.md | 1 +
 1 file changed, 1 insertion(+)

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (develop)
$ git switch main
Switched to branch 'main'

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (main)
$ git switch -c hotfix/error-precio
Switched to a new branch 'hotfix/error-precio'

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (hotfix/error-precio)
$ echo 'ajuste de precio aplicado correctamente' >> carrito.txt

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (hotfix/error-precio)
$ git commit -am 'Se corrige el fallo de cálculo de precios'
warning: in the working copy of 'carrito.txt', LF will be replaced by CRLF the next time Git touches it
[hotfix/error-precio 3d5508f] Se corrige el fallo de cálculo de precios
 1 file changed, 1 insertion(+)

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (hotfix/error-precio)
$ git switch main
Switched to branch 'main'

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (main)
$ git merge --no-ff hotfix/error-precio -m 'Se integra el hotfix de precios en main'
Merge made by the 'ort' strategy.
 carrito.txt | 1 +
 1 file changed, 1 insertion(+)

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (main)
$ git tag v1.0.1

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (main)
$ git switch develop
Switched to branch 'develop'

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (develop)
$ git merge --no-ff hotfix/error-precio -m 'Se integra el hotfix de precios en develop'
Merge made by the 'ort' strategy.
 carrito.txt | 1 +
 1 file changed, 1 insertion(+)

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (develop)
$ git log --oneline --all --graph
*   720a90b (HEAD -> develop) Se integra el hotfix de precios en develop
|\
* \   29bba59 se integra la release 1.0 en develop
|\ \
| | | *   efc960d (tag: v1.0.1, main) Se integra el hotfix de precios en main
| | | |\
| | | |/
| | |/|
| | * | 3d5508f (hotfix/error-precio) Se corrige el fallo de cálculo de precios
| | |/
| | *   2259721 (tag: v1.0) Se integra la release 1.0 en main
| | |\
| | |/
| |/|
| * | f275718 (release/1.0) Se actualiza el fichero README.md indicando la versión 1.0
|/ /
* |   e2a9ab8 Se integra la funcioanlidad del carrito de compra
|\ \
| |/
|/|
| * 48fda5f (feature/carrito-compra) Se añade un monitor al carrito de compra
| * daa964f Se crea el carrito con los primeros productos
|/
* 6b3c625 Se inicializa el proyecto de la tienda online

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (develop)
$ git remote add origin https://github.com/dv-coding/DAM_CD_Tema1_Ejercicio4.git

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (develop)
$ git push --all origin
Enumerating objects: 20, done.
Counting objects: 100% (20/20), done.
Delta compression using up to 2 threads
Compressing objects: 100% (16/16), done.
Writing objects: 100% (20/20), 2.05 KiB | 67.00 KiB/s, done.
Total 20 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), done.
To https://github.com/dv-coding/DAM_CD_Tema1_Ejercicio4.git
 * [new branch]      develop -> develop
 * [new branch]      feature/carrito-compra -> feature/carrito-compra
 * [new branch]      hotfix/error-precio -> hotfix/error-precio
 * [new branch]      main -> main
 * [new branch]      release/1.0 -> release/1.0

dev@VM-W11DEV UCRT64 /c/DAM/ED/CD_Tema1_tienda-online (develop)
$ git push --tags origin
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/dv-coding/DAM_CD_Tema1_Ejercicio4.git
 * [new tag]         v1.0 -> v1.0
 * [new tag]         v1.0.1 -> v1.0.1

```
# Cómo subir esto a GitHub

La carpeta ya está lista: solo falta crear el repositorio con tu cuenta.

## Opción A, desde Claude Code (lo más cómodo)

Ábrelo en esta carpeta y pídele:

> Crea un repositorio privado en GitHub llamado concrecion con el contenido de
> esta carpeta y súbelo.

## Opción B, a mano, si tienes GitHub CLI

```bash
cd "concrecion"
git init -b main
git add -A
git commit -m "Concreción curricular de Inglés: web paso a paso y datos"
gh repo create concrecion --private --source=. --push
```

## Opción C, a mano, sin GitHub CLI

Crea primero el repositorio vacío en github.com (botón New, sin README) y luego:

```bash
cd "concrecion"
git init -b main
git add -A
git commit -m "Concreción curricular de Inglés: web paso a paso y datos"
git remote add origin https://github.com/TU-USUARIO/concrecion.git
git push -u origin main
```

## Privado o público

Ponlo **privado** salvo que el centro decida lo contrario. El contenido no lleva datos de
alumnado, pero es documentación interna del colegio en elaboración.

Si algún día queréis que se vea como página web con su dirección, en un repositorio **público**
se activa en Settings, Pages, rama main, carpeta raíz, y queda publicado en
`https://TU-USUARIO.github.io/concrecion/`.

## Lo que NO debe entrar aquí

Ningún documento con nombres de alumnos: perfiles, resumen operativo, adaptaciones curriculares,
informes trimestrales, y tampoco el mapa ni la red interactiva, que llevan nombres. El archivo
`.gitignore` ya bloquea los .docx, los .pdf y esos nombres de archivo, pero conviene mirarlo
antes de cada subida con `git status`.

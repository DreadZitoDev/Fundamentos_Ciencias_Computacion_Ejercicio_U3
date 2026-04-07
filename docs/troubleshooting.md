# Troubleshooting básico (Git en clase)

## 1) "Me equivoqué en un archivo y aún no hice commit"

Usar:

`git restore <archivo>`

Esto revierte el archivo al último commit.

## 2) "Agregué un archivo con git add pero no quería"

Usar:

`git restore --staged <archivo>`

Esto lo quita del staging sin perder el contenido editado.

## 3) "No entiendo qué cambió"

Usar:

`git diff`

y luego revisar solo el archivo en cuestión.

## 4) "Tengo un conflicto de merge"

Pasos sugeridos:

1. Abrir el archivo con conflicto.
2. Buscar marcadores `<<<<<<<`, `=======`, `>>>>>>>`.
3. Elegir o combinar contenido.
4. Guardar archivo.
5. `git add <archivo>`
6. `git commit -m "resuelve conflicto en ..."`

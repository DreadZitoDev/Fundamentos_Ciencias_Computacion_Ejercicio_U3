# Comandos Git básicos para la actividad

## Sección A - Inicio del trabajo

- `git clone <url-o-ruta>`: copia el repositorio.
- `git status`: muestra estado de archivos y rama.

## Sección B - Guardar cambios

- `git add <archivo>`: prepara archivo para commit.
- `git commit -m "mensaje"`: guarda un punto de avance.

## Sección C - Revisar historial y diferencias

- `git log --oneline`: historial resumido.
- `git diff`: muestra cambios no confirmados.

## Sección D - Ramas e integración

- `git branch`: lista ramas.
- `git checkout -b <rama>`: crea y cambia a nueva rama.
- `git merge <rama>`: integra cambios de otra rama.
- cambio en comandos.md para integrar en ramaas evitando merges

## Sección E - Corrección de errores

- `git restore <archivo>`: descarta cambios no confirmados en un archivo.
- `git restore --staged <archivo>`: saca un archivo del área de staging.

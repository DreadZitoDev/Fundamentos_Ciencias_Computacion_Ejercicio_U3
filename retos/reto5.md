# Reto 5 - Recuperación de un error

## Objetivo

Usar `git restore` (o mecanismo básico equivalente) para corregir un error local.

## Consigna

1. Editar `docs/flujo-trabajo.md` e introducir un cambio incorrecto a propósito.
2. Ejecutar `git diff` para verificar el cambio.
3. Descartar el cambio con `git restore`.
4. Verificar con `git status` que no queden cambios pendientes.

## Variante opcional

- Hacer `git add` del archivo por error.
- Recuperar con `git restore --staged`.

## Criterio de logro

El archivo vuelve al estado anterior y el equipo comprende cuándo usar cada comando.

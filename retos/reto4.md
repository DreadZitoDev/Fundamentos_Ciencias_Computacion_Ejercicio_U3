# Reto 4 - Conflicto intencional

## Objetivo

Provocar y resolver un conflicto real de merge.

## Consigna

1. Crear dos ramas desde `main`:
   - `version-ajuste-1`
   - `version-ajuste-2`
2. En **ambas ramas**, editar la **misma línea** de `app/version.txt`:
   - Rama 1 cambia a: `version_actual=0.2.0`
   - Rama 2 cambia a: `version_actual=0.3.0`
3. Confirmar cambios con commit en cada rama.
4. Integrar la primera rama en `main`.
5. Intentar integrar la segunda rama en `main` (debe aparecer conflicto).
6. Resolver el conflicto eligiendo una versión final consensuada (por ejemplo `0.3.0`).
7. Confirmar la resolución con commit.

## Pista

Si aparece conflicto, revisen `git status`, editen el archivo y luego usen `git add` + `git commit`.

## Criterio de logro

El equipo puede explicar cómo detectó el conflicto y qué decisión tomó al resolverlo.

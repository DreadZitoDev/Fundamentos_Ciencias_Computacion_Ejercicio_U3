# Guía docente: demo de merge sin conflicto, con conflicto y corrección

Esta guía permite mostrar en clase una progresión clara en pocos minutos.

## Escenario 1: merge sin conflicto (mismo archivo, secciones distintas)

Archivo sugerido: `docs/comandos.md`

1. Crear rama A:
   - `git checkout -b demo-sin-conflicto-a`
2. Editar solo la **Sección A** y hacer commit.
3. Volver a `main` y crear rama B:
   - `git checkout main`
   - `git checkout -b demo-sin-conflicto-b`
4. Editar solo la **Sección D** y hacer commit.
5. Integrar en `main`:
   - `git checkout main`
   - `git merge demo-sin-conflicto-a`
   - `git merge demo-sin-conflicto-b`

Resultado esperado: merge exitoso sin conflicto.

## Escenario 2: conflicto real de merge (misma línea)

Archivo sugerido: `app/version.txt`

1. Crear rama C:
   - `git checkout -b demo-conflicto-c`
2. Cambiar la línea a `version_actual=0.2.0` y hacer commit.
3. Volver a `main` y crear rama D:
   - `git checkout main`
   - `git checkout -b demo-conflicto-d`
4. Cambiar la misma línea a `version_actual=0.3.0` y hacer commit.
5. Integrar en `main`:
   - `git checkout main`
   - `git merge demo-conflicto-c`
   - `git merge demo-conflicto-d`

Resultado esperado: conflicto de merge en `app/version.txt`.

## Escenario 3: resolución + explicación de estudiantes

1. Abrir `app/version.txt` y mostrar marcadores:
   - `<<<<<<<`
   - `=======`
   - `>>>>>>>`
2. Pedir que elijan una versión final consensuada.
3. Guardar archivo y cerrar conflicto:
   - `git add app/version.txt`
   - `git commit -m "resuelve conflicto de version"`
4. Pedir explicación breve por equipo:
   - qué generó el conflicto,
   - cómo lo detectaron,
   - qué decisión tomaron.

## Escenario 4: simular error y corregir con Git

Archivo sugerido: `docs/flujo-trabajo.md`

1. Hacer un cambio incorrecto intencional.
2. Revisar con `git diff`.
3. Descartar con:
   - `git restore docs/flujo-trabajo.md`
4. Confirmar estado limpio con `git status`.

Resultado esperado: comprensión práctica de recuperación de errores locales.

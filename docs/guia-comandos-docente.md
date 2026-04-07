# Guía de comandos para demo docente (uso en vivo)

Esta guía es para el/la docente. Está pensada para mostrar la secuencia completa en 8 a 10 minutos.

## Preparación mínima

Pararse en una copia local del repo y verificar estado:

```bash
git status
```

## Demo 1: merge sin conflicto (mismo archivo, secciones distintas)

```bash
git checkout main
git checkout -b demo-sin-conflicto-a
```

Editar `docs/comandos.md` (solo sección A), luego:

```bash
git add docs/comandos.md
git commit -m "demo: ajuste seccion A"
```

```bash
git checkout main
git checkout -b demo-sin-conflicto-b
```

Editar `docs/comandos.md` (solo sección D), luego:

```bash
git add docs/comandos.md
git commit -m "demo: ajuste seccion D"
```

```bash
git checkout main
git merge demo-sin-conflicto-a
git merge demo-sin-conflicto-b
git log --oneline -n 5
```

## Demo 2: conflicto real (misma línea)

```bash
git checkout main
git checkout -b demo-conflicto-c
```

Editar `app/version.txt` a `version_actual=0.2.0`, luego:

```bash
git add app/version.txt
git commit -m "demo: version 0.2.0"
```

```bash
git checkout main
git checkout -b demo-conflicto-d
```

Editar `app/version.txt` a `version_actual=0.3.0`, luego:

```bash
git add app/version.txt
git commit -m "demo: version 0.3.0"
```

```bash
git checkout main
git merge demo-conflicto-c
git merge demo-conflicto-d
```

Esperado: conflicto en `app/version.txt`.

## Demo 3: resolución del conflicto

```bash
git status
```

Abrir `app/version.txt`, resolver marcadores y guardar (por ejemplo dejar `version_actual=0.3.0`).

```bash
git add app/version.txt
git commit -m "demo: resuelve conflicto de version"
git log --oneline -n 6
```

## Demo 4: error local + recuperación

```bash
# simular error
echo "ERROR_INTENCIONAL" >> docs/flujo-trabajo.md
git diff docs/flujo-trabajo.md

# recuperar
git restore docs/flujo-trabajo.md
git status
```

## Cierre de reflexión para estudiantes

Preguntas sugeridas:

1. ¿Por qué en el primer caso no hubo conflicto?
2. ¿Qué causó el conflicto en `app/version.txt`?
3. ¿Qué indican `<<<<<<<`, `=======`, `>>>>>>>`?
4. ¿Cuándo usarían `git restore`?

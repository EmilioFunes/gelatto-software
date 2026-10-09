# Cómo trabajamos en Gelatto Software

## Ramas

Nunca se sube directo a `main`: está protegida. Cada tarea se hace en su propia rama, creada desde `main` actualizado.

Formato: `tipo/descripcion-corta`, en minúscula y con guiones.

Ejemplos:
- `docs/perfil-cristian`
- `chore/estructura-proyecto`
- `feat/formulario-login`

## Commits

Formato: `tipo: qué hiciste`, en minúscula y en presente.

| Tipo | Para qué |
|---|---|
| `feat` | Una funcionalidad nueva |
| `fix` | Corregir un error |
| `docs` | Documentación |
| `chore` | Configuración y mantenimiento |

Ejemplo: `docs: agrega perfil de villa`

Un commit por cambio con sentido; no se mezclan tareas distintas en el mismo commit.

## Revisión de Pull Requests

Nadie aprueba su propio Pull Request. Todo PR necesita la aprobación de otro integrante antes de fusionarse.

Cada PR se asigna a un revisor, y el equipo se turna para que todos revisen y todos sean revisados.

Antes de aprobar, el revisor comprueba que:
- El archivo está en la carpeta correcta.
- El nombre de la rama y el commit siguen las convenciones.
- El contenido está completo y sin errores de ortografía.
- No hay archivos que no deberían subirse (`.env`, `__pycache__/`, `.venv/`).
- El PR indica el issue que resuelve.

Si algo falla, el revisor deja un comentario explicando qué cambiar y no aprueba hasta que se corrija.

## Cuándo se aprueba un Pull Request

Un PR se aprueba y se fusiona solo si cumple todo esto:
- Escribe `Closes #N` en la descripción, con el número de su issue.
- La rama y los commits siguen las convenciones de este documento.
- Cambia únicamente lo que pide su issue.
- No incluye claves, contraseñas ni archivos ignorados.
- Tiene al menos 1 aprobación de otro integrante.

Después de fusionar, el autor actualiza su copia con `git switch main` y `git pull`.
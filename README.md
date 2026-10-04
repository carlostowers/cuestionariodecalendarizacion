# Cuestionario sobre Calendarización

Temporada Escolar / Temporada Club. Estudio de MOVE sobre el cruce de carga entre la temporada escolar y la de clubes de voleibol juvenil en Puerto Rico.

## Archivos

| Archivo | Uso |
|---|---|
| `index.html` | Cuestionario público |
| `resultados.html` | Resultados privados con login (Supabase Auth) |
| `.nojekyll` | Evita que GitHub Pages procese el sitio con Jekyll |
| `_privado/` | SQL de Supabase. No se sube al repo (está en `.gitignore`) |

## Backend

- Supabase: proyecto `nvsprmqwbnbltvryhcrx`, tabla `public.survey_responses`
- El público solo puede insertar respuestas. Solo los correos en `public.survey_admins` pueden leerlas.
- Para autorizar a otra persona: crear su usuario en Authentication > Users e insertar su correo en `survey_admins`.

## Publicar en GitHub Pages

1. Crear el repositorio y subir el contenido de esta carpeta (sin `_privado/`).
2. Settings > Pages > Source: Deploy from a branch, rama `main`, carpeta `/ (root)`.
3. Para el subdominio: Settings > Pages > Custom domain, y crear el registro CNAME en el DNS apuntando a `<usuario>.github.io`.

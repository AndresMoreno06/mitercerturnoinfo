# Sitio público de Mi Tercer Turno

Esta carpeta es lo que se publica en GitHub Pages: la política de privacidad y la página
"Cómo eliminar tu cuenta" (las dos URLs que pide Google Play).

**No se edita a mano.** Se genera con `node scripts/generar-sitio.mjs` desde el texto de la app
(`src/features/configuracion/politica-privacidad.json`), para que app y sitio digan lo mismo.

## Publicar por primera vez

1. En GitHub (cuenta AndresMoreno06): **New repository** → nombre `mitercerturnoinfo` → **Public** → Create.
2. Sube el CONTENIDO de esta carpeta a la raíz del repositorio (`index.html`, `privacidad/`,
   `eliminar-cuenta/` y `.nojekyll`). Con la web: *Add file → Upload files*, arrastrando todo
   (el archivo `.nojekyll` está oculto y es opcional: si no lo subes, el sitio funciona igual) y
   *Commit changes*.
3. En el repositorio: **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   rama `main`, carpeta `/ (root)` → Save.
4. En 1 o 2 minutos quedará disponible en:
   - https://andresmoreno06.github.io/mitercerturnoinfo/privacidad/
   - https://andresmoreno06.github.io/mitercerturnoinfo/eliminar-cuenta/

## Actualizar el texto

1. Editar `src/features/configuracion/politica-privacidad.json` (y la fecha `updatedAt`).
2. Ejecutar `node scripts/generar-sitio.mjs`.
3. Volver a subir los archivos cambiados al repositorio.

Si cambia el usuario de GitHub o el nombre del repositorio, actualizar `SITIO_URL` en
`src/constants/sitio.ts` (la app lo usa en el enlace del registro).

Este `LEEME.md` es solo para ti: no hace falta subirlo al repositorio.

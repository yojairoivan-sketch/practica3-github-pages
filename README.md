# Práctica 3 — Automatización de página web con GitHub Pages

Electiva 2 · ITLA · Yojairo Rodriguez

Página "Hola Mundo" que se despliega automáticamente en GitHub Pages cada vez que se hace push a `main`.

- **Página:** https://yojairoivan-sketch.github.io/practica3-github-pages/
- **Repositorio:** https://github.com/yojairoivan-sketch/practica3-github-pages

## Cómo funciona

1. `index.html` es la página.
2. `.github/workflows/deploy.yml` es un workflow de GitHub Actions que, en cada push a `main`:
   - descarga el repositorio (`actions/checkout`),
   - empaqueta los archivos como artefacto de Pages (`actions/upload-pages-artifact`),
   - lo publica en GitHub Pages (`actions/deploy-pages`).
3. En *Settings → Pages* el origen está configurado como **GitHub Actions**.

Para actualizar la página basta con editar `index.html`, hacer commit y `git push`; el sitio se actualiza solo en ~1 minuto.

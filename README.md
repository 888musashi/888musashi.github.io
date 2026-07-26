# 888musashi — sitio web estático

Web personal de ajedrez (gratis, $0 en hosting). HTML + CSS puro, sin frameworks.

## Estructura
- `index.html` — home: hero, link hub (9 redes), embeds en vivo, newsletter, coaching, blog
- `assets/styles.css` — tema oscuro ajedrez, responsive
- `blog/index.html` — índice del blog
- `blog/*.html` — posts

## Antes de publicar (edición manual)
1. Cambia los 9 links de redes por tus handles reales en `index.html` (busca `888musashi`).
2. Cambia `channel=888musashi` en el script al final de `index.html` por tu usuario de Twitch.
3. Cambia `channel=UCXXXXXXXXXXXXXX` del embed de YouTube por tu ID de canal.
4. Newsletter: cambia el `action` del `<form>` por tu Beehiiv / ConvertKit / Formspree.

## Publicar — Opción A: Netlify (1 min, sin cuenta dev)
1. Ve a https://app.netlify.com/drop
2. Arrastra la carpeta `888musashi/` al recuadro.
3. Listo. Te dan una URL `*.netlify.app`. (Opcional: conectas tu dominio propio después.)

## Publicar — Opción B: GitHub Pages (dueño del código)
1. Crea un repo en GitHub (ej. `888musashi.github.io` para dominio raíz, o cualquiera).
2. Sube esta carpeta:
   ```
   git init
   git add -A
   git commit -m "sitio 888musashi"
   git remote add origin https://github.com/TU_USUARIO/TU_REPO.git
   git push -u origin main
   ```
3. En el repo: Settings → Pages → Source: `main` / root → Save.
4. URL: `https://TU_USUARIO.github.io/TU_REPO/` (o `https://TU_USUARIO.github.io` si el repo se llama `TU_USUARIO.github.io`).

## Local
```
python -m http.server 8099
# abre http://localhost:8099
```
Los embeds en vivo solo cargan en el dominio real (no en localhost).

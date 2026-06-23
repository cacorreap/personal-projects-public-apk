# 📱 personal-projects-public-apk

Hub de descargas (GitHub Pages) con las **APKs de mis proyectos personales** para
Android, organizadas por proyecto.

🔗 **Página:** https://cacorreap.github.io/personal-projects-public-apk/

## Estructura

```
index.html            ← la página de descargas (lista de proyectos)
apps/
  kidnanzas/
    kidnanzas.apk      ← APK chica: vive en el repo
    preview.png        ← captura para la tarjeta
  cooksnap/
    icon.png           ← ícono (la APK enlaza al Release de cooksnap-public)
  mentirosamente/
    icon.png           ← ícono (la APK enlaza al Release de mentirosamente-public)
```

Cada proyecto es una tarjeta definida en el array `PROJECTS` dentro de
[`index.html`](index.html). El campo `apk` puede ser un archivo local
(`apps/<slug>/x.apk`) **o** una URL de GitHub Release.

## Agregar un proyecto nuevo

1. Copia su ícono a `apps/<slug>/icon.png` (o usa un `emoji`).
2. Agrega un objeto al array `PROJECTS` en `index.html` con su `apk`:
   - APK **< 100 MB**: cópiala a `apps/<slug>/` y usa la ruta local.
   - APK **≥ 100 MB**: súbela como **GitHub Release** y usa la URL
     `releases/latest/download/<archivo>.apk`.
3. `git add . && git commit -m "Agrega <proyecto>" && git push`.

La página se actualiza sola unos segundos después del push.

## Notas

- Las APKs van firmadas con llave debug: sirven para instalar directamente
  (sideload), no necesariamente para Google Play.
- GitHub bloquea archivos > 100 MB; por eso CookSnap (116 MB) se enlaza a su
  Release en vez de vivir en este repo.

# 📱 personal-projects-public-apk

Hub de descargas (GitHub Pages) con las **APKs de mis proyectos personales** para
Android, organizadas por proyecto.

🔗 **Página:** https://cacorreap.github.io/personal-projects-public-apk/

## Estructura

```
index.html            ← la página de descargas (lista de proyectos)
apps/
  kidnanzas/
    kidnanzas.apk      ← el instalable
    preview.png        ← captura para la tarjeta
  cooksnap/            ← (próximamente)
  mentirosamente/      ← (próximamente)
```

## Agregar un proyecto nuevo

1. Crea la carpeta `apps/<slug>/` y copia ahí su `.apk` (y un `preview.png` opcional).
2. Abre [`index.html`](index.html) y agrega un objeto al array `PROJECTS` (hay
   ejemplos comentados para Cooksnap y Mentirosamente).
3. `git add . && git commit -m "Agrega <proyecto>" && git push`.

La página se actualiza sola unos segundos después del push.

## Notas

- Las APKs van firmadas con llave debug: sirven para instalar directamente
  (sideload), no para Google Play.
- GitHub limita cada archivo a 100 MB. Si una APK pesa más, conviene usar
  **GitHub Releases** o Git LFS y enlazar desde aquí.

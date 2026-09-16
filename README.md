# MAS CLIENTES — Sitio web (masclientes.app)

Sitio landing estatico listo para GitHub Pages.

## Estructura

```
masclientes-site/
├── index.html          <- la pagina completa (logos van incrustados dentro)
├── CNAME               <- tu dominio personalizado (masclientes.app)
├── assets/
│   ├── mock_panel.png  <- captura de la app: panel de conversaciones
│   ├── mock_alert.png  <- captura de la app: alerta de venta
│   ├── mock_stats.png  <- captura de la app: estadisticas
│   └── qr_install.png  <- QR oficial de descarga (instalar.masclientes.app)
└── README.md
```

## Publicar en GitHub Pages con tu dominio (CNAME)

1. Crea un repositorio en GitHub, por ejemplo `masclientes-app`.
2. Sube **todo el contenido de esta carpeta** a la rama `main`
   (por la web: "Add file > Upload files", o con git: `git add . && git commit -m "site" && git push`).
3. Ve a **Settings > Pages**:
   - Source: **Deploy from a branch**
   - Branch: `main` / `/ (root)` > **Save**
4. En tu proveedor de dominio (donde compraste masclientes.app), configura los DNS:
   - Tipo **A** → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Tipo **CNAME** → `TU-USUARIO.github.io`
   (si usas el dominio raiz `masclientes.app` solo registros A; si usas `www`, el CNAME)
5. Espera unos minutos y entra a https://masclientes.app
   GitHub detecta el archivo CNAME y activa HTTPS automatico
   (marca "Enforce HTTPS" en Settings > Pages cuando aparezca).

## Notas

- Para actualizar el sitio: edita `index.html` (o las imagenes en `assets/`)
  y vuelve a subir. GitHub Pages publica solo.
- El formulario de contacto es un `mailto:hola@joel.cafe`, no necesita backend.
- El boton 'Descargar la app' y el QR apuntan a https://instalar.masclientes.app (tu QR anexo en assets/qr_install.png).

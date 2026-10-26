# 🎮 GameStation Control

PWA para administrar salas de videojuegos: tiempo por estación (libre o fijo), mandos adicionales, snacks/consumos, cobro con resumen de cuenta e historial de ventas.

## Características
- Funciona **100 % sin conexión** (sin wifi ni datos) una vez abierta por primera vez.
- Instalable en Android, iPhone y PC (botón **Instalar** en el encabezado).
- Datos guardados en el dispositivo (`localStorage`).
- Tema claro / oscuro.

## Estructura
```
index.html        App completa (estilos, íconos y fuentes incrustados)
manifest.json     Configuración de la PWA
sw.js             Service worker (modo sin conexión)
icons/            Íconos de la app
.nojekyll         Para GitHub Pages
```

## Publicar en GitHub Pages
1. Sube todos estos archivos a la **raíz** del repositorio (rama `main`).
2. Ve a **Settings → Pages**.
3. En *Source* elige **Deploy from a branch**, rama `main`, carpeta `/ (root)` y guarda.
4. Abre la URL `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/` en Chrome y toca **Instalar**.

## Actualizar la app
Cuando modifiques `index.html`, cambia la versión en `sw.js`
(`const CACHE = 'gamestation-v9'` → `'gamestation-v10'`) para que los teléfonos descarguen la nueva versión.

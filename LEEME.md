# Álbum Figuritas: app instalable

Esta carpeta es la app completa. Súbela gratis a GitHub Pages, ábrela en Chrome y agrégala a la pantalla de inicio. Queda con su ícono, a pantalla completa y funciona sin internet.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La app |
| `manifest.webmanifest` | Nombre, ícono y colores al instalarla |
| `sw.js` | Hace que funcione sin internet |
| `icons/` | Íconos de la app |

## 1. Subirla a GitHub Pages (una sola vez, desde el navegador)

1. Entra a <https://github.com> e inicia sesión (o crea una cuenta gratis).
2. Arriba a la derecha toca **+ → New repository**.
   - Nombre: `figuritas` (o el que quieras).
   - Déjalo en **Public**. GitHub Pages gratis necesita repositorio público.
   - Toca **Create repository**.
3. En la página del repositorio nuevo toca **uploading an existing file**.
4. Arrastra **todo el contenido de esta carpeta** (`index.html`, `manifest.webmanifest`, `sw.js` y la carpeta `icons`). Que `index.html` quede en la raíz, no dentro de otra carpeta.
5. Abajo toca **Commit changes**.
6. Ve a **Settings → Pages**. En *Branch* elige `main` y carpeta `/ (root)`, y toca **Save**.
7. Espera 1–2 minutos. Tu app queda en:
   `https://TU-USUARIO.github.io/figuritas/`

## 2. Instalarla en el celular

**Android (Chrome):** abre el enlace → menú ⋮ → **Agregar a pantalla de inicio** (o **Instalar app**).

**iPhone (Safari):** abre el enlace → botón compartir → **Agregar a inicio**.

Ábrela una vez con internet para que se guarde. Después funciona sin conexión.

## 3. Pasar tus datos desde la versión de Claude

Los datos se guardan en cada navegador por separado, así que la app instalada empieza vacía (con Anime World en 0 y la colección de ejemplo).

1. En la versión de Claude: **Mis colecciones → ícono de importar/exportar → Copiar JSON**.
2. En la app instalada: **Importar JSON**, pega el texto e importa.
3. Si ya no la usas, borra las colecciones repetidas desde Configurar.

## 4. Actualizar la app más adelante

1. En GitHub, abre `index.html` → ícono del lápiz, o súbelo de nuevo con **Add file → Upload files**.
2. Abre `sw.js` y cambia `figuritas-v1` por `figuritas-v2` (luego v3, etc.). Así los celulares bajan la versión nueva.
3. **Commit changes.** La próxima vez que abras la app con internet se actualiza sola. A veces hay que cerrarla y abrirla dos veces.

Tus figuritas no se pierden al actualizar.

## Respaldo

Tus datos viven en el navegador del celular. Si borras los datos de Chrome o desinstalas la app, se pierden. De vez en cuando entra a **Importar y exportar → Descargar archivo .json** y guarda ese archivo (en Drive o enviándotelo por WhatsApp).

## Diferencias con la versión de Claude

- **Enviar…** en la hoja de compartir abre el menú del celular, para mandar la lista directo a WhatsApp.
- **Descargar archivo .json** guarda el respaldo como archivo.

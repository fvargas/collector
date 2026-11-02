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

## Plantillas (para que otros creen su álbum en un toque)

La carpeta `plantillas/` del repositorio guarda álbumes listos para usar. En la app, **Nueva colección → Desde una plantilla** muestra todas las que estén ahí.

```
plantillas/
  index.json          ← lista de plantillas
  anime-world.json    ← una plantilla
```

`index.json` solo lista los archivos:

```json
{ "plantillas": ["anime-world.json", "mundial-2026.json"] }
```

### Crear o actualizar una plantilla

1. En la app, arma o ajusta el álbum como quieres que lo reciban los demás.
2. ⋮ de la colección → **Exportar configuración** → marca **Exportar como plantilla** → **Descargar archivo .json**. El archivo ya sale con el nombre correcto y con la versión subida en 1.
3. En GitHub, entra a la carpeta `plantillas/` → **Add file → Upload files** → sube el archivo (reemplaza el anterior) → **Commit changes**.
4. Si es una plantilla **nueva**, abre `plantillas/index.json` → lápiz ✎ → agrega su nombre a la lista → **Commit changes**.

No hace falta tocar `sw.js` para actualizar plantillas.

### Qué ven los demás

- Quien creó su álbum desde la plantilla ve **"Nueva versión"** en la tarjeta de la colección cuando subes una versión mayor.
- Con ⋮ → **Actualizar plantilla** reciben tus cambios (secciones, variantes, brillos) y conservan sus figuritas marcadas, su nombre y su meta.
- Si borras una sección o un número de la plantilla, las figuritas marcadas ahí se pierden al actualizar. La app avisa cuántas.
- Para no romper nada, no cambies el nombre de las secciones entre versiones si puedes evitarlo.

## Respaldo

Tus datos viven en el navegador del celular. Si borras los datos de Chrome o desinstalas la app, se pierden. De vez en cuando entra a **Importar y exportar → Descargar archivo .json** y guarda ese archivo (en Drive o enviándotelo por WhatsApp).

## Diferencias con la versión de Claude

- **Enviar…** en la hoja de compartir abre el menú del celular, para mandar la lista directo a WhatsApp.
- **Descargar archivo .json** guarda el respaldo como archivo.

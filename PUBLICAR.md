# Cómo publicar AgroApp Web en GitHub Pages

## Archivos generados
- `index.html` — Página principal / landing page
- `politica-privacidad.html` — Política de privacidad (URL para Google Play)
- `style.css` — Estilos compartidos
- `icon.png` — Icono de la app

---

## Pasos para publicar (método más sencillo)

### 1. Crear un repositorio en GitHub
1. Ve a https://github.com/new
2. Nombre del repositorio: `agroapp-web`
   (la URL resultante será `https://TU_USUARIO.github.io/agroapp-web/`)
3. Visibilidad: **Public** (obligatorio para GitHub Pages gratuito)
4. Haz clic en "Create repository"

### 2. Subir los archivos
En la página del repositorio recién creado, haz clic en **"uploading an existing file"**
y arrastra estos cuatro archivos:
- `index.html`
- `politica-privacidad.html`
- `style.css`
- `icon.png`

Haz clic en "Commit changes".

### 3. Activar GitHub Pages
1. Ve a **Settings** → **Pages** (en el menú lateral)
2. En "Branch", selecciona `main` y la carpeta `/ (root)`
3. Haz clic en **Save**

En unos 2–5 minutos la web estará disponible en:
```
https://TU_USUARIO.github.io/agroapp-web/
```

---

## URL para Google Play / Google Payments

Una vez publicada, las URLs que debes usar son:

| Campo                      | URL                                                        |
|----------------------------|------------------------------------------------------------|
| Sitio web de la app        | `https://TU_USUARIO.github.io/agroapp-web/`               |
| Política de privacidad     | `https://TU_USUARIO.github.io/agroapp-web/politica-privacidad.html` |

---

## Alternativa: si ya tienes el proyecto en un repositorio Git
Puedes crear una rama `gh-pages` y publicar solo la carpeta `web/`:
```bash
# Desde la raíz del proyecto agrogest
git subtree push --prefix web origin gh-pages
```
Y en GitHub Pages elegir la rama `gh-pages`.

---

## Nota sobre el badge de Google Play
El archivo `index.html` incluye el enlace al badge de Google Play apuntando a
`https://play.google.com/store` — cuando tengas la URL real de tu app, reemplaza
esa línea por la URL exacta de la ficha de tu aplicación.

# Cómo publicar en GitHub Pages

## Estructura del repo
```
inspection-viewer/
├── index.html
├── models/
│   └── Francel_aerogenerador.glb   ← ya está aquí
├── images/
│   ├── thermal/                    ← 30 frames térmicos, ya están
│   └── rgb/                        ← 9 frames RGB anotados, ya están
└── DEPLOY.md
```

## Pasos (5 minutos)

1. **Crea un repo en GitHub**
   - Ve a https://github.com/new
   - Nombre: `aion-inspection-gamesa-g52` (o el que quieras)
   - Visibilidad: **Public** (GitHub Pages gratis solo funciona en repos públicos)

2. **Sube esta carpeta completa**
   ```
   cd C:\Users\franc\AION\inspection-viewer
   git init
   git add .
   git commit -m "Initial inspection viewer"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/aion-inspection-gamesa-g52.git
   git push -u origin main
   ```

3. **Activa GitHub Pages**
   - En el repo → Settings → Pages
   - Source: **Deploy from a branch**
   - Branch: `main` / `/ (root)`
   - Guarda

4. **Tu URL estará disponible en ~2 minutos:**
   ```
   https://TU_USUARIO.github.io/aion-inspection-gamesa-g52/
   ```

> ⚠️ El GLB pesa 13 MB — GitHub Pages lo sirve bien, pero la carga inicial
> tarda ~3-5 seg en conexión normal. Si quieres más velocidad, sube el GLB
> a Cloudflare R2 o cualquier CDN y cambia la ruta en index.html.

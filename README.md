# Scrapin-OCC Frontend

Frontend para el scraper de vacantes de OCC.com.mx

## Configuración para Vercel

### 1. Actualizar URLs del Backend

Antes de desplegar, debes actualizar las URLs del backend en los siguientes archivos:

**En `index.html` línea ~52:**
```javascript
const API_BASE_URL = window.location.hostname === 'localhost' 
    ? 'http://localhost:3000/api'
    : 'https://TU-BACKEND-RENDER-APP.onrender.com/api'; // ⬅️ Cambiar esta URL
```

**En `vacantes.html` línea ~88:**
```javascript
const API_BASE_URL = window.location.hostname === 'localhost' 
    ? 'http://localhost:3000/api'
    : 'https://TU-BACKEND-RENDER-APP.onrender.com/api'; // ⬅️ Cambiar esta URL
```

### 2. Despliegue en Vercel

1. Sube este directorio `frontend/` a un repositorio de GitHub
2. Ve a [Vercel.com](https://vercel.com) y crea una cuenta
3. Conecta tu repositorio de GitHub
4. Importa el proyecto
5. Configura:
   - **Framework Preset**: Other
   - **Build Command**: (dejar vacío)
   - **Output Directory**: (dejar vacío)
   - **Install Command**: npm install

### 3. Estructura de Archivos

```
frontend/
├── index.html          # Página principal
├── vacantes.html       # Página de resultados
├── img/               # Imágenes del equipo
├── package.json       # Configuración NPM
├── vercel.json        # Configuración de Vercel
└── README.md          # Este archivo
```

### 4. URLs de la Aplicación

- **Búsqueda**: `/` o `/index.html`
- **Resultados**: `/vacantes` o `/vacantes.html`

## Desarrollo Local

```bash
npm install
npm run dev
```

Esto iniciará un servidor local en `http://localhost:3000`

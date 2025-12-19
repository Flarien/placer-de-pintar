# 🎨 Portfolio Norma Luján Brignoni

> Sitio web portfolio para artista plástica - Galería de obras, filtros por categoría y sección de contacto

[![Astro](https://img.shields.io/badge/Astro-4.0-FF5D01?logo=astro&logoColor=white)](https://astro.build)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📖 Descripción

Portfolio web minimalista y elegante para la artista plástica **Norma Luján Brignoni**. El sitio destaca las obras de la artista a través de una galería interactiva con filtros por categoría, diseño responsivo y animaciones suaves.

### ✨ Características

- 🖼️ **Galería interactiva** con filtros por categoría (Cuadros, Tejas, Murales, Retratos)
- 🎭 **Modal de visualización** para ver obras en detalle
- 📱 **Diseño responsivo** - se adapta perfectamente a móviles y tablets
- ⚡ **Performance optimizada** - sitio estático generado con Astro
- 🎨 **Animaciones suaves** - scroll animations, hover effects, transiciones
- 🎯 **SEO friendly** - HTML semántico y metadatos optimizados
- 🌐 **Multilingüe preparado** - estructura lista para i18n

## 🚀 Tech Stack

- [Astro](https://astro.build) - Framework para sitios estáticos
- HTML5 / CSS3 (Grid, Flexbox, Custom Properties)
- JavaScript Vanilla (Intersection Observer API)
- Tipografía: Georgia (serif)

## 📁 Estructura del Proyecto

```
portfolio-norma/
├── public/
│   ├── images/               # Imágenes de las obras
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── Header.astro      # Navegación principal
│   │   ├── Hero.astro        # Hero section
│   │   ├── Gallery.astro     # Galería con filtros
│   │   ├── About.astro       # Biografía
│   │   ├── Contact.astro     # Información de contacto
│   │   └── Footer.astro      # Footer
│   ├── layouts/
│   │   └── Layout.astro      # Layout base
│   ├── pages/
│   │   └── index.astro       # Página principal
│   └── data/
│       └── obras.json        # (opcional) Datos de obras
└── package.json
```

## 🛠️ Instalación

### Prerrequisitos

- Node.js 18+ 
- npm o pnpm

### Pasos

1. **Clonar el repositorio**
```bash
git clone https://github.com/tu-usuario/portfolio-norma-lujan.git
cd portfolio-norma-lujan
```

2. **Instalar dependencias**
```bash
npm install
```

3. **Agregar las imágenes**
   - Colocar las fotos de las obras en `/public/images/`
   - Actualizar las rutas en `src/components/Gallery.astro`

4. **Iniciar servidor de desarrollo**
```bash
npm run dev
```

El sitio estará disponible en `http://localhost:4321`

## 📝 Scripts Disponibles

```bash
npm run dev          # Inicia servidor de desarrollo
npm run build        # Genera build de producción
npm run preview      # Preview del build
npm run astro        # Comandos CLI de Astro
```

## 🎨 Personalización

### Colores

Editar variables CSS en `src/layouts/Layout.astro`:

```css
:root {
  --primary: #2d2d2d;    /* Color principal (texto) */
  --accent: #8b6f47;     /* Color acento (dorado/tierra) */
  --light: #f8f8f8;      /* Fondo claro */
  --white: #ffffff;      /* Blanco puro */
}
```

### Obras de la galería

**Opción 1**: Editar directamente en `Gallery.astro`

```astro
const obras = [
  { 
    id: 1, 
    title: "Título de la obra", 
    category: "cuadros", 
    technique: "Técnica utilizada", 
    image: "/images/obra-1.jpg" 
  },
  // ... más obras
];
```

**Opción 2**: Crear archivo `src/data/obras.json`

```json
[
  {
    "id": 1,
    "title": "Tigre Hiperrealista",
    "category": "cuadros",
    "technique": "Acrílico sobre tela",
    "image": "/images/tigre.jpg"
  }
]
```

Y luego importar en `Gallery.astro`:
```astro
---
import obras from '../data/obras.json';
---
```

### Tipografía

Cambiar `'Georgia'` por otra fuente en `Layout.astro`:

```css
body {
  font-family: 'Tu-Fuente', serif;
}
```

Si usás Google Fonts, agregar en `<head>` del Layout.

## 🚀 Deployment

### Netlify

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start)

```bash
npm run build
# Subir carpeta /dist a Netlify
```

### Vercel

```bash
npm install -g vercel
vercel
```

### Cloudflare Pages

1. Conectar repositorio de GitHub
2. Build command: `npm run build`
3. Output directory: `dist`

## 📸 Screenshots

### Desktop
![Desktop View](screenshots/desktop.png)

### Mobile
![Mobile View](screenshots/mobile.png)

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add: nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

## 👤 Autora

**Norma Luján Brignoni**
- Artista Plástica
- Email: lujanbrig@gmail.com
- Instagram: [@placer.de.pintar](https://instagram.com/placer.de.pintar)
- Facebook: [@el.placer.de.pintar](https://instagram.com/el.placer.de.pintar)

**Desarrollado por:** [Flavia S. Briglia]
- GitHub: [@Flarien](https://github.com/Flarien)

## 🙏 Agradecimientos

- Diseño inspirado en portfolios minimalistas de Behance y Dribbble
- Tipografía Georgia por su elegancia clásica
- Paleta de colores tierra que complementa las obras de arte
- Íconos de contacto: [@icons8](https://icons8.com) 

---

⭐ Si te gustó el proyecto, considerá darle una estrella en GitHub

*Hecho con ❤️ y [Astro](https://astro.build)*
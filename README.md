# Heliana Studio - Landing Page

Landing page moderna y responsive para un estudio de arquitectura, desarrollada con HTML, CSS y JavaScript vanilla (sin frameworks).

## Características

- ✨ Diseño moderno y profesional
- 📱 Totalmente responsive (móvil, tablet, desktop)
- 🎨 Animaciones suaves y transiciones
- 🚀 Sin dependencias de frameworks (HTML, CSS, JS puro)
- ♿ Navegación accesible con menú hamburguesa para móviles
- 📧 Formulario de contacto funcional
- 🎯 4 páginas completas: Home, Proyectos, Acerca, Contacto

## Estructura del Proyecto

```
heliana-studio-landing/
├── index.html              # Página principal
├── proyectos.html          # Galería de proyectos
├── acerca.html             # Información de la empresa
├── contacto.html           # Formulario de contacto
├── css/
│   └── styles.css          # Estilos CSS
├── js/
│   └── main.js             # JavaScript principal
├── assets/
│   └── images/             # Carpeta para imágenes
└── README.md               # Este archivo
```

## Cómo Usar

### Opción 1: Abrir directamente en el navegador

1. Descarga o clona este repositorio
2. Abre el archivo `index.html` en tu navegador web
3. Navega entre las diferentes páginas usando el menú

### Opción 2: Usar un servidor local

Para una mejor experiencia de desarrollo, puedes usar un servidor local:

**Con Python 3:**
```bash
python -m http.server 8000
```

**Con Node.js (http-server):**
```bash
npx http-server
```

Luego abre tu navegador en `http://localhost:8000`

## Personalización

### Cambiar Colores

Los colores se definen en variables CSS en `css/styles.css`. Modifica estas variables para cambiar la paleta de colores:

```css
:root {
    --primary-color: #2c3e50;      /* Color principal */
    --secondary-color: #e67e22;    /* Color secundario */
    --accent-color: #3498db;       /* Color de acento */
    --text-color: #333;            /* Color del texto */
    --light-bg: #f8f9fa;          /* Fondo claro */
    --white: #ffffff;              /* Blanco */
}
```

### Agregar Imágenes Reales

1. Coloca tus imágenes en la carpeta `assets/images/`
2. Modifica los elementos con clase `.project-image` y `.about-image` en los archivos HTML
3. Ejemplo:

```html
<!-- Reemplaza esto: -->
<div class="project-image">
    <span>Casa Moderna Vista al Mar</span>
</div>

<!-- Por esto: -->
<div class="project-image">
    <img src="assets/images/proyecto1.jpg" alt="Casa Moderna Vista al Mar">
</div>
```

### Modificar Contenido

- **Nombre del estudio**: Busca "Heliana Studio" en todos los archivos HTML y reemplázalo
- **Proyectos**: Edita el contenido en `proyectos.html`
- **Información de la empresa**: Modifica `acerca.html`
- **Datos de contacto**: Actualiza la información en `contacto.html`

### Conectar el Formulario de Contacto

El formulario actualmente solo muestra un mensaje de éxito. Para conectarlo a un backend:

1. Abre `js/main.js`
2. Busca la función del formulario (línea ~40)
3. Reemplaza el `console.log` con una llamada a tu API:

```javascript
// Ejemplo con fetch API
fetch('https://tu-api.com/contacto', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify(formData)
})
.then(response => response.json())
.then(data => {
    // Mostrar mensaje de éxito
    successMessage.classList.add('show');
})
.catch(error => {
    console.error('Error:', error);
});
```

## Funcionalidades JavaScript

- **Menú Hamburguesa**: Se activa automáticamente en dispositivos móviles
- **Formulario de Contacto**: Validación y mensaje de confirmación
- **Animaciones al Scroll**: Los elementos aparecen suavemente al hacer scroll
- **Scroll Suave**: Navegación suave entre secciones

## Navegadores Compatibles

- Chrome (últimas 2 versiones)
- Firefox (últimas 2 versiones)
- Safari (últimas 2 versiones)
- Edge (últimas 2 versiones)
- Opera (últimas 2 versiones)

## Responsive Breakpoints

- **Desktop**: 1200px y superior
- **Tablet**: 768px - 1199px
- **Móvil**: Hasta 767px

## Licencia

Este proyecto es de código abierto y está disponible para uso personal y comercial.

## Soporte

Para preguntas o problemas, por favor abre un issue en el repositorio.

---

Desarrollado con ❤️ para Heliana Studio

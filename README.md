# Heliana Studio - Architectural Studio Website

A modern, lightweight, and multilingual website for Heliana Architectural Studio built with Astro.

## Features

- ✨ Modern and professional design
- 📱 Fully responsive (mobile, tablet, desktop)
- 🌐 Multi-language support (English and Spanish)
- 🚀 Lightning-fast performance with Astro
- 🎨 Smooth animations and transitions
- ♿ Accessible navigation with hamburger menu for mobile
- 📧 Functional contact form
- 🎯 4 complete pages: Home, Projects, About, Contact

## Tech Stack

- **Framework**: Astro 4.0
- **Internationalization**: astro-i18next + i18next
- **Styling**: Pure CSS with CSS variables
- **JavaScript**: Minimal, only for interactive features

## Project Structure

```
heliana-studio-landing/
├── public/
│   └── locales/           # Translation files
│       ├── es/            # Spanish translations
│       └── en/            # English translations
├── src/
│   ├── components/        # Reusable components
│   │   └── Navigation.astro
│   ├── layouts/           # Page layouts
│   │   └── Layout.astro
│   ├── pages/             # Page routes
│   │   ├── index.astro    # Home page
│   │   ├── proyectos.astro # Projects page
│   │   ├── acerca.astro   # About page
│   │   └── contacto.astro # Contact page
│   └── styles/            # Global styles
│       └── global.css
├── astro.config.mjs       # Astro configuration
└── package.json           # Dependencies
```

## Getting Started

### Prerequisites

- Node.js 18 or higher
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd heliana-studio-landing
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

The site will be available at `http://localhost:4321`

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run astro` - Run Astro CLI commands

## Multi-Language Support

The website supports both Spanish (default) and English:

- **Spanish**: `http://localhost:4321/` (default)
- **English**: `http://localhost:4321/en/`

### Adding or Editing Translations

Translation files are located in `public/locales/`:

- Spanish: `public/locales/es/*.json`
- English: `public/locales/en/*.json`

Each page has its own translation file:
- `common.json` - Navigation, footer, and shared content
- `home.json` - Home page content
- `projects.json` - Projects page content
- `about.json` - About page content
- `contact.json` - Contact page content

### Language Switcher

The language switcher is included in the navigation bar and allows users to seamlessly switch between Spanish and English.

## Customization

### Changing Colors

Colors are defined as CSS variables in `src/styles/global.css`:

```css
:root {
    --primary-color: #2c3e50;      /* Main color */
    --secondary-color: #e67e22;    /* Secondary color */
    --accent-color: #3498db;       /* Accent color */
    --text-color: #333;            /* Text color */
    --light-bg: #f8f9fa;          /* Light background */
    --white: #ffffff;              /* White */
}
```

### Adding Real Images

1. Place your images in the `public/` folder (e.g., `public/images/`)
2. Update the project cards and other image placeholders in the page files
3. Example:

```astro
<!-- Replace placeholder: -->
<div class="project-image">
    <span>Project Title</span>
</div>

<!-- With real image: -->
<div class="project-image">
    <img src="/images/project1.jpg" alt="Project Title">
</div>
```

### Connecting the Contact Form

The contact form currently shows a success message. To connect it to a backend:

1. Open `src/pages/contacto.astro`
2. Find the `<script>` section
3. Replace the form submission logic with your API call:

```javascript
// Example with fetch API
fetch('https://your-api.com/contact', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify(formData)
})
.then(response => response.json())
.then(data => {
    successMessage.classList.add('show');
})
.catch(error => {
    console.error('Error:', error);
});
```

## Building for Production

To create a production build:

```bash
npm run build
```

The built files will be in the `dist/` directory, ready to be deployed to any static hosting service:

- Netlify
- Vercel
- GitHub Pages
- Cloudflare Pages
- AWS S3
- Any web server

## Deployment

### Netlify

1. Connect your repository to Netlify
2. Build command: `npm run build`
3. Publish directory: `dist`

### Vercel

1. Import your repository on Vercel
2. Framework preset: `Astro`
3. Deploy!

### GitHub Pages

1. Update `astro.config.mjs` with your site URL
2. Run `npm run build`
3. Deploy the `dist/` folder

## Browser Support

- Chrome (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Edge (latest 2 versions)
- Opera (latest 2 versions)

## Responsive Breakpoints

- **Desktop**: 1200px and above
- **Tablet**: 768px - 1199px
- **Mobile**: Up to 767px

## Performance

Astro delivers exceptional performance:
- Static HTML generation
- Minimal JavaScript
- Optimized CSS
- Fast page loads
- SEO-friendly

## License

This project is open source and available for personal and commercial use.

## Support

For questions or issues, please open an issue in the repository.

---

Built with ❤️ using Astro for Heliana Studio

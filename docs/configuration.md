# Configuration Guide

Learn how to configure Max Docs to match your project's needs and branding.

## Basic Configuration

### Site Information

Update the basic site information in `index.html`:

```html
<!-- Page title (appears in browser tab) -->
<title>Your Project Name - Documentation</title>

<!-- Site logo/name in sidebar -->
<h1 class="logo">Your Project</h1>

<!-- Version number -->
<p class="version">v2.0.0</p>

<!-- GitHub repository link -->
<a href="https://github.com/yourusername/your-repo" class="github-link">
```

### Navigation Structure

The navigation is defined in the sidebar section. To modify the navigation:

```html
<div class="nav-section">
    <h3>Section Title</h3>
    <ul class="nav-list">
        <li><a href="#section-id" class="nav-link">Page Title</a></li>
        <li><a href="#another-section" class="nav-link">Another Page</a></li>
    </ul>
</div>
```

### Content Sections

Each navigation link should correspond to a content section:

```html
<section id="section-id" class="content-section">
    <h2>Section Title</h2>
    <p>Your content here...</p>
</section>
```

## Styling Configuration

### Color Scheme

Max Docs uses CSS custom properties for theming. Update these in `assets/styles.css`:

```css
:root {
    /* Primary colors */
    --primary-color: #2563eb;        /* Main brand color */
    --primary-light: #3b82f6;        /* Lighter shade */
    --primary-dark: #1d4ed8;         /* Darker shade */
    
    /* UI colors */
    --background-color: #ffffff;      /* Main background */
    --surface-color: #f8fafc;        /* Cards, sidebar */
    --border-color: #e2e8f0;         /* Borders */
    
    /* Text colors */
    --text-color: #1e293b;           /* Primary text */
    --text-muted: #64748b;           /* Secondary text */
    --text-light: #94a3b8;           /* Light text */
}
```

### Typography

Change the font family:

```css
:root {
    --font-family: 'Your Font', -apple-system, BlinkMacSystemFont, sans-serif;
    --font-mono: 'Your Mono Font', Monaco, 'Cascadia Code', monospace;
}
```

### Layout

Adjust the sidebar width and content max-width:

```css
:root {
    --sidebar-width: 300px;          /* Sidebar width */
    --content-max-width: 1200px;     /* Max content width */
}
```

## Advanced Configuration

### Custom Logo

Replace the text logo with an image:

```html
<div class="sidebar-header">
    <img src="assets/logo.png" alt="Your Project" class="logo-image">
    <p class="version">v2.0.0</p>
</div>
```

Add corresponding CSS:

```css
.logo-image {
    height: 40px;
    width: auto;
    margin-bottom: 0.25rem;
}
```

### Custom Favicon

Add a favicon in the `<head>` section:

```html
<link rel="icon" type="image/png" sizes="32x32" href="assets/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="assets/favicon-16x16.png">
```

### Analytics Integration

Add Google Analytics or other analytics services:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Search Functionality

While not included by default, you can add search functionality:

```html
<div class="search-container">
    <input type="text" id="search" placeholder="Search documentation...">
</div>
```

## Environment-Specific Configuration

### Development

For development, consider using a local server:

```bash
# Python 3
python -m http.server 8000

# Node.js
npx http-server

# PHP
php -S localhost:8000
```

### Production

For production deployment:

1. **Minify CSS/JS** for better performance
2. **Optimize images** in the assets folder
3. **Set up proper caching headers**
4. **Enable compression** (gzip/brotli)

### GitHub Pages

To deploy on GitHub Pages:

1. Push your code to a GitHub repository
2. Go to repository Settings
3. Navigate to Pages section
4. Select source branch (usually `main`)
5. Your site will be available at `https://username.github.io/repository-name`

## Troubleshooting

### Styles not loading
- Check that `assets/styles.css` exists
- Verify the CSS file path in `index.html`
- Ensure no syntax errors in CSS

### Navigation not working
- Check that JavaScript is enabled
- Verify section IDs match navigation hrefs
- Look for JavaScript console errors

### Mobile responsiveness issues
- Test with browser dev tools
- Check CSS media queries
- Verify viewport meta tag is present
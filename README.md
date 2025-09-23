# Max Docs

A modern, responsive documentation template for your projects. Max Docs provides a clean and professional interface for organizing and presenting project documentation with intuitive navigation and beautiful design.

## ✨ Features

- **📱 Responsive Design** - Works perfectly on desktop, tablet, and mobile devices
- **🎨 Modern UI** - Clean, professional design with carefully chosen typography and spacing
- **🚀 Easy to Use** - Simple HTML structure that's easy to customize and extend
- **💡 Syntax Highlighting** - Beautiful code blocks with Prism.js integration
- **📋 Organized Navigation** - Clear sidebar navigation with sections and subsections
- **🌙 Dark Mode Ready** - Built-in support for system dark mode preferences
- **♿ Accessible** - Proper semantic HTML and keyboard navigation support

## 🚀 Quick Start

1. **Clone the repository:**
   ```bash
   git clone https://github.com/maxvbuda/Max-docs.git
   cd Max-docs
   ```

2. **Open the documentation:**
   - Simply open `index.html` in your web browser
   - Or use a local development server for the best experience:
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js (with http-server)
   npx http-server
   
   # Using VS Code Live Server extension
   # Right-click on index.html and select "Open with Live Server"
   ```

3. **Start customizing:**
   - Edit the content sections in `index.html`
   - Modify styles in `assets/styles.css`
   - Add your own documentation content

## 📁 Project Structure

```
Max-docs/
├── assets/
│   └── styles.css          # Main stylesheet
├── docs/                   # Documentation files (optional)
├── index.html             # Main documentation page
└── README.md              # This file
```

## 🛠️ Customization

### Basic Configuration

Update these elements in `index.html`:

```html
<!-- Update the page title -->
<title>Your Project Name - Documentation</title>

<!-- Update the logo/brand name -->
<h1 class="logo">Your Project</h1>

<!-- Update the version -->
<p class="version">v2.0.0</p>

<!-- Update the GitHub link -->
<a href="https://github.com/yourusername/your-repo" class="github-link">
```

### Styling

The design uses CSS custom properties (variables) for easy theming. Modify these values in `assets/styles.css`:

```css
:root {
    --primary-color: #2563eb;      /* Main brand color */
    --secondary-color: #64748b;    /* Secondary text color */
    --background-color: #ffffff;   /* Main background */
    --text-color: #1e293b;        /* Primary text color */
    /* ... more variables available */
}
```

### Adding New Sections

To add a new section to your documentation:

1. **Add navigation link** in the sidebar:
   ```html
   <li><a href="#your-section" class="nav-link">Your Section</a></li>
   ```

2. **Add content section** in the main content area:
   ```html
   <section id="your-section" class="content-section">
       <h2>Your Section Title</h2>
       <p>Your content here...</p>
   </section>
   ```

3. The JavaScript handles the navigation automatically!

## 🎨 Content Components

Max Docs includes several pre-styled components:

### Callout Boxes
```html
<div class="callout info">
    <strong>💡 Tip:</strong> Your helpful tip here.
</div>
```

Available types: `info`, `warning`, `danger`, `success`

### Feature Cards
```html
<div class="feature-grid">
    <div class="feature-card">
        <h3>🚀 Feature Title</h3>
        <p>Feature description</p>
    </div>
</div>
```

### Code Blocks
```html
<pre><code class="language-javascript">
// Your code here
function example() {
    return "Hello, World!";
}
</code></pre>
```

### Tables
```html
<div class="table-wrapper">
    <table>
        <thead>
            <tr><th>Column 1</th><th>Column 2</th></tr>
        </thead>
        <tbody>
            <tr><td>Data 1</td><td>Data 2</td></tr>
        </tbody>
    </table>
</div>
```

## 🌐 Browser Support

Max Docs works in all modern browsers:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 📱 Mobile Experience

The template is fully responsive and provides an excellent experience on mobile devices with:
- Collapsible navigation
- Touch-friendly interface
- Optimized typography for small screens
- Fast loading times

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 💖 Acknowledgments

- Typography powered by [Inter](https://rsms.me/inter/)
- Syntax highlighting by [Prism.js](https://prismjs.com/)
- Icons from [Heroicons](https://heroicons.com/)

## 📞 Support

If you have questions or need help:

- 📧 Email: [your-email@example.com](mailto:your-email@example.com)
- 🐛 Issues: [GitHub Issues](https://github.com/maxvbuda/Max-docs/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/maxvbuda/Max-docs/discussions)

---

**Happy documenting! 📚✨**
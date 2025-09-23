# Customization Guide

Learn how to customize Max Docs to create a unique documentation experience for your project.

## Content Customization

### Writing Effective Documentation

#### Structure Your Content
- **Start with an overview** - Explain what your project does
- **Provide quick start instructions** - Help users get running fast  
- **Include examples** - Show real code and use cases
- **Add troubleshooting** - Address common issues

#### Use Clear Headings
```html
<h2>Main Section</h2>
<h3>Subsection</h3>
<h4>Details</h4>
```

#### Write Scannable Content
- Use bullet points for lists
- Keep paragraphs short (2-3 sentences)
- Highlight important information
- Use code blocks for examples

### Content Components

#### Callout Boxes
Perfect for tips, warnings, and important information:

```html
<!-- Info callout -->
<div class="callout info">
    <strong>💡 Tip:</strong> This is helpful information.
</div>

<!-- Warning callout -->
<div class="callout warning">
    <strong>⚠️ Warning:</strong> Be careful with this.
</div>

<!-- Success callout -->
<div class="callout success">
    <strong>✅ Success:</strong> You did it right!
</div>

<!-- Error callout -->
<div class="callout danger">
    <strong>🚫 Error:</strong> Something went wrong.
</div>
```

#### Feature Cards
Great for showcasing features or benefits:

```html
<div class="feature-grid">
    <div class="feature-card">
        <h3>🚀 Fast Performance</h3>
        <p>Lightning-fast loading times with optimized code.</p>
    </div>
    <div class="feature-card">
        <h3>📱 Responsive Design</h3>
        <p>Looks great on desktop, tablet, and mobile devices.</p>
    </div>
    <div class="feature-card">
        <h3>🎨 Customizable</h3>
        <p>Easy to customize with CSS variables and clean HTML.</p>
    </div>
</div>
```

#### Code Examples
Use syntax highlighting for better readability:

```html
<!-- JavaScript -->
<pre><code class="language-javascript">
function greetUser(name) {
    return `Hello, ${name}! Welcome to our docs.`;
}
</code></pre>

<!-- CSS -->
<pre><code class="language-css">
.custom-style {
    color: var(--primary-color);
    font-weight: 600;
}
</code></pre>

<!-- HTML -->
<pre><code class="language-html">
&lt;div class="example"&gt;
    &lt;p&gt;This is an example&lt;/p&gt;
&lt;/div&gt;
</code></pre>
```

#### Tables
Organize data with responsive tables:

```html
<div class="table-wrapper">
    <table>
        <thead>
            <tr>
                <th>Feature</th>
                <th>Description</th>
                <th>Status</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Responsive Design</td>
                <td>Works on all screen sizes</td>
                <td>✅ Complete</td>
            </tr>
            <tr>
                <td>Dark Mode</td>
                <td>Automatic dark mode support</td>
                <td>🚧 In Progress</td>
            </tr>
        </tbody>
    </table>
</div>
```

## Visual Customization

### Color Themes

#### Light Theme (Default)
```css
:root {
    --primary-color: #2563eb;
    --background-color: #ffffff;
    --text-color: #1e293b;
    --surface-color: #f8fafc;
    --border-color: #e2e8f0;
}
```

#### Dark Theme
```css
:root {
    --primary-color: #3b82f6;
    --background-color: #0f172a;
    --text-color: #f1f5f9;
    --surface-color: #1e293b;
    --border-color: #334155;
}
```

#### Custom Brand Colors
```css
:root {
    /* Example: Purple brand */
    --primary-color: #7c3aed;
    --primary-light: #8b5cf6;
    --primary-dark: #6d28d9;
    
    /* Example: Green brand */
    --primary-color: #10b981;
    --primary-light: #34d399;
    --primary-dark: #059669;
}
```

### Typography Customization

#### Font Selection
```css
:root {
    /* Modern fonts */
    --font-family: 'Inter', system-ui, sans-serif;
    
    /* Classic fonts */
    --font-family: 'Georgia', 'Times New Roman', serif;
    
    /* Technical fonts */
    --font-family: 'IBM Plex Sans', monospace;
}
```

#### Font Sizes
```css
:root {
    --font-size-xs: 0.75rem;
    --font-size-sm: 0.875rem;
    --font-size-base: 1rem;
    --font-size-lg: 1.125rem;
    --font-size-xl: 1.25rem;
    --font-size-2xl: 1.5rem;
    --font-size-3xl: 1.875rem;
}
```

### Layout Modifications

#### Wider Sidebar
```css
:root {
    --sidebar-width: 350px;
}
```

#### Full-Width Content
```css
:root {
    --content-max-width: none;
}

.content-wrapper {
    max-width: none;
}
```

#### Centered Layout
```css
.docs-container {
    max-width: 1400px;
    margin: 0 auto;
}
```

## Advanced Customization

### Custom Components

#### Progress Bars
```html
<div class="progress-container">
    <div class="progress-bar" style="width: 75%"></div>
</div>
```

```css
.progress-container {
    background: var(--border-color);
    border-radius: 1rem;
    height: 0.5rem;
    margin: 1rem 0;
}

.progress-bar {
    background: var(--primary-color);
    border-radius: 1rem;
    height: 100%;
    transition: width 0.3s ease;
}
```

#### Badges
```html
<span class="badge badge-primary">New</span>
<span class="badge badge-success">Stable</span>
<span class="badge badge-warning">Beta</span>
```

```css
.badge {
    display: inline-block;
    padding: 0.25rem 0.5rem;
    border-radius: 0.375rem;
    font-size: 0.75rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.025em;
}

.badge-primary {
    background: var(--primary-color);
    color: white;
}

.badge-success {
    background: var(--success-color);
    color: white;
}

.badge-warning {
    background: var(--warning-color);
    color: white;
}
```

### Interactive Elements

#### Collapsible Sections
```html
<div class="collapsible">
    <button class="collapsible-toggle">Click to expand</button>
    <div class="collapsible-content">
        <p>This content can be collapsed and expanded.</p>
    </div>
</div>
```

```css
.collapsible-content {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease;
}

.collapsible.open .collapsible-content {
    max-height: 500px; /* Adjust as needed */
}
```

#### Tabs
```html
<div class="tabs">
    <div class="tab-buttons">
        <button class="tab-button active" data-tab="tab1">Tab 1</button>
        <button class="tab-button" data-tab="tab2">Tab 2</button>
    </div>
    <div class="tab-content">
        <div id="tab1" class="tab-panel active">Content for tab 1</div>
        <div id="tab2" class="tab-panel">Content for tab 2</div>
    </div>
</div>
```

### Performance Optimization

#### Image Optimization
- Use WebP format when possible
- Provide multiple sizes for responsive images
- Lazy load images below the fold

#### CSS Optimization
- Remove unused CSS rules
- Minify CSS for production
- Use CSS custom properties for consistency

#### JavaScript Optimization
- Minify JavaScript files
- Load non-critical scripts asynchronously
- Use modern JavaScript features

## Accessibility

### Screen Reader Support
```html
<!-- Add ARIA labels -->
<nav aria-label="Documentation navigation">
<main aria-label="Main content">
<button aria-expanded="false" aria-controls="menu">Menu</button>
```

### Keyboard Navigation
```css
/* Focus indicators */
.nav-link:focus,
button:focus {
    outline: 2px solid var(--primary-color);
    outline-offset: 2px;
}
```

### Color Contrast
Ensure sufficient color contrast (4.5:1 for normal text, 3:1 for large text):

```css
/* Good contrast example */
:root {
    --text-color: #1e293b;        /* Dark text */
    --background-color: #ffffff;  /* Light background */
}
```

Test your color combinations with accessibility tools like WebAIM's Contrast Checker.
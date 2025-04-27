# Kensington Landing Page - Maintenance Guide

This guide will help you maintain and customize the Kensington landing page for luxury glass shower enclosures. Follow these detailed instructions to make common updates while preserving the design integrity.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold tracking-tighter">Kensington</a>
```
- Replace "Kensington" with your company name
- Maintain the existing classes for consistent styling

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `>` and `</a>` tags
- Keep the `href` attributes matching your section IDs

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tighter mb-8">Experience Spa-Like Luxury With Premium Glass Shower Enclosures</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">Transform your bathroom into a sanctuary of elegance and sophistication.</p>
```

- Update headline text between `<h1>` tags
- Modify subheading text between `<p>` tags
- Maintain responsive classes (`text-4xl md:text-5xl lg:text-6xl`)

### Understanding Tailwind Classes
Common classes used in this page:

- Text sizes: `text-xl`, `text-2xl`, etc.
- Colors: `text-gray-300`, `bg-gray-900`
- Spacing: `px-6`, `py-4`, `mb-8`
- Responsive prefixes: `md:`, `lg:`

Example of modifying text size:
```html
<!-- Original -->
<p class="text-xl">Your text</p>

<!-- Larger text -->
<p class="text-2xl">Your text</p>
```

## Managing Links

### External Links
Current external links that need attention:

```html
<!-- Main CTA button -->
<a href="http://www.customeuroglass.com" class="hidden md:block px-6 py-2 bg-white text-gray-900 rounded-full">Get Started</a>

<!-- Email link -->
<a href="mailto:ts@customeuroglass.com" class="text-xl text-white hover:text-gray-300">ts@customeuroglass.com</a>
```

To update:
1. Replace `http://www.customeuroglass.com` with your website URL
2. Update `mailto:ts@customeuroglass.com` with your contact email

### Internal Navigation
Internal links use section IDs:

```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

To modify:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#` followed by the section ID
3. Ensure the linked section has a matching `id` attribute

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer's Quick Links section:

```html
<!-- Add inside the Quick Links ul element -->
<ul class="space-y-2">
    <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
    <!-- Add these new lines -->
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Creating Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

Example structure for policy pages:
```html
<!-- privacy.html or terms.html -->
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="bg-gray-900 text-gray-100 antialiased">
    <!-- Copy header section -->
    
    <main class="container mx-auto px-6 py-24">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Verify section IDs match href attributes exactly
   - Check for typos in IDs and href values
   - Ensure sections have unique IDs

2. **Responsive Design Issues**
   - Keep responsive class prefixes (`md:`, `lg:`)
   - Test on different screen sizes
   - Don't remove `hidden md:block` classes from navigation

3. **Styling Inconsistencies**
   - Copy existing classes when adding new elements
   - Maintain color scheme using `text-gray-*` and `bg-gray-*` classes
   - Keep spacing consistent using `px-*`, `py-*`, `mb-*` classes

Need additional help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).
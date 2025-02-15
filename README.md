# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text (TWD):**
```html
<!-- Find this line -->
<a href="/" class="text-2xl font-bold text-gray-800 hover:text-blue-600 transition-colors">TWD</a>
```
Simply replace "TWD" with your desired text.

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors">Features</a>
```
Replace "Features" with your new menu item name. The classes control:
- `text-gray-600`: Text color
- `hover:text-blue-600`: Color when hovering
- `transition-colors`: Smooth color transition

### Hero Section
To modify the main headline and subheading:

```html
<h1 class="text-4xl md:text-6xl font-bold text-gray-900 mb-6 leading-tight">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```
- `text-4xl`: Controls text size on mobile
- `md:text-6xl`: Controls text size on desktop
- `mb-6`: Adds margin bottom spacing

### Features Section
To add or modify feature cards:

1. Copy the existing feature card structure:
```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4 text-gray-900">Free Hosting</h3>
    <p class="text-gray-600 leading-relaxed">Your feature description here</p>
</div>
```

2. Paste it within the grid container and update the content.

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://twd.com" class="...">Get Started</a>
```

### Updating Links
1. For internal section links (starting with #):
   - Ensure the href matches the id of the target section
   - Example: `href="#features"` links to `<section id="features">`

2. For external links:
   - Replace "https://twd.com" with your actual website URL
   - Example: `<a href="https://yourwebsite.com">`

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

1. Locate the footer section:
```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
    <p>&copy; 2024 Texas Web Design. All rights reserved.</p>
</div>
```

2. Add the new links before the copyright notice:
```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
    <div class="mb-4">
        <a href="/privacy.html" class="text-gray-400 hover:text-white mr-4">Privacy Policy</a>
        <a href="/terms.html" class="text-gray-400 hover:text-white">Terms of Service</a>
    </div>
    <p>&copy; 2024 Texas Web Design. All rights reserved.</p>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links:**
   - Check that section IDs match href attributes exactly
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues:**
   - Look for classes starting with `md:` or `lg:`
   - These control appearance on different screen sizes
   - Example: `text-4xl md:text-6xl` means:
     - Mobile: text-4xl
     - Desktop: text-6xl

3. **Missing Styles:**
   - Verify the Tailwind CSS CDN link is present in the head section
   - Check for typos in class names
   - Tailwind classes must be exact matches

### Need Help?
- Inspect elements using browser developer tools (Right-click → Inspect)
- Compare your changes with the original code
- Test on both mobile and desktop views
- Verify all links work before publishing changes

Remember to always backup your code before making changes, and test thoroughly on different devices and browsers.
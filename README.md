# Landing Page Maintenance Guide

This guide will help you maintain and customize the landing page, with detailed instructions for common modifications. This documentation assumes basic familiarity with HTML but explains concepts thoroughly for beginners.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name**
```html
<!-- Find this line in the header -->
<a href="#" class="text-2xl font-bold text-gray-900">Lorem ipsum</a>
```
Replace "Lorem ipsum" with your company name. The classes control:
- `text-2xl`: Text size
- `font-bold`: Text weight
- `text-gray-900`: Text color

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">Transform Your Vision Into Reality</h1>
<p class="text-xl text-gray-600 mb-12 leading-relaxed">We create modern and minimalist solutions...</p>
```

To modify:
1. Replace the h1 text with your main headline
2. Update the paragraph text with your description
3. The responsive text sizes are:
   - Mobile: `text-4xl`
   - Tablet: `md:text-5xl`
   - Desktop: `lg:text-6xl`

### Services Section
Each service card follows this structure:
```html
<div class="p-8 rounded-2xl bg-gray-50 hover:bg-white hover:shadow-xl transition-all duration-300">
    <div class="w-12 h-12 bg-gray-900 rounded-lg mb-6"></div>
    <h3 class="text-xl font-bold mb-4">Web Design</h3>
    <p class="text-gray-600 leading-relaxed">Modern and minimalist designs...</p>
</div>
```

To modify:
1. Update the h3 text for service titles
2. Change the paragraph text for service descriptions
3. Key classes explained:
   - `rounded-2xl`: Rounds the corners
   - `hover:shadow-xl`: Adds shadow on hover
   - `transition-all`: Ensures smooth animations

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are placeholder hashtags (#). To update:

```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">About</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Services</a>
    <!-- More links -->
</div>
```

To fix:
1. Replace `href="#"` with proper page URLs:
   - Internal pages: `href="about.html"`
   - External links: `href="https://example.com"`
2. Maintain the existing classes for consistent styling

### Call-to-Action Links
Located in the hero and CTA sections:

```html
<a href="#" class="inline-block bg-gray-900 text-white px-8 py-4 rounded-lg">Get Started</a>
```

Update these links to point to:
- Contact forms
- Signup pages
- Product pages

## Linking Privacy and Terms Pages

### Footer Legal Links
Located in the footer's "Legal" section:

```html
<div>
    <h4 class="font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy</a></li>
        <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the links:
```html
<li><a href="privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy</a></li>
<li><a href="terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Responsive Design**
   - Check that you haven't removed important responsive classes (md:, lg:)
   - Verify the viewport meta tag is present in the head

2. **Missing Styles**
   - Ensure the Tailwind CSS CDN link is working
   - Check for typos in class names

3. **Social Media Icons Not Showing**
   - Verify SVG paths are complete and correct
   - Check that the viewBox attribute is present

4. **Hover Effects Not Working**
   - Confirm hover: classes are properly formatted
   - Ensure transition classes are present

Remember to test all changes across different screen sizes using your browser's developer tools (F12 or right-click > Inspect).
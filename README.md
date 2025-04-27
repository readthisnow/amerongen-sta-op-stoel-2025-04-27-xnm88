# Amerongen Landing Page Maintenance Guide

This guide will help you maintain and customize the Amerongen landing page. It's written for beginners and provides step-by-step instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-gray-800">Amerongen</a>
```
Simply replace "Amerongen" with your desired company name.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Voordelen</a>
    <!-- More menu items -->
</div>
```
Replace the text between `<a>` tags to change menu items.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Amerongen Sta Op Stoel
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">
    Tijdelijk 10% Korting op Alle Modellen
</p>
```
- To change the main title, update the text inside `<h1>`
- For the subtitle, modify the text inside the `<p>` tag

### Understanding Tailwind Classes
Common classes used in this page:
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `font-bold`: Makes text bold
- `text-{color}-{shade}`: Sets text color (gray-900, blue-600, etc.)
- `mb-{number}`: Adds margin bottom (mb-4, mb-8, etc.)
- `py-{number}`: Adds padding top and bottom
- `px-{number}`: Adds padding left and right

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Voordelen</a>
<a href="#benefits">Kenmerken</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Change the `href` value to your desired section ID
2. Ensure the corresponding section has a matching `id` attribute
3. For external links, use the full URL: `href="https://yoursite.com"`

### Call-to-Action Buttons
Located in the hero section:
```html
<a href="https://sta-opstoelen.nl" class="inline-flex items-center px-8 py-4 bg-blue-600 text-white">
    Bekijk Aanbod
</a>
```
Replace `https://sta-opstoelen.nl` with your desired URL.

### Contact Link
```html
<a href="mailto:support@example.com">Contact Opnemen</a>
```
Replace `support@example.com` with your actual email address.

## Adding Privacy and Terms Pages

### Footer Links Setup
Current footer links:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors">Algemene Voorwaarden</a></li>
</ul>
```

To link to privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project directory
2. Update the links in the footer:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors">Algemene Voorwaarden</a></li>
```

### Maintaining Consistent Styling
When creating new pages, copy these elements from index.html:
- The entire `<head>` section
- Header and footer sections
- CSS classes for consistent styling

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match exactly with href values
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
- Look for classes starting with `md:` or `lg:`
- These control how elements appear on different screen sizes
- Example: `hidden md:flex` means hidden on mobile, visible as flex on medium screens

3. **Style Changes Not Working**
- Verify Tailwind CSS is properly loaded
- Check for typos in class names
- Ensure classes are space-separated

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always test changes across different devices and browsers before publishing updates to your live site.
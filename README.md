# PinSpector Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the PinSpector landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text**: Find this line and update the text between the `div` tags:
```html
<div class="text-2xl font-bold text-blue-600">PinSpector</div>
```

2. **Navigation Menu Items**: Located in the header `nav` section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
To update the main headline and subtitle:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Best Pinterest Spy Tool 2025
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Uncover Top Trending Searches on Pinterest
</p>
```

#### Tailwind CSS Class Guide
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `mb-6`: Adds margin bottom spacing
- `text-gray-900`: Dark gray text color

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-search text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Spy on Competition</h3>
    <p class="text-gray-600">Track your competitors' strategies...</p>
</div>
```

To modify:
1. Change the icon by updating the `fas fa-search` class
2. Update the heading text in the `h3` tag
3. Modify the description in the `p` tag

## Managing Links

### Internal Navigation Links
Current internal links use anchor tags (#):
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```

To update:
1. Ensure section IDs match the href values
2. Example: `href="#features"` links to `<section id="features">`

### External Links
The main call-to-action buttons link to:
```html
<a href="https://pinspector.com" class="inline-block px-8 py-4 bg-blue-600">
```

To update:
1. Replace `https://pinspector.com` with your desired URL
2. Test the link after updating
3. Ensure all instances are updated (header, hero, and CTA sections)

## Adding Privacy and Terms Pages

### Footer Links Section
Locate the legal links in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Check that section IDs match exactly with href values
- IDs are case-sensitive
- Remove any spaces in IDs

2. **Responsive Design Issues**
- Verify Tailwind classes starting with `md:` and `lg:`
- Test on different screen sizes
- Common classes:
  - `md:flex`: Shows on medium screens
  - `hidden md:block`: Hidden on mobile, visible on medium screens

3. **Icon Problems**
- Ensure Font Awesome is properly loaded
- Check icon class names at [Font Awesome](https://fontawesome.com/icons)
- Verify the icon classes start with `fas`, `far`, or `fab`

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12 key)
2. Verify all files are in the correct directory
3. Ensure all HTML tags are properly closed
4. Validate your HTML at [W3C Validator](https://validator.w3.org/)

Remember to always test your changes across different devices and browsers before deploying to production.
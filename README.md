# Landing Page Maintenance Guide

This guide will help you maintain and customize the KalmerendeKnuffel landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<div class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    KalmerendeKnuffel <!-- Change this text -->
</div>
```

2. **Navigation Links:**
```html
<div class="hidden lg:flex space-x-8">
    <a href="#features">Kenmerken</a> <!-- Change menu item text here -->
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-8 leading-tight">
    Kalmerende Knuffel Volwassenen <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Koop Nu Met Speciale Korting <!-- Update subheadline -->
</p>
```

### Tailwind CSS Tips
- `text-4xl` to `text-6xl`: Controls text size
- `md:` and `lg:`: Responsive breakpoints
- `mb-8`: Margin bottom spacing
- `text-gray-300`: Text color
- `font-bold`: Text weight

To modify styling:
1. Find the element you want to change
2. Locate its class attribute
3. Add or replace Tailwind classes

Example:
```html
<!-- Original -->
<h3 class="text-xl font-semibold mb-4">

<!-- Making text larger and purple -->
<h3 class="text-2xl font-semibold mb-4 text-purple-500">
```

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#features">Kenmerken</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. The `#` symbol indicates an internal page section
2. Match the href value with section IDs in the HTML
3. For external links, use complete URLs

### Call-to-Action Buttons
```html
<a href="https://amzn.to/4iy7Qfm" class="inline-flex items-center px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full">
    Bestel Nu Met Korting
</a>
```

To update:
1. Replace `https://amzn.to/4iy7Qfm` with your desired URL
2. Update button text between opening and closing tags

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-purple-500">
        <i class="fab fa-facebook text-2xl"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-purple-500">
        <i class="fab fa-instagram text-2xl"></i>
    </a>
</div>
```

Replace `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Create New Files
1. Create `privacy.html` and `terms.html` in your project folder
2. Copy the basic structure from `index.html`

### Step 2: Update Footer Links
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="privacy.html" class="hover:text-purple-500 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-purple-500 transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Step 3: Maintain Consistent Styling
Copy these classes for consistent link styling:
```html
class="hover:text-purple-500 transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href values
   - IDs must be unique
   - Check for typos in href attributes

2. **Responsive Design Issues**
   - Check responsive classes (md:, lg:)
   - Test on different screen sizes
   - Verify container class is present

3. **Style Problems**
   - Confirm Tailwind CDN is loaded
   - Check class spelling
   - Ensure no conflicting classes

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always test changes across different devices and browsers before publishing updates.
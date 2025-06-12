# Texas Pro Locksmith Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Pro Locksmith landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold text-white hover:text-blue-400 transition duration-300">
    Texas Pro Locksmith  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>  <!-- Change menu item text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
To update the main headline and subtext:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 text-white">
    San Antonio's Premier Locksmith Service  <!-- Change main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-8 max-w-3xl mx-auto">
    Professional, fast, and reliable locksmith services  <!-- Change subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:

- Text sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-white`, `text-gray-300`, `bg-gray-900`
- Spacing: `px-4`, `py-24`, `mb-8`, `mt-12`
- Responsive design: `md:text-5xl`, `lg:text-6xl`

To modify a style, simply change the class value. For example:
```html
<!-- Original -->
<div class="bg-gray-900">

<!-- Modified to be lighter -->
<div class="bg-gray-800">
```

## Fixing Broken Links

### Current Link Structure
The page contains several types of links:

1. **Navigation Menu Links (Internal):**
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update these, ensure the href matches the ID of the target section.

2. **Call-to-Action Links (External):**
```html
<!-- Update this URL to your actual service page -->
<a href="https://texasprolocksmiths.com/" class="inline-block bg-blue-600">
    Get Emergency Service
</a>
```

### How to Update Links
1. For internal links:
   ```html
   <!-- Format -->
   <a href="#sectionID">Link Text</a>
   
   <!-- Example -->
   <a href="#contact">Contact Us</a>
   ```

2. For external links:
   ```html
   <!-- Format -->
   <a href="https://your-full-url.com">Link Text</a>
   
   <!-- Example -->
   <a href="https://texasprolocksmiths.com/contact">Contact Us</a>
   ```

## Linking Privacy and Terms Pages

### Footer Links
Located in the footer section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="text-gray-400 space-y-2">
        <!-- Update these href attributes -->
        <li><a href="/privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Adding New Policy Pages
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the href attributes in the footer:
```html
<!-- For local files in the same directory -->
<a href="privacy.html">Privacy Policy</a>

<!-- For files in a subdirectory -->
<a href="policies/privacy.html">Privacy Policy</a>

<!-- For external policy pages -->
<a href="https://texasprolocksmiths.com/privacy">Privacy Policy</a>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links:**
   - Ensure section IDs match the href attributes
   - Check for typos in both the href and id attributes
   - IDs are case-sensitive

2. **Responsive Design Issues:**
   - Keep the `md:` and `lg:` prefixed classes for responsive behavior
   - Test on different screen sizes using browser dev tools
   - Don't remove the `container` classes from parent elements

3. **Style Inconsistencies:**
   - Maintain color scheme using existing classes
   - Keep consistent spacing using provided padding/margin classes
   - Use the same transition effects: `transition duration-300`

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using Chrome DevTools (F12)

Remember to always test changes in multiple browsers and screen sizes before deploying to production.
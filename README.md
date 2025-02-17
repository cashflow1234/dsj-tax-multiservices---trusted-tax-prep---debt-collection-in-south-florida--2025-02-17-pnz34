# DSJ Tax Multiservices Landing Page - Maintenance Guide

This guide will help you maintain and customize the DSJ Tax Multiservices landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Company Name and Logo
```html
<div class="text-2xl font-bold text-white">DSJ<span class="text-blue-500">Tax</span></div>
```
- To change the company name, modify the text between the `<div>` tags
- The blue highlight is created by `text-blue-500` class on the `<span>` element

### Hero Section Text
Located in the first section after the header:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    DSJ Tax Multiservices
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Reliable Tax Prep & Debt Collection - We've Got You Covered!
</p>
```
To modify:
1. Change the text between the tags
2. Adjust text size using Tailwind classes:
   - `text-4xl`: Base size
   - `md:text-5xl`: Medium screens
   - `lg:text-6xl`: Large screens

### Service Cards
Located in the "Our Core Services" section:
```html
<div class="bg-gray-900 p-8 rounded-xl shadow-lg">
    <i class="fas fa-shield-alt text-4xl text-blue-500 mb-4"></i>
    <h3 class="text-xl font-bold mb-4">Trust</h3>
    <p class="text-gray-400">Built on years of experience...</p>
</div>
```
To modify:
1. Change icon: Update `fa-shield-alt` to any [Font Awesome](https://fontawesome.com/icons) icon name
2. Update heading: Modify text in `<h3>` tags
3. Update description: Change text in `<p>` tags

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-300 hover:text-white">Services</a>
    <a href="#benefits" class="text-gray-300 hover:text-white">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white">FAQ</a>
    <a href="#contact" class="text-gray-300 hover:text-white">Contact</a>
</div>
```
To update:
1. Locate the `href` attribute in each `<a>` tag
2. Replace the `#section-name` with:
   - Internal links: Use `#` followed by the section's ID
   - External links: Use full URL (e.g., `https://example.com`)

### Call-to-Action Links
The "Get Started" button links:
```html
<a href="https://form.jotform.com/250476421727054" class="inline-block px-8 py-4 bg-blue-600">
    Start Your Tax Journey
</a>
```
To update:
1. Replace the JotForm URL with your new form URL
2. Ensure all instances of this link are updated (header and CTA section)

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```
To add proper links:
1. Create your privacy policy page (e.g., `privacy.html`)
2. Create your terms page (e.g., `terms.html`)
3. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - IDs are case-sensitive
   - Example: `href="#services"` must match `id="services"`

2. **Responsive Design Issues**
   - Check responsive classes start with correct breakpoints:
     - `md:` for medium screens
     - `lg:` for large screens
   - Example: `text-4xl md:text-5xl lg:text-6xl`

3. **Icon Not Displaying**
   - Verify Font Awesome is properly loaded
   - Check icon class names against Font Awesome documentation
   - Example: `fas fa-shield-alt`

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct directory
3. Ensure all external resources (Tailwind CSS, Font Awesome) are loading properly

Remember to always test changes across different devices and browsers to ensure consistency.
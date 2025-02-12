# CaptureOsa Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the CaptureOsa photography workshop landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line -->
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-emerald-400 to-teal-500 bg-clip-text text-transparent">CaptureOsa</a>
```
- Replace "CaptureOsa" with your desired text
- The gradient effect is created by `from-emerald-400 to-teal-500`

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#workshops" class="text-gray-300 hover:text-white transition-colors duration-300">Workshops</a>
    <!-- Add or modify menu items here -->
</div>
```
- Each link uses `text-gray-300` for default state
- `hover:text-white` creates the hover effect
- `transition-colors duration-300` adds smooth color transition

### Hero Section
The main banner section contains:

```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8 bg-gradient-to-r from-emerald-400 to-teal-500 bg-clip-text text-transparent">Capture the Wild Beauty of Costa Rica</h1>
```
- `text-4xl` sets mobile size
- `md:text-6xl` and `lg:text-7xl` adjust size for larger screens
- The gradient text effect matches the logo

### Features Section
To modify feature cards:

```html
<div class="bg-gray-800 rounded-2xl p-8 hover:scale-105 transition-transform duration-300 border border-gray-700">
    <!-- Icon container -->
    <div class="w-16 h-16 bg-gradient-to-br from-emerald-500 to-teal-600 rounded-full mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Photography Workshops</h3>
    <p class="text-gray-400">Your description here</p>
</div>
```
- Each card has hover animation via `hover:scale-105`
- Maintain consistent spacing with `mb-4` and `mb-6`

## Fixing Broken Links

### Navigation Menu Links
Current internal links:
```html
<a href="#workshops">Workshops</a>
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
To update:
1. For internal sections, keep the `#` prefix
2. Ensure the ID matches in the corresponding section:
```html
<section id="features" class="py-24 bg-gray-800/50">
```

### External Links
The booking button links need updating:
```html
<!-- Find all instances of -->
<a href="https://captureosa.com">Book Now</a>
```
Replace with your actual booking URL.

## Linking Privacy and Terms Pages

### Footer Links Section
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Gradients**
- Ensure all gradient classes include both `from-` and `to-` values
- Example: `bg-gradient-to-r from-emerald-400 to-teal-500`

2. **Responsive Issues**
- Check that media query classes start with `md:` or `lg:`
- Example: `text-4xl md:text-6xl lg:text-7xl`

3. **Missing Hover Effects**
- Verify hover classes start with `hover:`
- Example: `hover:scale-105 hover:text-white`

### Need Help?
- Double-check class names against [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Ensure all sections have matching IDs for navigation
- Verify all external links start with `https://`

Remember to test all changes across different screen sizes using your browser's developer tools (F12 or right-click > Inspect).
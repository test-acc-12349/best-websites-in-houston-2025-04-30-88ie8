# Houston Web Landing Page Maintenance Guide

This guide provides instructions for maintaining and customizing the Houston Web landing page. It's designed for beginners with no prior coding experience.

## Table of Contents

1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting Tips](#troubleshooting-tips)

## Updating Text and Tailwind CSS Classes

### Header Section

The header contains the logo and navigation menu.

To update the logo text:

1. Locate the following line in the HTML:
   ```html
   <a href="#" class="text-2xl font-bold text-blue-600">Houston Web</a>
   ```
2. Change "Houston Web" to your desired text.

To modify navigation menu items:

1. Find the `<div class="hidden md:flex space-x-6">` section.
2. Update the text within the `<a>` tags. For example:
   ```html
   <a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Our Features</a>
   ```

### Hero Section

The hero section is the large blue area at the top of the page.

To update the main heading:

1. Locate the `<h1>` tag:
   ```html
   <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 leading-tight">Best Websites In Houston</h1>
   ```
2. Replace "Best Websites In Houston" with your desired text.

To change the subheading:

1. Find the `<p>` tag below the `<h1>`:
   ```html
   <p class="text-xl md:text-2xl mb-8">Custom Websites For Your Business</p>
   ```
2. Update the text as needed.

### Features Section

To modify feature items:

1. Locate the `<section id="features">` area.
2. Each feature is within a `<div>` with class `bg-gray-50 p-8 rounded-lg shadow-md...`.
3. Update the `<h3>` and `<p>` tags within each feature div.

Example:
```html
<div class="bg-gray-50 p-8 rounded-lg shadow-md hover:shadow-lg transition duration-300 transform hover:scale-105">
    <svg class="w-12 h-12 text-blue-500 mb-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
    </svg>
    <h3 class="text-xl font-semibold mb-4">User-Friendly Design</h3>
    <p class="text-gray-600">Our websites are designed with the user in mind, ensuring easy navigation and a great experience.</p>
</div>
```

### Modifying Tailwind CSS Classes

Tailwind CSS uses utility classes to style elements. Here's a breakdown of some key classes used in this landing page:

- `text-{size}`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-{weight}`: Sets font weight (e.g., `font-bold`, `font-semibold`)
- `text-{color}`: Changes text color (e.g., `text-blue-600`, `text-gray-600`)
- `bg-{color}`: Sets background color (e.g., `bg-white`, `bg-blue-600`)
- `p-{size}`: Adds padding (e.g., `p-8`)
- `m-{size}`: Adds margin (e.g., `mb-6` for margin-bottom)
- `rounded-{size}`: Applies border radius (e.g., `rounded-lg`)

To modify these classes:

1. Identify the element you want to change.
2. Locate its class attribute.
3. Add, remove, or modify the classes as needed.

Example: To change the button color in the hero section from blue to green:

```html
<a href="https://sigmaseo.io" class="bg-green-500 text-white py-3 px-8 rounded-full font-semibold text-lg hover:bg-green-600 transition duration-300 transform hover:scale-105">Get Started</a>
```

## Fixing Broken Links

### Navigation Menu Links

The navigation menu contains internal links to page sections:

1. Features: `#features`
2. Benefits: `#benefits`
3. FAQ: `#faq`
4. Contact: `#contact`

To update these:

1. Locate the `<div class="hidden md:flex space-x-6">` in the header.
2. Modify the `href` attributes of the `<a>` tags.

Example:
```html
<a href="#our-features" class="text-gray-600 hover:text-blue-600 transition duration-300">Features</a>
```

### Footer Quick Links

The footer contains similar links. Update them in the same way:

1. Find the `<div>` with the heading "Quick Links" in the footer.
2. Modify the `href` attributes of the `<a>` tags within the `<ul>`.

### External Links

There are two external links in the page:

1. "Get Started" button in the hero section
2. "Get Your Website Now" button in the call-to-action section

Both currently link to `https://sigmaseo.io`. To update:

1. Locate these `<a>` tags.
2. Change the `href` attribute to your desired URL.

Example:
```html
<a href="https://your-website.com" class="bg-white text-blue-600 py-3 px-8 rounded-full font-semibold text-lg hover:bg-blue-100 transition duration-300 transform hover:scale-105">Get Started</a>
```

## Linking Privacy and Terms Pages

To add links to privacy and terms pages:

1. Locate the footer section (last `<footer>` tag in the HTML).
2. Find the `<div>` containing the "Quick Links".
3. Add new list items for Privacy and Terms:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Ensure that `privacy.html` and `terms.html` exist in the same directory as your `index.html` file.

## Troubleshooting Tips

1. If changes don't appear, try hard refreshing your browser (Ctrl+F5 on Windows, Cmd+Shift+R on Mac).
2. Validate your HTML using an online tool like [W3C Markup Validation Service](https://validator.w3.org/).
3. Check for typos in class names, as Tailwind CSS won't apply styles for misspelled classes.
4. If a section disappears, ensure you haven't accidentally deleted a closing tag.
5. For responsive design issues, test your page at different screen sizes using browser developer tools.

Remember to save your changes and upload the updated file to your web server after making modifications.
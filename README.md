# Essendon Accounting Landing Page - Maintenance Guide

This guide will help you maintain and customize the Essendon Accounting landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

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
<div class="text-2xl font-bold text-white">
    <a href="/" class="flex items-center space-x-2">
        <i class="fas fa-calculator text-blue-500"></i>
        <span>Essendon Accounting</span> <!-- Change company name here -->
    </a>
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-300 hover:text-white transition duration-300">Services</a>
    <!-- Add or modify menu items here -->
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-400 to-blue-600 bg-clip-text text-transparent">
    Essendon accounting services <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    Trusted advisors for your financial future <!-- Update subheading -->
</p>
```

### Tailwind CSS Tips
- `text-{size}`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-{size}`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `bg-{color}-{shade}`: Sets background color (e.g., `bg-blue-600`)
- `hover:`: Adds hover effects (e.g., `hover:text-white`)

## Managing Links

### Navigation Menu Links
Current links that need review:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
    <a href="https://theaccountants.com">Get Started</a> <!-- Update external link -->
</div>
```

To update:
1. Internal links (starting with #) point to section IDs
2. External links need full URLs
3. Always test links after updating

### Footer Links
Update company information and links:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <div>
        <h3 class="text-xl font-bold mb-4">Essendon Accounting</h3>
        <!-- Update company description -->
        <p class="text-gray-400">Your trusted partner for financial success.</p>
    </div>
    <!-- Service links -->
    <div>
        <ul class="space-y-2 text-gray-400">
            <li><a href="#">Tax Services</a></li> <!-- Add proper href -->
            <li><a href="#">Cloud Accounting</a></li>
            <li><a href="#">Financial Planning</a></li>
        </ul>
    </div>
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links with actual page links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="hover:text-white transition duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly (case-sensitive)
   - Example: `href="#services"` must match `id="services"`

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify these classes are present:
     ```html
     class="container mx-auto px-6"
     class="grid grid-cols-1 md:grid-cols-3"
     ```

3. **Icon Not Showing**
   - Verify Font Awesome is loaded:
     ```html
     <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
     ```

### Need Help?
- Check the Tailwind CSS documentation for class references
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test across different browsers
- Use browser developer tools to inspect elements

Remember to always backup your files before making changes, and test thoroughly on both desktop and mobile devices.
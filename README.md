# Armadale Accounting Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Armadale Accounting landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Company Name -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Armadale  <!-- Change this text to update company name -->
</a>

<!-- Navigation Menu Items -->
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>  <!-- Update menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

**Styling Tip:** The header uses `bg-gray-900/95 backdrop-blur-md` for a semi-transparent dark background with blur effect. Adjust the opacity by changing `900/95` to values between `900/0` and `900/100`.

### Hero Section
Located at the top of the page, the hero section contains the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-7xl font-bold tracking-tight mb-8">
    Building financial clarity in a complex world  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Expert accounting services tailored to your business needs  <!-- Subheading -->
</p>
```

**Responsive Design Tip:** The text sizes use responsive classes:
- `text-4xl`: Default size
- `md:text-5xl`: Medium screens
- `lg:text-7xl`: Large screens

### Services Section
Each service card follows this structure:

```html
<div class="bg-gray-800 rounded-2xl p-8 hover:scale-105">
    <h3 class="text-xl font-semibold mb-4">
        Business Valuation  <!-- Service title -->
    </h3>
    <p class="text-gray-400">
        Comprehensive analysis and valuation...  <!-- Service description -->
    </p>
</div>
```

## Managing Links

### Navigation Links
The page uses anchor links for internal navigation. Update these in two places:

1. Desktop Menu:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

2. Mobile Menu:
```html
<div x-show="isOpen" class="md:hidden mt-4">
    <!-- Update both desktop and mobile menus to match -->
    <a href="#services" class="block py-2">Services</a>
    <a href="#benefits" class="block py-2">Benefits</a>
    <a href="#contact" class="block py-2">Contact</a>
</div>
```

### External Links
Replace placeholder links with actual URLs:

```html
<!-- Get Started Button -->
<a href="https://theaccountants.com" class="inline-flex items-center">
    Get Started
</a>

<!-- Contact Email -->
<a href="mailto:support@example.com">
    support@example.com  <!-- Update with actual email -->
</a>
```

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Insert new links in the footer section:

```html
<div class="border-t border-gray-700 mt-12 pt-8 text-center text-gray-400">
    <p>&copy; 2024 Armadale Accounting. All rights reserved.</p>
    <!-- Add these lines below the copyright notice -->
    <div class="mt-4 space-x-4">
        <a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
        <a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
    </div>
</div>
```

### Step 2: Create New Pages
Create `privacy.html` and `terms.html` in your root directory using the same styling as the main page.

## Troubleshooting

### Common Issues

1. **Broken Responsive Design**
   - Check that you haven't removed important Tailwind classes like `md:` or `lg:` prefixes
   - Verify all responsive containers have `container mx-auto px-6`

2. **Missing Hover Effects**
   - Ensure hover classes (e.g., `hover:scale-105`, `hover:text-white`) remain intact
   - Check that `transition-colors duration-300` is present for smooth animations

3. **Gradient Text Not Showing**
   - Verify these classes are present for gradient text:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

### Need Help?
If you encounter issues:
1. Compare your changes against the original HTML
2. Check the browser console for errors
3. Verify all required CSS classes are present
4. Ensure all opening tags have corresponding closing tags

Remember to test your changes across different screen sizes using browser developer tools.
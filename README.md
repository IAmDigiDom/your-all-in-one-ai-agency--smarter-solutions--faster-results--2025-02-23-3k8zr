# AI Agency Landing Page - Maintenance Guide

This guide will help you maintain and customize the AI Agency landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates while preserving the design integrity.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Located in the header section -->
<div class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-cyan-500 bg-clip-text text-transparent">
    AI Agency  <!-- Change this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update text here -->
    <a href="#benefits">Benefits</a>  <!-- Update text here -->
    <a href="#faq">FAQ</a>           <!-- Update text here -->
    <a href="#contact">Contact</a>    <!-- Update text here -->
</div>
```

### Hero Section
The main headline and subheading can be updated here:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-500 to-cyan-500 bg-clip-text text-transparent">
    Your All-in-One AI Agency: Smarter Solutions, Faster Results!  <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    The #1 A.I. Agent Full Service Online!  <!-- Update subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:

- Text sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-gray-300`, `bg-gray-900`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-8` (margin bottom)
- Responsive design: `md:text-5xl` (applies at medium screens and up)

To modify styling:

1. Find the element you want to change
2. Locate its class attribute
3. Modify existing classes or add new ones
4. Test on different screen sizes

Example:
```html
<!-- Original -->
<div class="text-xl text-gray-300">

<!-- Modified for larger, blue text -->
<div class="text-2xl text-blue-300">
```

## Managing Links

### Navigation Links
All internal navigation links use section IDs:

```html
<!-- In the navigation menu -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Find the section you're linking to
2. Note its ID attribute
3. Use that ID in the href with a # prefix

### Call-to-Action Links
The main CTA buttons link to an external page:

```html
<!-- Current external link -->
<a href="https://digidom.databutton.app/prophet-folio">Get Started</a>

<!-- To update, replace the URL -->
<a href="https://your-new-url.com">Get Started</a>
```

### Social Media Links
Located in the footer:

```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <!-- Twitter icon -->
    </a>
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <!-- LinkedIn icon -->
    </a>
</div>
```

Replace the `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the legal section in the footer:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2 text-gray-400">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="hover:text-white transition-colors duration-300"
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Check for extra spaces in IDs

2. **Responsive Design Issues**
   - Test on multiple screen sizes
   - Use browser developer tools to check breakpoints
   - Verify `md:` and `lg:` classes are working

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     ```html
     bg-gradient-to-r from-blue-500 to-cyan-500 bg-clip-text text-transparent
     ```

4. **Social Media Icons Not Displaying**
   - Verify SVG paths are complete
   - Check if icons have proper viewBox attributes
   - Ensure icon classes include proper dimensions (`w-6 h-6`)

Remember to always test changes in multiple browsers and screen sizes before deploying to production.
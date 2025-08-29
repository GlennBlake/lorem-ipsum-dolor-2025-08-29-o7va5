# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Navigation Links](#managing-navigation-links)
- [Adding Legal Pages](#adding-legal-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this section in the header -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">
    Logo
</div>
```
Simply replace "Logo" with your company name. The gradient styling will automatically apply.

### Hero Section
Located at the top of the page with large text and two buttons:

1. **Main Heading**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent mb-8">
    Lorem ipsum dolor
</h1>
```
Replace "Lorem ipsum dolor" with your headline. Keep it brief for best appearance.

2. **Subheading**
```html
<p class="text-xl text-gray-600 mb-12">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.
</p>
```
Update this text with your main value proposition.

### Modifying Tailwind Classes

Important classes explained:
- `text-4xl`: Large text size
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `font-bold`: Bold text weight
- `text-gray-600`: Medium gray text color

To modify sizes:
1. Find the element you want to change
2. Locate the sizing class (e.g., `text-4xl`)
3. Replace with desired size:
   - Smaller: `text-2xl`
   - Larger: `text-6xl`

## Managing Navigation Links

### Main Navigation
```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Locate the `<a>` tag you want to modify
2. Update the `href="#"` to your desired URL:
   - Internal page: `href="about.html"`
   - External site: `href="https://example.com"`
   - Page section: `href="#features"`

### Footer Links
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">About</a></li>
    <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Careers</a></li>
    <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a></li>
</ul>
```

Follow the same process as main navigation to update these links.

## Adding Legal Pages

To add privacy policy and terms of service links:

1. Locate the footer section
2. Add new list items in the appropriate footer column:

```html
<ul class="space-y-2">
    <!-- Add these lines -->
    <li><a href="privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

Common issues and solutions:

### Text Styling Issues
- **Problem**: Gradient text not visible
- **Solution**: Ensure these classes are present:
  ```html
  bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent
  ```

### Link Problems
- **Problem**: Links not working
- **Solution**: Check for:
  1. Correct file names in `href`
  2. Proper file location (same folder or correct path)
  3. Complete URLs for external links (including `https://`)

### Responsive Design Issues
- **Problem**: Layout breaks on mobile
- **Solution**: Verify responsive classes:
  - `md:` prefix for medium screens
  - `lg:` prefix for large screens
  - `hidden md:flex` for mobile menu visibility

Need additional help? Consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or create an issue in your project repository.
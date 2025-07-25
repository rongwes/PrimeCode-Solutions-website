# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview
PrimeCode Solutions is a static website for a software engineering company specializing in frontend development, backend development, and mobile app development. The site is built with pure HTML, CSS, and vanilla JavaScript - no build tools or package managers are used.

## Tech Stack
- **Frontend**: Pure HTML5, CSS3, and vanilla JavaScript
- **Backend**: PHP (for contact form handling)
- **Styling**: Custom CSS with CSS Grid, Flexbox, and CSS Custom Properties (variables)
- **Icons**: Font Awesome 4.7.0
- **Fonts**: Google Fonts (Inter and JetBrains Mono)

## File Structure
```
/
├── index.html          # Homepage
├── aboutUs.html        # About Us page
├── services.html       # Services page
├── contact.html        # Contact page
├── form-handler.php    # Contact form processing
├── css/
│   ├── general.css     # Shared styles for all pages except homepage
│   └── homepage.css    # Homepage-specific styles
└── img/               # Images and assets
```

## Development Commands
Since this is a static website with no build process:
- **Local Development**: Open HTML files directly in browser or use a local server like `python -m http.server` or Live Server extension
- **No build commands**: Files are served directly as written
- **No package manager**: All dependencies are loaded via CDN

## Code Architecture

### CSS Architecture
- **CSS Custom Properties**: Extensive use of CSS variables defined in `:root` for consistent theming
- **Modular Approach**: `general.css` contains shared styles, page-specific CSS files for unique styling
- **Responsive Design**: Mobile-first approach with extensive media queries
- **Design System**: Consistent color palette, typography scale, and spacing system

### Key CSS Variables
- Primary colors: `--primary-color`, `--secondary-color`, `--accent-color`
- Text colors: `--text-primary`, `--text-secondary`, `--text-light`
- Background colors: `--background-light`, `--background-dark`, `--card-background`
- Shadows: `--shadow-sm`, `--shadow-md`, `--shadow-lg`, `--shadow-xl`
- Gradients: `--gradient-primary`, `--gradient-hero`

### JavaScript Functionality
- **Mobile Navigation**: Toggle functionality for responsive mobile menu
- **Menu Management**: Auto-close on link clicks and outside clicks
- **Smooth Scrolling**: For anchor links within pages
- **Form Handling**: Contact form submissions processed by PHP

### Page Structure
All pages follow a consistent structure:
1. **Navigation**: Sticky header with logo and navigation links
2. **Hero Section**: Page-specific hero with background images and overlays
3. **Content Sections**: Modular sections with consistent styling patterns
4. **Footer**: Company information, quick links, and social media

### Contact Form
- **form-handler.php**: Processes contact form submissions
- **Email Configuration**: Currently set to send emails to `morongwemolaba@gmail.com`
- **Fields**: Name, email, subject, message
- **Redirect**: Returns to contact.html after submission

## Content Management
- **Images**: Stored in `/img/` directory
- **Logo**: `logo.png` used consistently across all pages
- **Background Images**: Various background images for hero sections
- **Service Icons**: Font Awesome icons used throughout

## Responsive Design
- **Mobile-First**: Responsive design with breakpoints at 768px
- **Mobile Menu**: Slide-in navigation for mobile devices
- **Grid Systems**: CSS Grid and Flexbox for responsive layouts
- **Image Optimization**: Responsive images with proper aspect ratios

## Browser Compatibility
- **Modern Browsers**: Uses CSS Grid, Flexbox, and CSS Custom Properties
- **Progressive Enhancement**: Graceful degradation for older browsers
- **Font Loading**: Google Fonts with fallback system fonts

## Maintenance Notes
- **No Dependencies**: All external resources loaded via CDN
- **Static Hosting**: Can be deployed to any static hosting service
- **Email Configuration**: Update email addresses in `form-handler.php` as needed
- **Content Updates**: Direct HTML editing for content changes
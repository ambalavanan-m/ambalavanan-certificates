# Ambalavanan — Academic Record & Certificates

A modern, elegant personal portfolio website showcasing academic certificates, awards, and professional achievements. Built with vanilla HTML, CSS, and JavaScript with a focus on beautiful UI/UX and SEO optimization.

## 🎯 Features

### Core Functionality
- **Responsive Grid Layout** — Two-column grid that adapts to mobile (single column)
- **Certificate Modal Viewer** — Full-screen lightbox with smooth animations
- **Share & Download** — Native sharing via Web Share API with fallback to clipboard
- **Deep Linking** — Hash-based URL routing for direct certificate access
- **Keyboard Navigation** — Arrow keys and Escape for modal navigation
- **Smooth Animations** — Entrance animations, hover effects, and transitions
- **Toast Notifications** — User feedback for copy/share actions

### Design & UX
- **Premium Typography** — Cormorant Garamond (serif) + DM Sans (sans-serif)
- **Gold Accent Color Scheme** — Luxurious, professional aesthetic
- **Frosted Glass Header** — Backdrop blur effect on scroll
- **Intersection Observer** — Staggered card entrance animations
- **Hover Effects** — Image zoom, overlay, action button animations
- **Mobile-First Responsive** — Works seamlessly on all devices

### SEO & Performance
- **Structured Data (JSON-LD)** — Rich snippets for search engines
- **Meta Tags** — OpenGraph and Twitter Card support
- **Canonical URLs** — Prevents duplicate content issues
- **Semantic HTML** — Proper heading hierarchy and ARIA labels
- **Performance Optimized** — Lazy loading, minimal dependencies
- **Google Site Verification** — Pre-configured verification tags

## 🛠 Technologies Used

- **HTML5** — Semantic markup with ARIA attributes
- **CSS3** — Custom properties, Grid, Flexbox, Animations
- **Vanilla JavaScript** — No frameworks, ~300 lines of ES6 code
- **Google Fonts** — Cormorant Garamond & DM Sans
- **No Dependencies** — Fully self-contained

## 📋 File Structure

```
.
├── index.html                 # Main HTML file with embedded CSS/JS
├── certificates/
│   ├── 41279.png             # Certificate of Merit
│   └── 41280.png             # Certificate of Appreciation
├── profile.webp              # Profile image (used in logo & favicon)
└── README.md                 # This file
```

## 🚀 Getting Started

### Quick Setup

1. **Clone or download** this repository
2. **Ensure you have** the certificate images in a `certificates/` folder:
   - `41279.png` — Merit certificate
   - `41280.png` — Attendance certificate
3. **Add** your `profile.webp` image to the root directory
4. **Open** `index.html` in your browser — no build step required!

### Customization

#### Update Personal Information
Edit the following in `index.html`:

```html
<!-- Logo & Header -->
<span class="logo-main">Your Name</span>

<!-- Hero Title -->
<h1 class="hero-title">Your Custom Title</h1>

<!-- Footer -->
<span class="footer-text">Copyrights © Your Name</span>
<span class="footer-gold">Your Tagline</span>
```

#### Add/Remove Certificates
Each certificate is a `certificate-card` article. To add a new certificate:

```html
<article class="certificate-card" id="unique-id" data-index="2"
    data-full="certificates/image.png" 
    data-title="Certificate Title" 
    data-desc="Description">
    <!-- Copy structure from existing cards -->
</article>
```

#### Change Colors
All colors are CSS variables in `:root`:

```css
:root {
    --gold: #C9A84C;           /* Primary accent */
    --ink: #0D0D0D;            /* Text color */
    --cream: #FAF8F3;          /* Background */
    /* ... update as needed */
}
```

#### Modify Fonts
Update Google Fonts import and font-family declarations:

```css
body {
    font-family: 'Your Font', sans-serif;
}

.logo-main {
    font-family: 'Your Serif Font', serif;
}
```

## 📱 Browser Support

| Browser | Support |
|---------|---------|
| Chrome/Edge | ✅ Full |
| Firefox | ✅ Full |
| Safari | ✅ Full |
| iOS Safari | ✅ Full |
| Android Chrome | ✅ Full |

Requires ES6 support (IntersectionObserver, Web Share API with fallback).

## 🎨 Customization Guide

### Responsive Breakpoints
The design includes a media query at `768px` for tablet/mobile. Adjust as needed:

```css
@media (max-width: 768px) {
    /* Mobile-specific styles */
}
```

### Grid Layout
Change the number of columns (currently 2):

```css
.grid {
    grid-template-columns: repeat(3, 1fr);  /* 3 columns */
    gap: 2rem;
}
```

### Animation Easing
Customize the animation curve (currently `cubic-bezier(0.16, 1, 0.3, 1)`):

```css
--ease-expo: cubic-bezier(0.25, 0.46, 0.45, 0.94);
```

### Card Image Height
Adjust the certificate image container height:

```css
.card-image-wrapper {
    height: 380px;  /* Increase or decrease */
}
```

## 🔧 JavaScript API

### Open Modal Programmatically
```javascript
openModal(0);  // Open certificate at index 0
```

### Show Toast Notification
```javascript
showToast('Your message here');
```

### Share Certificate
```javascript
const card = cards[0];
shareCard(card);
```

## 📊 SEO Configuration

The site includes:
- ✅ Title & Meta Description
- ✅ Keywords
- ✅ OpenGraph tags (Facebook)
- ✅ Twitter Card tags
- ✅ Structured Data (JSON-LD)
- ✅ Canonical URL
- ✅ Google Site Verification
- ✅ Mobile viewport meta tag

**To deploy:** Replace verification IDs and URLs with your own:

```html
<meta name="google-site-verification" content="YOUR_ID" />
<meta property="og:url" content="YOUR_DOMAIN" />
```

## 🎯 Performance Optimizations

1. **Lazy Loading** — Images load on demand (`loading="lazy"`)
2. **CSS Variables** — Minimal CSS footprint with theming capability
3. **Hardware Acceleration** — Transforms/opacity for smooth animations
4. **No External Dependencies** — Single HTML file (embed CSS/JS)
5. **Minification Ready** — CSS and JavaScript can be minified for production

## 🚀 Deployment

### Netlify (Recommended)
```bash
# Push to GitHub, connect to Netlify
# Auto-deploys on push
```

### GitHub Pages
```bash
git push origin main  # Automatically deploys
```

### Vercel
```bash
# Connect repository and deploy automatically
```

### Manual Hosting
Simply upload all files to your web server (no build step required).

## 🎁 Feature Suggestions

See [FEATURES.md](./FEATURES.md) for a comprehensive list of enhancement ideas.

## 📝 License

This project is open-sourced for personal use. Modify and customize as needed.

## 🙋 Support

For issues or questions:
1. Check the customization guide above
2. Review the inline CSS comments for styling options
3. Inspect the JavaScript for functional details

---

**Built with attention to detail and modern web standards.**
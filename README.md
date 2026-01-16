# Cosmic Horizon BJJ - BITKRAFT Aesthetic

A dark, futuristic redesign of the Cosmic Horizon BJJ website inspired by the BITKRAFT Ventures aesthetic. This site combines Brazilian Jiu Jitsu academy content with cutting-edge web design optimized for performance on low-end devices.

## Design Philosophy

**BITKRAFT-Inspired Elements:**
- Dark background (#0a0a0a) with near-black sections
- Cyan (#00d4ff) and purple (#8b5cf6) gradient accents
- "Welcome to the Mat" loading screen with gradient text
- Futuristic glass-morphism navigation
- Minimal, clean typography with Inter font
- Subtle hover effects and transitions
- Card-based layout with dark cards (#121212)

**BJJ Content Preserved:**
- Complete class schedule
- All programs (Fundamentals, Advanced Gi, No-Gi, Kids, Women's, Open Mat)
- Membership pricing (Founders, Standard, Family, Class Packs)
- Contact information and free trial offer
- Baldwin Park, CA location details

## Performance Optimizations

### 1. **Minimal CSS Animations**
- Only GPU-accelerated properties (transform, opacity)
- No heavy 3D transforms or complex keyframes
- Respects `prefers-reduced-motion` for accessibility
- Simple CSS-only loader animation

### 2. **Efficient JavaScript**
- **~4KB minified** - No frameworks or libraries
- RequestAnimationFrame for scroll throttling
- Event delegation for menu interactions
- Loader removed from DOM after page load

### 3. **Optimized CSS**
- **CSS Custom Properties** for easy theming
- **Mobile-First Responsive Design**
- **Efficient Selectors** - No complex nesting
- **Backdrop Blur** - Hardware-accelerated
- **Clamp()** for fluid typography

### 4. **Lightweight Assets**
- **SVG Icons** - No image requests
- **Gradient Backgrounds** instead of images
- **Web Fonts** with preconnect for faster loading
- **Inline SVGs** in HTML

### 5. **Low-End Device Support**
- CSS blur filters instead of image processing
- No parallax scrolling
- Minimal DOM nodes
- Optimized reflow/repaint performance

## File Structure

```
.
├── index.html          # BJJ content with BITKRAFT design
├── styles.css          # Dark futuristic CSS (~12KB)
├── script.js           # Minimal JavaScript (~4KB)
└── README.md           # This file
```

## Color Palette

```css
--bg-dark: #0a0a0a        /* Main background */
--bg-darker: #050505      /* Sections background */
--bg-card: #121212        /* Card backgrounds */
--text-white: #ffffff     /* Primary text */
--text-gray: #a0a0a0      /* Secondary text */
--accent-blue: #00d4ff    /* Cyan accent */
--accent-purple: #8b5cf6  /* Purple accent */
--accent-cyan: #06b6d4    /* Alternative cyan */
```

## Key Features

### Hero Section
- Large gradient text: "Training Beyond The Horizon"
- Blurred radial gradient background effect
- Clean call-to-action button

### Classes Section
- 6 program cards with hover effects
- Class level badges (Beginner, Advanced, All Levels, etc.)
- Arrow-style bullet points
- Purple glow on hover

### Schedule Table
- Gradient header with blue-to-purple
- Dark card design
- Responsive horizontal scroll on mobile
- Hover states for rows

### Membership Plans
- 4 pricing tiers with featured "Founders" card
- Cyan border on featured plan
- Gradient badge for special rates
- Hover effects with glow
- Additional benefits section

### Contact Form
- Dark input fields with cyan focus states
- Gradient submit button
- Success/error message handling
- Free trial banner with gradient background

## Browser Support

- Chrome/Edge (modern)
- Firefox (modern)
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)
- Graceful degradation for older browsers

## Running Locally

1. **Simple HTTP Server:**
   ```bash
   python3 -m http.server 8080
   # Visit http://localhost:8080
   ```

2. **Or use npx:**
   ```bash
   npx serve
   ```

3. **Or just open:**
   - Double-click `index.html` (works but fonts may not load locally)

## Performance Metrics

Target metrics on low-end devices:

- **FCP (First Contentful Paint)**: < 1.8s
- **LCP (Largest Contentful Paint)**: < 2.5s
- **TBT (Total Blocking Time)**: < 200ms
- **CLS (Cumulative Layout Shift)**: < 0.1
- **Bundle Size**: ~25KB (HTML + CSS + JS)

## Customization

### Change Accent Colors
Edit `styles.css`:
```css
:root {
    --accent-blue: #00d4ff;    /* Change primary accent */
    --accent-purple: #8b5cf6;  /* Change secondary accent */
    --accent-cyan: #06b6d4;    /* Change tertiary accent */
}
```

### Modify Loading Message
Edit `index.html` line 17:
```html
<h1 class="loader-text">Welcome to the Mat</h1>
```

### Update Hero Text
Edit `index.html` lines 47-48:
```html
<span class="hero-title-line">Training Beyond</span>
<span class="hero-title-line gradient-text">The Horizon</span>
```

## Production Deployment

Before deploying:

1. **Minify Files**
   - Minify CSS and JavaScript
   - Consider using PostCSS for autoprefixing

2. **Optimize Fonts**
   - Use `font-display: swap` (already configured)
   - Consider self-hosting fonts

3. **Server Configuration**
   - Enable Gzip/Brotli compression
   - Set proper cache headers
   - Add security headers

4. **Testing**
   - Test on real low-end devices
   - Run Lighthouse audit
   - Check mobile responsiveness

## Design Comparison

| Aspect | Original BJJ Site | BITKRAFT Redesign |
|--------|-------------------|-------------------|
| Background | White/Light Gray | Dark (#0a0a0a) |
| Typography | Bebas Neue/Roboto | Inter (modern) |
| Accent Colors | Black | Cyan/Purple Gradients |
| Cards | Light with shadows | Dark with borders |
| Animations | Standard transitions | Minimal GPU-optimized |
| Loading Screen | None | "Welcome to the Mat" |
| Bundle Size | ~25KB | ~25KB (optimized) |
| Performance | Good | Excellent (60fps) |

## Credits

- **Design Inspiration**: BITKRAFT Ventures (bitkraft.vc)
- **Content**: Cosmic Horizon BJJ
- **Font**: Inter by Rasmus Andersson
- **Built with**: Vanilla HTML, CSS, JavaScript (no frameworks)

## License

This is a design demo/exercise. Brazilian Jiu Jitsu academy content belongs to Cosmic Horizon BJJ.

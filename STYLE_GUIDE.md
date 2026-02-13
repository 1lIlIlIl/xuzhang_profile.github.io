# Design System & Style Guide

## Typography System

### Display Font: Playfair Display
Used for:
- Main headings (h1, h2, h3)
- Section titles
- Project titles

```html
<h1 class="hero-title">Title</h1>
```

### Body Font: Montserrat
Used for:
- Paragraphs
- Navigation
- Labels
- Descriptions

```css
font-family: 'Montserrat', sans-serif;
font-weight: 300; /* Light */
font-weight: 400; /* Regular */
font-weight: 500; /* Medium */
font-weight: 600; /* Semibold */
font-weight: 700; /* Bold */
```

## Color System

### Primary Colors
- **Black**: #000000 (primary text, borders)
- **White**: #ffffff (backgrounds)
- **Gray**: #888888 (secondary text, accents)
- **Light**: #f5f5f5 (section backgrounds)
- **Dark**: #0a0a0a (footer, deep backgrounds)

## Spacing Scale

```css
--spacing-xs: 0.5rem    /* 8px */
--spacing-sm: 1rem      /* 16px */
--spacing-md: 2rem      /* 32px */
--spacing-lg: 3rem      /* 48px */
--spacing-xl: 4rem      /* 64px */
--spacing-2xl: 6rem     /* 96px */
```

## Transitions

```css
--transition-fast: 200ms ease-in-out
--transition-standard: 300ms ease-in-out
--transition-slow: 500ms ease-in-out
```

## Design Principles

### 1. Architectural Clarity (Virgil Abloh)
- Geometric shapes with clear borders
- Large typography with precision
- Strategic whitespace
- Grid-based layouts

### 2. Structural Refinement (Matthew Williams)
- Precise measurements
- Fine details and accents
- Hierarchical organization
- Subtle visual relationships

### 3. Deconstructed Luxury (Maison Margiela)
- Layered elements
- Border frames and boxes
- Asymmetric compositions
- Strategic minimalism

## Component Guidelines

### Buttons
```html
<a href="#" class="btn btn-primary">Primary Button</a>
<a href="#" class="btn btn-secondary">Secondary Button</a>
```

**States:**
- Default
- Hover: Color inversion
- Active: Slight elevation

### Cards
```html
<div class="research-card">
  <div class="card-number">01</div>
  <h3>Card Title</h3>
  <p>Description text</p>
</div>
```

**Features:**
- Minimal border treatment
- Hover: subtle lift and shadow
- Responsive grid layout

### Tags
```html
<span class="tag">Tag Label</span>
```

**Interactive:**
- Hover: background highlight
- Border color change on focus

## Layout System

### Container
Max-width: 1400px
Margin: 0 auto
Padding: responsive (var(--spacing-lg) on desktop)

### Grid Examples

Two-column layout (uses CSS Grid):
```css
grid-template-columns: 1fr 1fr;
gap: var(--spacing-2xl);
```

Responsive auto-fit:
```css
grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
```

## Responsive Breakpoints

```css
/* Desktop: 1200px+ */
/* Tablet: 768px - 1199px */
/* Mobile: Below 480px */

@media (max-width: 768px) {
  /* Tablet/Mobile styles */
}

@media (max-width: 480px) {
  /* Mobile-only styles */
}
```

## Animation Guidelines

### Scroll Animations
- Elements fade in as user scrolls to them
- Slight upward transform (20px)
- 500ms duration

### Hover Animations
- Buttons: translateY(-2px)
- Cards: translateY(-5px)
- Links: underline expansion
- 300ms duration

### Parallax
- Hero section: Subtle movement on scroll
- Rate: 0.5x scroll position

## Accessibility Considerations

✓ Sufficient color contrast (AA standard)
✓ Semantic HTML structure
✓ Focus states on interactive elements
✓ Descriptive link text
✓ Proper heading hierarchy
✓ Alternative text for visual content

## Performance Optimization

1. **CSS**
   - Minimal external dependencies
   - GPU-accelerated transforms
   - Efficient selectors

2. **JavaScript**
   - Debounced scroll listeners
   - Passive event listeners
   - No render-blocking scripts

3. **Images**
   - Geometric shapes via CSS (no image files needed)
   - Optimized formats
   - Lazy loading where applicable

## Browser Compatibility

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## Customization Examples

### Change Primary Color
```css
:root {
    --color-primary: #your-color;
}
```

### Add New Section
```html
<section class="new-section">
    <div class="section-header">
        <h2>Section Title</h2>
        <div class="header-line"></div>
    </div>
    <!-- Content -->
</section>
```

### Modify Spacing
```css
/* All padding/margins use CSS variables */
padding: var(--spacing-lg);
margin-bottom: var(--spacing-md);
```

---

For implementation questions or customization help, refer to the source files or the README.md

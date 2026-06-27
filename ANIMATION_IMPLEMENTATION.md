# Animation Implementation Guide

## Overview
This document outlines all the new animations added to the PICT OSS Community website to enhance user experience.

## Animation Classes & Utilities

### Smooth Transitions
- **`.transition-smooth`** - Standard 0.3s smooth transition
- **`.transition-smooth-fast`** - Quick 0.15s transition
- **`.transition-smooth-slow`** - Slow 0.5s transition

### Button Animations
- **`.btn-hover`** - Button lifts on hover with shadow
  - Hover: `translateY(-2px)` with `box-shadow: 0 6px 12px`
  - Active: Returns to original position

### Link Animations  
- **`.link-hover`** - Animated underline on hover
  - Creates animated `::after` pseudo-element
  - Underline grows from left to right on hover

### Interactive Effects
- **`.hover-scale`** - Scale to 1.05 on hover
- **`.hover-slide`** - Slide right 4px on hover
- **`.hover-glow`** - Blue glow effect on hover
- **`.color-transition`** - Smooth color/background transitions

### Keyframe Animations

#### Page Load
- **`pageSlideIn`** - Slide up with fade-in (0.4s)
- **`scaleIn`** - Scale from 0.95 to 1 with fade-in

#### Interactive
- **`buttonPress`** - Compress/release effect (0.2s)
- **`staggerSlideIn`** - Staggered list animations
  - Items 1-7 with delays from 0.05s to 0.35s

#### Navigation
- **`.nav-active::after`** - Animated active nav indicator
  - Slides in from top with `slideInUp` animation

## Usage Examples

### Button with Hover Animation
```jsx
<button className="btn-hover pixelated-border bg-blue-500">
  Click Me
</button>
```

### Link with Underline Animation
```jsx
<a href="#" className="link-hover text-blue-500">
  Hover over me
</a>
```

### Scaled Hover Effect
```jsx
<div className="hover-scale cursor-pointer">
  Hover to scale
</div>
```

### Staggered List Items
```jsx
<ul>
  {items.map((item, i) => (
    <li key={i} className="stagger-in-item">
      {item}
    </li>
  ))}
</ul>
```

## Accessibility Considerations

✅ All animations respect `prefers-reduced-motion`
✅ No animations for users with motion sensitivity
✅ Keyboard navigation unaffected
✅ Focus states maintained
✅ Page functionality works without animations

## Performance

- Uses GPU-accelerated properties (`transform`, `opacity`)
- No layout thrashing
- CSS-based (not JavaScript)
- Minimal bundle size impact
- No performance degradation

## Browser Support

| Browser | Support |
|---------|----------|
| Chrome  | ✅ Full  |
| Firefox | ✅ Full  |
| Safari  | ✅ Full  |
| Edge    | ✅ Full  |
| IE 11   | ⚠️ Partial (transitions only) |

## Future Enhancements

- [ ] Framer Motion integration for complex animations
- [ ] Intersection Observer for scroll animations
- [ ] Page transition animations between routes
- [ ] Micro-interactions for form feedback
- [ ] Entrance animations for modals

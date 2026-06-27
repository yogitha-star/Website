# Pull Request: Add Subtle Animations to the Website

## Description
This PR implements subtle, non-intrusive animations for UI elements to enhance user experience and make the website feel more engaging.

## Changes Made

### 1. **Smooth Transition Utilities**
- Added `.transition-smooth` (0.3s)
- Added `.transition-smooth-fast` (0.15s)
- Added `.transition-smooth-slow` (0.5s)

### 2. **Button Hover Animations**
- `.btn-hover` - Lifts button on hover with shadow effect
- Smooth `translateY(-2px)` on hover
- Subtle box-shadow for depth

### 3. **Link Hover Effects**
- `.link-hover` - Animated underline that grows on hover
- `::after` pseudo-element with smooth width transition

### 4. **Interactive Hover Effects**
- `.hover-scale` - Scales elements to 1.05 on hover
- `.hover-slide` - Slides element right by 4px
- `.hover-glow` - Adds blue glow effect
- `.color-transition` - Smooth color changes

### 5. **Page & Component Animations**
- `pageSlideIn` - Smooth page load animation
- `buttonPress` - Press animation feedback (0.2s)
- `staggerSlideIn` - Staggered list item animations with delays from 0.05s to 0.35s

### 6. **Navigation Enhancements**
- Updated `.nav-active::after` with smooth slide-in animation

### 7. **Scrollbar Improvements**
- Added smooth transitions to scrollbar thumb
- Hover effect with color change

## Performance & Accessibility
- All animations respect `prefers-reduced-motion` media query
- Uses cubic-bezier timing functions for smooth feel
- No performance impact on animations
- Maintains retro pixel art aesthetic

## Browser Support
- All modern browsers (Chrome, Firefox, Safari, Edge)
- Graceful degradation in older browsers

## Testing
Before merging, please verify:
- [ ] Animations work smoothly in all supported browsers
- [ ] Animations respect reduced motion preferences
- [ ] No jank or performance issues
- [ ] Mobile responsiveness maintained

## Related Issue
Closes #10

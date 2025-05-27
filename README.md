# AI Evolution Group - Landing Page

A modern, responsive landing page for AI chatbot services with a dark theme and conversion-optimized design.

## Features

### ✨ Design & UX
- **Dark Theme**: Sleek, minimalist design with cyan and orange accent colors
- **Responsive Layout**: Optimized for desktop, tablet, and mobile devices
- **Smooth Animations**: Fade-in effects, hover animations, and scroll-triggered animations
- **Modern Typography**: Clean, readable fonts with proper hierarchy

### 🚀 Performance
- **Single File**: All CSS and JavaScript embedded for fast loading
- **Optimized Images**: SVG icons and CSS gradients instead of heavy images
- **Smooth Scrolling**: Native CSS smooth scrolling with JavaScript enhancements
- **Scroll Indicator**: Visual progress bar at the top of the page

### 📱 Navigation
- **Sticky Header**: Fixed navigation that becomes more opaque on scroll
- **Smooth Scrolling**: Clicking nav links smoothly scrolls to sections
- **Mobile Responsive**: Navigation adapts to smaller screens

### 💼 Services Showcase
Four main services with detailed pricing:

1. **Website AI Chatbot Integration**
   - Standard: €50/month
   - Premium: €70/month

2. **Omnichannel AI Chatbot Integration**
   - Standard: €70/month
   - Premium: €90/month

3. **AI Reactivation Campaigns** (Special highlight)
   - Performance-based: 20% revenue share

4. **AI Lead Magnet Funnel**
   - Custom pricing

### 🎯 Conversion Elements
- **Clear CTAs**: Multiple call-to-action buttons throughout the page
- **Demo Request**: Prominent demo button with special styling
- **Trust Indicators**: Feature icons and benefit highlights
- **Social Proof Ready**: Structure ready for testimonials/logos

## File Structure

```
├── index.html          # Main landing page (complete with CSS/JS)
└── README.md          # This documentation
```

## Customization

### Colors
The color scheme is defined in CSS custom properties at the top of the file:

```css
:root {
    --primary-color: #00d4ff;      /* Cyan blue */
    --secondary-color: #0099cc;    /* Darker cyan */
    --accent-color: #ff6b35;       /* Orange */
    --bg-dark: #0a0a0a;           /* Main background */
    --bg-card: #1a1a1a;          /* Card backgrounds */
    /* ... more colors */
}
```

### Content Updates
1. **Company Name**: Update "AI Evolution Group" in the navigation and footer
2. **Services**: Modify service descriptions and pricing in the services section
3. **Contact Info**: Update the demo request functionality in the JavaScript section

### Demo Button Functionality
Currently shows an alert. To implement real functionality, update the `requestDemo()` function:

```javascript
function requestDemo() {
    // Option 1: Redirect to booking system
    window.open('https://calendly.com/your-booking-link', '_blank');
    
    // Option 2: Open email client
    window.location.href = 'mailto:demo@yourcompany.com?subject=Demo Request';
    
    // Option 3: Redirect to contact form
    window.location.href = '/contact';
}
```

## Browser Support
- Chrome/Edge 88+
- Firefox 85+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance Tips
- The page loads quickly due to embedded CSS/JS
- Images are minimal (only SVG patterns and emoji icons)
- Animations are GPU-accelerated for smooth performance
- Lazy loading is implemented for scroll-triggered animations

## SEO Optimization
- Semantic HTML structure
- Meta description included
- Proper heading hierarchy (H1, H2, H3)
- Alt text ready for when you add real images

## Next Steps
1. **Analytics**: Add Google Analytics or your preferred tracking
2. **Forms**: Implement contact forms with backend processing
3. **CMS**: Consider integrating with a headless CMS for easy content updates
4. **A/B Testing**: Test different headlines, CTAs, and pricing presentations
5. **Real Images**: Replace emoji icons with professional graphics/photos

## License
This landing page template is ready for commercial use for AI Evolution Group. 
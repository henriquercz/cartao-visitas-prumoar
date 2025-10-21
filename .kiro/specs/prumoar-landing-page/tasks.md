# Implementation Plan - PrumoAr Landing Page

- [ ] 1. Create base HTML structure with meta tags and CSS variables
  - Create index.html file with DOCTYPE, html lang="pt-BR", and head section
  - Add all required meta tags (charset, viewport, description, Open Graph tags)
  - Add Google Fonts link for Poppins and Inter font families
  - Add Font Awesome CDN link for icons
  - Define CSS custom properties (:root) for colors, spacing, typography, and effects
  - Set up base body styles with grid background CSS
  - _Requirements: 1.1, 1.2, 1.4, 1.5, 10.1, 10.2, 10.3, 10.4, 10.5_

- [x] 2. Implement animated grid background and spotlight effect




  - [x] 2.1 Create grid background pattern with CSS





    - Write CSS for .grid-background class with linear-gradient pattern
    - Set background-size to 50px x 50px for desktop
    - Add media query for mobile (<768px) with 30px x 30px grid
    - Add subtle background-position animation over 60 seconds
    - _Requirements: 2.1, 2.5_
  -

  - [x] 2.2 Implement spotlight effect animation





    - Create .spotlight-effect div element in HTML body
    - Write CSS for circular spotlight with radial-gradient (300px diameter)
    - Implement @keyframes moveSpotlight animation with rectangular path
    - Set animation duration to 20 seconds with infinite loop
    - Add media query for mobile with 200px diameter spotlight
    - _Requirements: 2.2, 2.3, 2.4, 2.5_

- [ ] 3. Build hero section with logo and branding
  - Create semantic <header> and hero <section> elements
  - Add logo container with img element (placeholder or SVG)
  - Write h1 for company name "PrumoAr Instalações" with Poppins font
  - Add subtitle paragraph with tagline using Inter font
  - Include decorative snowflake icon from Font Awesome
  - Style hero section with responsive font sizes using clamp()
  - Implement fade-in animation on page load (800ms duration)
  - Add floating animation to logo element
  - _Requirements: 1.1, 1.3, 1.4, 1.5, 8.1_

- [ ] 4. Create service cards with glassmorphism effect
  - [ ] 4.1 Build service cards HTML structure
    - Create services <section> with .services-grid container
    - Add four .service-card divs with icon, title, and description
    - Use Font Awesome icons: fa-wind, fa-tools, fa-snowflake, fa-fan
    - Add service titles: "Instalação de Ar Condicionado Split", "Manutenção e Limpeza", "Refrigeração Comercial", "Automação de Fluxo de Ar"
    - _Requirements: 3.1, 3.3_
  -

  - [x] 4.2 Implement glassmorphism styling and grid layout



    - Write CSS for .service-card with rgba background and backdrop-filter blur
    - Add border, border-radius (16px), padding, and box-shadow
    - Style service icons in silver color (#C0C0C0)
    - Implement CSS Grid layout: 1 column mobile, 2 columns tablet, 4 columns desktop
    - Add hover effect with scale(1.05), translateY(-8px), and enhanced shadow
    - Set transition with cubic-bezier timing function
    - _Requirements: 3.2, 3.4, 3.5, 5.2, 5.3, 5.4_

- [ ] 5. Implement CTA section with WhatsApp and Email buttons
  - [ ] 5.1 Create CTA section HTML structure
    - Add CTA <section> with title "Entre em Contato Agora"
    - Add description paragraph "Solicite um orçamento sem compromisso"
    - Create two <a> buttons with .btn class for WhatsApp and Email
    - Add Font Awesome icons (fa-whatsapp, fa-envelope) inside buttons
    - Set href for WhatsApp (https://wa.me/5511985000118) and Email (mailto:adrianochagas25@hotmail.com)
    - _Requirements: 4.1, 4.2, 4.3, 4.4_
  
  - [ ] 5.2 Style CTA buttons with gradients and effects
    - Write CSS for .btn base styles (flexbox, min-width 280px, padding, pill shape)
    - Implement .btn-whatsapp with green gradient background (#25D366 to #1ea952)
    - Implement .btn-email with dark gradient background (#4A4A4A to #2C2C2C)
    - Add box-shadow with appropriate colors for each button
    - Create hover states with translateY(-4px), scale(1.02), and enhanced shadow
    - Add media query for mobile: full-width buttons stacked vertically with 24px gap
    - Add media query for desktop: buttons side-by-side horizontally
    - _Requirements: 4.1, 4.2, 4.5, 5.1_
  
  - [ ] 5.3 Add ripple effect to buttons with JavaScript
    - Write createRipple() function that creates span element on click
    - Calculate ripple position based on click coordinates
    - Add CSS for .ripple class with animation
    - Attach click event listeners to both CTA buttons
    - Remove ripple element after animation completes (600ms)
    - _Requirements: 4.5, 8.3_

- [ ] 6. Create contact information display section
  - Add contact-info <section> below CTA buttons
  - Create two .contact-item divs for phone and email
  - Add phone number "📞 +55 (11) 98500-0118" with icon
  - Add email "📧 adrianochagas25@hotmail.com" with icon
  - Style contact items with dark background cards and #B8B8B8 text color
  - Add subtle hover effect to contact items
  - _Requirements: 4.6_

- [ ] 7. Build footer with logo and copyright
  - Create semantic <footer> element
  - Add small grayscale version of PrumoAr logo
  - Add copyright text "© 2025 PrumoAr Instalações. Todos os direitos reservados."
  - Style footer with rgba(0, 0, 0, 0.8) background
  - Apply generous padding (48px) and center content
  - Set text color to #B8B8B8
  - _Requirements: 9.1, 9.2, 9.3, 9.4, 9.5_
-

- [x] 8. Implement scroll animations with Intersection Observer




  - Write JavaScript function initScrollAnimations() using Intersection Observer API
  - Create observer for service cards with threshold 0.1
  - Add .fade-in class to elements when they enter viewport
  - Write CSS for fade-in animation (opacity 0 to 1, translateY 20px to 0)
  - Set animation duration to 600ms with staggered delays
  - Add smooth scroll behavior to html element (scroll-behavior: smooth)
  - _Requirements: 8.2, 8.4, 6.3_
-

- [x] 9. Add accessibility features and semantic improvements




  - Add ARIA labels to icon-only elements and decorative graphics
  - Ensure all interactive elements have visible focus states with silver outline
  - Verify semantic HTML structure (header, main, section, footer tags)
  - Add alt text to all images including logo
  - Test keyboard navigation for all interactive elements (Tab, Enter, Space)
  - Verify color contrast ratios meet WCAG AA standards
  - _Requirements: 7.1, 7.2, 7.3, 7.4, 7.5_

- [x] 10. Optimize performance and add final polish







  - [x] 10.1 Add performance optimizations



    - Add CSS containment (contain: layout style paint) to service cards
    - Add will-change: transform to spotlight effect
    - Ensure all animations use only transform and opacity properties
    - Verify all assets are inline (CSS and JavaScript in HTML file)
    - _Requirements: 6.1, 6.2, 6.5_


  
  - [x] 10.2 Add browser fallbacks and progressive enhancement
    - Write @supports rule for backdrop-filter fallback
    - Add system font stack fallback for Google Fonts
    - Add font-display: swap to Google Fonts link


    - Ensure core functionality works without JavaScript
    - _Requirements: 6.2_
  
  - [x] 10.3 Verify responsive behavior across breakpoints
    - Test layout at 320px, 375px, 768px, 1024px, 1440px, 1920px
    - Verify no horizontal scroll at any breakpoint
    - Confirm touch targets are minimum 44x44px on mobile
    - Test grid background and spotlight scaling on all devices
    - Verify button layout switches correctly (stacked vs side-by-side)
    - _Requirements: 5.1, 5.2, 5.3, 5.4, 5.5, 2.5_

- [ ]* 11. Testing and validation
  - [ ]* 11.1 Run accessibility audit
    - Test with axe DevTools browser extension
    - Verify WCAG 2.1 AA compliance
    - Test with screen reader (NVDA or JAWS)
    - Validate keyboard-only navigation
    - _Requirements: 7.1, 7.2, 7.3, 7.4, 7.5_
  
  - [ ]* 11.2 Performance testing
    - Run Lighthouse audit in Chrome DevTools
    - Verify FCP < 1.5s, LCP < 2.5s, CLS < 0.1
    - Test animation frame rate (should be 60fps)
    - Validate file size is optimized
    - _Requirements: 6.1, 6.2, 6.4_
  
  - [ ]* 11.3 Cross-browser testing
    - Test in Chrome, Firefox, Safari, Edge (latest versions)
    - Test on mobile Safari iOS and Chrome Android
    - Verify backdrop-filter fallback works in older browsers
    - Confirm all animations work smoothly across browsers
    - _Requirements: 6.2_

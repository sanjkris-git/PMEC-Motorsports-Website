Purdue Motorsports Engineering Club (PMEC) Website
The official club website for the Purdue Motorsports Engineering Club, built to showcase our engineering projects, team leadership, event accolades, and sponsorship opportunities. It serves as a central hub for prospective members and potential partners to see our work in both the Purdue Grand Prix and Autocross competitions.

Link to project: https://mecpurdue.com/

How It's Made:
Tech used: HTML5, CSS3, Vanilla JavaScript, Adobe Fonts (Typekit)

This project is a multi-page static website built from the ground up without relying on heavy frontend frameworks. By sticking to Vanilla HTML, CSS, and JS, I ensured a lightweight, fast-loading experience while maintaining complete control over the UI components and layout.

Here are a few key features I implemented:
1. Custom JavaScript Components: Instead of using heavy carousel libraries, I built a custom, responsive team carousel (our-team.html) using Vanilla JS that supports touch-swipe for mobile devices, keyboard navigation, and automatic looping. I also built a dynamic tab-switching interface for the Kart Selector (purdue-gp.html) to cleanly display driver and crew chief profiles without cluttering the page.
2. Responsive Layouts: The site relies heavily on CSS Flexbox and media queries to ensure a seamless experience across desktop, tablet, and mobile. The navigation bars, image galleries, and layout grids stack intelligently on smaller viewports.
3. Dynamic Visuals: Implemented an infinite-scrolling sponsor track (sponsorship.html) using CSS keyframe animations, and integrated a background HTML5 video on the landing page with custom overlay elements.

**Optimizations**
While building the site, I focused heavily on accessibility and performance optimizations:
1. Accessibility & Reduced Motion: I implemented @media (prefers-reduced-motion: reduce) media queries and corresponding JavaScript logic. If a user has "reduce motion" enabled on their OS, the site automatically disables the infinite sponsor scroll animation and pauses the background hero video.
2. GPU Hardware Acceleration: For the continuous sponsor banner scrolling animation, I used transform: translate3d() rather than animating the left or margin properties. This offloads the animation to the GPU, preventing layout thrashing and resulting in a much smoother, jank-free scroll.
3. No Dependency Bloat: By writing the interactivity (carousel, kart selector tabs, autoplay video fallbacks) entirely in Vanilla JS and using raw CSS for the styling, I completely eliminated the need to load external libraries like jQuery or Bootstrap, drastically reducing the time to interactive (TTI) on page load.
4. Smart Stacking Contexts: Carefully managed z-index and stacking contexts across mobile media queries to ensure fixed navigation banners seamlessly float above the page content without overlapping interactive elements or imagery.

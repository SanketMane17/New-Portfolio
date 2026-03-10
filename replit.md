# Portfolio Website

A modern, responsive portfolio website built with React, TypeScript, and Tailwind CSS.

## Features

- **Responsive Design**: Works seamlessly on all devices
- **Modern UI**: Dark mode with neon accent colors (cyan, violet, amber)
- **Portfolio Showcase**: Display of featured projects with descriptions and tech stacks
- **Interactive Navigation**: Smooth scrolling and navigation between sections
- **Projects Section**: Three featured projects:
  - StreamMate (Video Conferencing Platform)
  - QKart (E-commerce Application)
  - Fintech Accounting Platform

## Technology Stack

- **Frontend**: React 18, TypeScript, Tailwind CSS
- **Build Tool**: Vite
- **Backend**: Express.js (Node.js)
- **UI Components**: Shadcn UI
- **Styling**: Custom CSS with glass-morphism effects
- **Routing**: Wouter

## Project Structure

```
/client/src/
  ├── pages/
  │   └── portfolio.tsx          # Main portfolio page
  ├── components/
  │   ├── layout/                # Navbar, Footer
  │   ├── sections/              # Hero, About, Projects, Experience, Contact
  │   └── ui/                    # Shadcn UI components
  ├── lib/                       # Utility functions and query client
  └── index.css                  # Global styles with custom variables

/server/
  ├── index.ts                   # Express app setup
  ├── vite.ts                    # Vite setup for dev
  └── routes.ts                  # API routes

/shared/                         # Shared types and schemas
```

## Local Development

```bash
npm run dev    # Start development server (runs on port 5000)
npm run build  # Build for production
npm run start  # Start production server
```

## Deployment

### Netlify

The project is configured for Netlify deployment with the following setup:

1. **netlify.toml** - Configuration file with:
   - Build command: `npm run build`
   - Publish directory: `dist`
   - Redirect rules for SPA routing

2. **Build Output**: The production build outputs to the `dist/` directory

3. **Deployment Steps**:
   - Connect your repository to Netlify
   - Netlify will automatically detect `netlify.toml`
   - The site will be built and deployed on every push

### Environment Variables

No environment variables are required for this portfolio website.

## Screenshots Included

The portfolio now displays three featured projects with screenshots:
1. **Screenshot_2026-03-06_at_1.53.30_PM_1773165399053.png** - StreamMate
2. **Screenshot_2026-03-06_at_1.53.43_PM_1773165399054.png** - QKart
3. **Screenshot_2026-03-06_at_1.55.05_PM_1773165399054.png** - Fintech Platform

All screenshots are imported and displayed in the Projects section.

## Styling

- **Color Scheme**: 
  - Background: Deep dark (#0A0A0F)
  - Primary: Neon Cyan (#00F5FF)
  - Accent: Violet (#7C3AED)
  - Secondary: Amber (#F59E0B)
  
- **Effects**: Glass-morphism cards, gradient text, neon glows, smooth animations

## Notes

- The app is fully responsive and mobile-friendly
- All images are optimized and use the @assets alias
- The build is optimized for production with code splitting and minification

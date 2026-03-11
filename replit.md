# Portfolio Website

A modern, responsive, fully client-side portfolio website built with React, TypeScript, and Tailwind CSS.

## Features

- **Fully Client-Side**: No backend needed - ready for free Netlify hosting
- **Responsive Design**: Works seamlessly on all devices
- **Modern UI**: Dark mode with neon accent colors (cyan, violet, amber)
- **Portfolio Showcase**: Display of featured projects with descriptions and tech stacks
- **Interactive Navigation**: Smooth scrolling and navigation between sections
- **Netlify Forms Integration**: Contact form sends messages directly to Netlify (no server needed)
- **Projects Section**: Three featured projects:
  - StreamMate (Video Conferencing Platform)
  - QKart (E-commerce Application)
  - BizPe (Fintech Platform)

## Technology Stack

- **Frontend**: React 18, TypeScript, Tailwind CSS
- **Build Tool**: Vite
- **UI Components**: Shadcn UI
- **Forms**: EmailJS with react-hook-form & Zod validation (client-side only, no backend)
- **Email Library**: EmailJS (free tier) for sending emails
- **Validation**: Zod schema with email validation, real-time error messages
- **Styling**: Custom CSS with glass-morphism effects
- **Routing**: Wouter
- **No Backend**: Fully static site for Netlify deployment

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

### Netlify (Recommended - Free)

The project is configured for **free** Netlify deployment with the following setup:

1. **netlify.toml** - Configuration file with:
   - Build command: `npm run build`
   - Publish directory: `dist`
   - Redirect rules for SPA routing
   - Netlify Forms integration for contact form

2. **Build Output**: The production build outputs to the `dist/` directory

3. **Deployment Steps**:
   - Push code to GitHub
   - Connect repository to Netlify (netlify.com)
   - Netlify auto-detects `netlify.toml` and deploys
   - Form submissions appear in Netlify dashboard

4. **Zero Costs**:
   - Free Netlify hosting for static sites
   - Free form submissions
   - No backend server needed
   - No database fees

### Environment Variables

**No environment variables required** - this is a fully client-side static site.

## Screenshots Included

The portfolio displays three featured projects with screenshots:
1. **StreamMate** - Video conferencing platform
2. **QKart** - E-commerce application
3. **BizPe** - Fintech platform for SMBs in India

All screenshots dynamically adjust aspect ratios and are optimized for display.

## Styling

- **Color Scheme**: 
  - Background: Deep dark (#0A0A0F)
  - Primary: Neon Cyan (#00F5FF)
  - Accent: Violet (#7C3AED)
  - Secondary: Amber (#F59E0B)
  
- **Effects**: Glass-morphism cards, gradient text, neon glows, smooth animations

## Backend Removed

All backend code has been removed:
- ❌ No Express.js server for forms
- ❌ No database connection
- ❌ No API endpoints
- ✅ Contact form uses Netlify Forms (client-side only)

## Email Integration

The portfolio uses **EmailJS** for sending contact form messages directly to your email:
- **Service**: Free EmailJS tier (no backend needed)
- **Email Delivery**: Messages sent to msanket450@gmail.com
- **Client-Side Only**: No server required - works on static Netlify deployment

### Setup Instructions

1. **Create EmailJS Account**
   - Go to [emailjs.com](https://www.emailjs.com)
   - Sign up for free account
   - Verify your email address

2. **Configure Email Service**
   - Add a new service (Gmail, Outlook, etc.)
   - Get your **Service ID**
   - Create a template with variables: `{from_name}`, `{from_email}`, `{message}`, `{reply_to}`
   - Get your **Template ID**
   - Copy your **Public Key** from Account page

3. **Set Environment Variables**
   - Create `.env.local` with:
     ```
     VITE_EMAILJS_PUBLIC_KEY=your_public_key
     VITE_EMAILJS_SERVICE_ID=your_service_id
     VITE_EMAILJS_TEMPLATE_ID=your_template_id
     ```
   - Variables with `VITE_` prefix are exposed to the frontend

## Form Validation

The contact form includes comprehensive client-side validation:
- **Name**: 2-100 characters required
- **Email**: Valid email format required (RFC 5322 compliant)
- **Message**: 10-1000 characters required
- **Real-time Feedback**: Validation on blur with inline error messages
- **Error Display**: Alert icons with descriptive messages
- **Visual Feedback**: Red border and focus ring on invalid fields

Validation is implemented using:
- `Zod` for schema definition and type inference
- `react-hook-form` for form state management
- `@hookform/resolvers/zod` for integration
- `emailjs-com` for email delivery

## Notes

- The app is fully responsive and mobile-friendly
- All images use dynamic aspect ratios
- The build is optimized for production with code splitting and minification
- Zero server costs - fully static site
- Contact form validates all fields before submission to Netlify

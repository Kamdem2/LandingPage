# Emerson Empire LLC - Landing Page

A modern, fully responsive landing page for The Emerson Empire LLC - the unified command center connecting The Emerson Agency LLC and the Emerson Professional Development Group.

## 🎨 Project Overview

This is a premium dark-themed landing page built with React, TypeScript, and Vite. The design features a sophisticated color palette with gold accents, teal highlights, and a deep navy background.

### Color Palette
- **Primary Background**: `#0a0e27` (Deep Navy)
- **Card Background**: `#0f1629` (Darker Navy)
- **Primary Accent**: `#d4af37` (Gold)
- **Secondary Accent**: `#4db8a8` (Teal)
- **Text Primary**: `#ffffff` (White)
- **Text Secondary**: `#a8b5d4` (Light Blue-Gray)

## 📦 Tech Stack

- **Framework**: React 19.2.5
- **Language**: TypeScript
- **Build Tool**: Vite
- **Styling**: CSS3 with CSS Variables
- **CSS Framework**: Tailwind CSS 4.2.4

## 🚀 Quick Start

### Installation

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Run linting
npm run lint
```

The development server will start at `http://localhost:5173`

## 📁 Project Structure

```
src/
├── components/
│   ├── LandingPage.tsx       # Main landing page component
│   ├── Dashboard.tsx          # Dashboard module
│   ├── IntakeForm.tsx         # Intake form module
│   ├── ClientTable.tsx        # Client management table
│   └── StatusCard.tsx         # Status display card
├── styles/
│   └── landingpage.css        # Landing page styles (CSS variables, responsive design)
├── context/
│   └── ClientContext.tsx      # Client data context
├── types/
│   └── client.ts              # Type definitions
├── App.tsx                    # Main app component
├── main.tsx                   # Entry point
├── index.css                  # Global styles
└── App.css                    # App-specific styles

public/                        # Static assets
dist/                          # Production build output
```

## 🎯 Pages

### Landing Page
The main landing page featuring:
- **Navigation Bar** - Sticky navigation with links
- **Hero Section** - Bold headline with CTAs
- **Metrics Dashboard** - Command center statistics
- **Modules Section** - Agency Ops and Dev Group modules
- **Call-to-Action** - Engagement section
- **Newsletter Signup** - Email subscription form
- **Footer** - Links and social media

### Dashboard & Intake Form
Additional modules accessible from the app navigation.

## 🎨 Styling

All styles are defined in `src/styles/landingpage.css` using CSS custom properties (variables):

```css
:root {
  --color-dark-bg: #0a0e27;
  --color-gold: #d4af37;
  --color-teal: #4db8a8;
  --font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", ...;
  /* ... more variables */
}
```

### Responsive Design
- **Desktop**: 1280px and above
- **Tablet**: 768px - 1024px
- **Mobile**: Below 640px

All layouts automatically adapt to screen size with responsive grids and flexible typography.

## 🎯 Key Features

✅ **Fully Responsive** - Mobile-first design works on all devices  
✅ **Dark Theme** - Professional premium appearance  
✅ **Accessibility** - Semantic HTML, good contrast ratios  
✅ **Performance** - Optimized CSS, minimal bundle size  
✅ **Interactive Elements** - Hover effects, form validation  
✅ **Form Handling** - Email subscription with validation  
✅ **Social Integration** - Social media links in footer  

## 📝 Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start Vite dev server |
| `npm run build` | Build for production (TypeScript + Vite) |
| `npm run lint` | Run ESLint on codebase |
| `npm run preview` | Preview production build locally |

## 🔧 Configuration Files

- `vite.config.ts` - Vite bundler configuration
- `tsconfig.json` - TypeScript compiler options
- `tsconfig.app.json` - App-specific TypeScript settings
- `tsconfig.node.json` - Node-specific TypeScript settings
- `eslint.config.js` - ESLint rules and configuration
- `index.html` - HTML entry point

## 📧 Contact & Modules

The landing page includes contact information and module links:
- **Email**: info@emersonempire.com
- **Agency Ops Module**: Task management and project tracking
- **Professional Development Group**: Courses and learning platform

## 🎓 Learning & Development

This project serves as a template for:
- Building responsive React applications with TypeScript
- Implementing CSS variables for consistent theming
- Using Vite for modern, fast development
- Creating professional landing pages
- Form handling and validation in React

## 📄 License

© 2026 The Emerson Empire LLC. All Rights Reserved.

## 🤝 Contributing

To contribute to this project:
1. Create a new branch for your feature
2. Make your changes
3. Test thoroughly on mobile and desktop
4. Submit a pull request

---

**Last Updated**: May 7, 2026
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

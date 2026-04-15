# Rahul Gavit — Portfolio

A single-page Nuxt 3 + Vue 3 portfolio with dark mode, smooth animations, and resume download.

## Setup

```bash
npm install
npm run dev      # Development server → http://localhost:3000
npm run generate # Static build (for Netlify / Vercel)
```

## Add Your Resume

Place your PDF at: `public/Rahul_Awesome_Resume.pdf`

## Deploy to Netlify

```bash
npm run generate
# Upload the `.output/public` folder to Netlify
```

## Features

- Dark / Light mode toggle (auto-detects system preference)
- Sticky navbar with active section highlighting
- Animated hero with cursor glow effect
- Timeline-based experience section
- Project cards with stack tags and links
- Responsive for all screen sizes (mobile-first)
- Resume download button in Navbar + Contact section

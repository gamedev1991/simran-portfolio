# Simran Malhotra — Strategic Brand Communications Portfolio

A personal portfolio website showcasing 10+ years of brand communications and content strategy expertise, designed with an editorial credibility-first approach.

## Overview

This portfolio site demonstrates Simran Malhotra's work as a Strategic Brand Communications & Business Storyteller, featuring:

- **10+ years** of experience across start-ups, Fortune 500s, and listed companies
- **100+ businesses** served across sectors, industries, and countries
- **Proven outcomes** including 114% brand value growth, ₹200cr+ campaigns, and 300K+ monthly traffic growth

## Design Philosophy: Proof + Craft

The site follows a "proof + craft" pattern—pairing specific, quantified outcomes with recognizable clients alongside persuasive, well-crafted prose. This approach demonstrates both expertise through evidence and communication skill through the writing itself.

### Key Sections

1. **Hero** — Professional photo, compelling positioning statement, brief value proposition, and primary CTA
2. **Client Strip** — Social-proof row of the companies and agencies she's worked with (Suzlon Group, Repos Energy, GWEC, BCG, KPMG)
3. **Proof Bar** — Four quantified statistics highlighting career achievements
4. **Case Studies** — Three selected roles (Suzlon Group, Repos Energy, Freelance) presented as a horizontal scroll-snap card track, with narratives and outcome metrics
5. **About** — Short bio and a memorable brand philosophy quote
6. **Capabilities** — Core skill areas (Content Strategy, Campaign Communication, Thought Leadership, etc.) as interactive hover tags
7. **Contact** — Email, phone, LinkedIn, and location

## Technical Stack

- **HTML5** — Single-page, semantic markup
- **CSS3** — Hand-written styles with CSS custom properties for maintainable theming
  - Warm, editorial color palette: `#20201C` ink, `#FAF6EF` paper, `#B5652C` accent
  - Responsive grid layouts for proof bar and case studies
  - Horizontal scroll-snap track for case-study cards (no JS carousel library)
  - Hover/lift interactions on cards, tags, and CTAs
  - Soft radial-gradient hero band for visual depth
- **JavaScript** — Small dependency-free scroll-reveal effect using `IntersectionObserver`, respecting `prefers-reduced-motion`
- **Typography**
  - Display headlines: [Fraunces](https://fonts.google.com/specimen/Fraunces) (serif)
  - Body copy: [Public Sans](https://fonts.google.com/specimen/Public+Sans) (sans-serif)
  - Tabular numerals for statistics
- **Fonts** — Served via Google Fonts CDN (privacy-friendly, CSP-safe)
- **Responsive** — Mobile-first design; tested at 390px (mobile) and 1280px (desktop) viewports

## File Structure

```
simran-portfolio/
├── index.html          # Single-page portfolio (complete HTML + CSS + JS)
├── assets/
│   └── simran.png      # Hero headshot photo
└── README.md           # This file
```

## How to View

1. **Local preview**: Open `index.html` in any modern web browser
2. **Live deployment**: Host on any static web server (GitHub Pages, Netlify, Vercel, etc.)
3. **Artifact version**: Also available as a published interactive artifact for mobile preview and sharing

## Design Notes

- **No build step required** — Single HTML file with embedded CSS; Google Fonts loaded via CDN
- **Accessible** — Focus states on interactive elements, semantic HTML structure
- **Print-friendly** — Layout respects print media queries for professional printing
- **Performance** — Minimal external dependencies; fast initial load

## Content Sources

All role descriptions, dates, statistics, and outcomes are sourced from verified professional experience and achievement data. The writing demonstrates Simran's brand voice and storytelling approach.

## Browser Support

Works on all modern browsers:
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)
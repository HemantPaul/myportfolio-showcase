# Architecture Overview

> High-level system design — no implementation details are shared here.

---

## Application Layers

```
┌─────────────────────────────────────────────────────────────┐
│                        CLIENT LAYER                          │
│                                                              │
│   Next.js 14 App Router  ·  React 18  ·  TypeScript         │
│   Framer Motion  ·  GSAP  ·  Three.js / WebGL               │
│   Tailwind CSS  ·  Lenis Smooth Scroll                       │
└──────────────────────────┬──────────────────────────────────┘
                           │  Static / SSG
┌──────────────────────────▼──────────────────────────────────┐
│                      DELIVERY LAYER                          │
│                                                              │
│   Vercel Edge Network  ·  CDN  ·  Automatic HTTPS            │
│   Security Headers  ·  Image Optimization                    │
└──────────────────────────┬──────────────────────────────────┘
                           │  External APIs (optional)
┌──────────────────────────▼──────────────────────────────────┐
│                      SERVICES LAYER                          │
│                                                              │
│   Font CDN (Fontshare)  ·  Email Service (optional)          │
│   Analytics (optional)                                       │
└─────────────────────────────────────────────────────────────┘
```

---

## Rendering Strategy

| Section | Strategy | Reason |
|---|---|---|
| Hero / All Sections | Static Generation (SSG) | Zero server cost, instant load |
| 3D Canvas | Client-side only | WebGL requires browser APIs |
| Contact Form | Client-side | No backend required |
| Images / Fonts | CDN cached | Performance |

---

## Performance Approach

- Three.js scene loaded via **dynamic import** (prevents SSR errors, reduces initial bundle)
- Custom cursor loaded **client-side only** (no SSR flash)
- Animations driven by **CSS variables + GPU compositor** (avoids layout recalculation)
- Lenis scroll synced with **GSAP ticker** (single RAF loop, no jank)
- All section components use **`useInView`** to trigger animations only when visible

---

## Security Decisions

- No backend — static site, nothing to attack
- No API keys in the frontend
- Security headers set at the CDN edge layer
- All external links use `rel="noopener noreferrer"`

---

*The actual implementation is kept in a private repository.*

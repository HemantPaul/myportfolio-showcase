<div align="center">

<br/>

<!-- Replace with your own logo or remove -->
<img src="assets/logo.png" alt="HP Logo" width="80" height="80" style="border-radius:50%"/>

<br/><br/>

# Hemant Paul — MyPortfolio

### *A next-generation cinematic developer portfolio*

<br/>

[![Live Demo](https://img.shields.io/badge/🌐%20Live%20Demo-Visit%20Site-00d4ff?style=for-the-badge)](https://my-portfolio-kappa-flame-21.vercel.app)
&nbsp;
[![Status](https://img.shields.io/badge/Status-Live%20%26%20Active-00ff88?style=for-the-badge)](#)
&nbsp;
[![Made With](https://img.shields.io/badge/Made%20With-Next.js%2014-000000?style=for-the-badge&logo=nextdotjs)](https://nextjs.org)

<br/>

> **Not just a portfolio. A digital experience.**
>
> Built to feel like a fusion of an Apple keynote, a sci-fi OS, and an Awwwards-winning interaction design.

<br/>

**[🚀 View Live →](https://my-portfolio-kappa-flame-21.vercel.app)**

<br/>

---

</div>

## 🎯 Why I Built This

Most developer portfolios are templates. I wanted mine to be a statement.

The goal was to answer one question: **"Can a portfolio itself demonstrate a developer's skill level?"**

Every technical decision — the physics cursor, the WebGL orb, the scroll-triggered animations, the holographic glass cards — is intentional. It's not decoration. It's a live demo of what I can build.

> *When a recruiter lands on this page, I want them to feel the difference before they read a single word.*

---

## ✨ Features

### 🎬 Cinematic Experience
- **Digital boot sequence** — Custom loading screen with system-boot terminal copy and animated progress
- **Letter-by-letter hero reveal** — Staggered character animation with parallax depth
- **Scroll storytelling** — Every section animates into existence as you navigate
- **Section transitions** — No hard cuts; everything flows cinematically

### 🌌 3D & WebGL
- **Live Three.js hero scene** — Neural orb with particle field and three animated orbital rings
- **Mouse-reactive 3D** — The orb physically tracks your cursor in real time using lerp interpolation
- **Dynamic lighting** — Point lights follow the cursor and shift color based on position
- **Ambient particle field** — 200+ particles orbit the scene responding to interaction

### 🖱️ Advanced Interactions
- **Custom physics cursor** — Spring-damping cursor with a fading particle trail (8-particle trail system)
- **Magnetic buttons** — CTA buttons physically attract toward the cursor using motion values
- **3D card tilt** — Project cards tilt on X and Y axes tracking exact mouse position
- **Particle explosions** — Skill nodes emit bursts of particles on hover

### 🎨 Visual Design System
- **Glassmorphism** — Frosted-glass cards with holographic colour-shifting overlays
- **Cyber grid** — Animated perspective grid with neon blue lines throughout
- **Film grain** — SVG noise texture overlay for cinematic depth
- **Neon glow** — Dynamic `box-shadow` and `text-shadow` glow effects on all interactive elements
- **Gradient text** — Animated blue-to-purple gradient on headings via `background-clip`

### 📜 Scroll & Motion
- **Lenis smooth scrolling** — Eased, buttery scroll synced with GSAP ScrollTrigger
- **Parallax layers** — Background elements translate at different rates on scroll
- **Timeline animations** — Experience nodes pulse as they enter the viewport
- **Scroll velocity effects** — Animation speed adapts to scroll speed

### 📱 Production Quality
- **Fully responsive** — Works on mobile, tablet, and desktop
- **Performance optimised** — Three.js scene lazy-loaded, animations GPU-accelerated
- **Accessible** — Semantic HTML, ARIA labels, keyboard navigation support
- **Security headers** — X-Frame-Options, XSS protection, Referrer-Policy at edge

---

## 🏗️ High-Level Architecture

```
┌─────────────────────────────────────────────────────┐
│                    CLIENT LAYER                      │
│  Next.js 14 · React 18 · TypeScript · Tailwind CSS  │
│  Framer Motion · GSAP · Three.js · Lenis            │
└─────────────────────┬───────────────────────────────┘
                      │ Static Site (SSG)
┌─────────────────────▼───────────────────────────────┐
│                  DELIVERY LAYER                      │
│  Vercel Edge Network · CDN · HTTPS · Image Optim.   │
└─────────────────────────────────────────────────────┘
```

**Rendering:** 100% Static Generation (SSG) — zero server cost, instant global load times.

**3D Performance Strategy:** The Three.js canvas is loaded via dynamic import (client-side only), preventing SSR conflicts and keeping the initial JS bundle small.

**Animation Architecture:** All animations run on the GPU compositor thread using `transform` and `opacity` only — no layout recalculations, no jank.

→ See [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) for the full breakdown.

---

## 🛠️ Tech Stack

| Category | Technology | Purpose |
|---|---|---|
| **Framework** | Next.js 14 (App Router) | SSG, routing, performance |
| **Language** | TypeScript | Type safety across all components |
| **Styling** | Tailwind CSS | Utility-first design system |
| **3D / WebGL** | Three.js + React Three Fiber | Hero scene, orb, particles |
| **3D Helpers** | @react-three/drei | Stars, Float, MeshDistortMaterial |
| **Animation** | Framer Motion | Component animations, spring physics |
| **Animation** | GSAP + ScrollTrigger | Scroll-driven animations, timeline |
| **Smooth Scroll** | Lenis | Eased scroll synced with GSAP ticker |
| **Fonts** | Clash Display + Satoshi | Premium typographic identity |
| **Deployment** | Vercel | Edge CDN, automatic HTTPS, previews |

---



## 🚀 Live Deployment

| Environment | URL | Status |
|---|---|---|
| **Production** | [my-portfolio-kappa-flame-21.vercel.app](https://my-portfolio-kappa-flame-21.vercel.app) | 🟢 Live |

**Hosting:** Vercel (Hobby Plan)
**CDN:** Vercel Edge Network — served from the nearest global region
**Deploy time:** ~45 seconds from push to live
**Uptime:** 99.99% (Vercel SLA)

---

## 🔮 Future Improvements

- [ ] **Blog section** — MDX-powered technical writing
- [ ] **Case studies** — Deep-dive pages for each project
- [ ] **EmailJS integration** — Make the contact form actually send emails
- [ ] **Cursor audio** — Subtle ambient sound effects tied to interactions
- [ ] **Dark/Light mode** — System preference detection
- [ ] **GSAP page transitions** — Cinematic route change animations
- [ ] **Prefers-reduced-motion** — Full accessibility compliance
- [ ] **Lighthouse 100** — Push all four scores to 100
- [ ] **WebGL shader upgrades** — Custom GLSL vertex/fragment shaders on the orb
- [ ] **i18n** — Hindi / multilingual support

---

## 📬 Contact

<div align="center">

I'm open to full-time roles, internships, and interesting freelance projects.

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-my--portfolio--kappa--flame--21.vercel.app-00d4ff?style=for-the-badge)](https://my-portfolio-kappa-flame-21.vercel.app)

[![Email](https://img.shields.io/badge/Email-hemant.paul%40kiit.ac.in-ea4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:hemantpaul3011@gmail.com)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_HANDLE)

[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/HemantPaul)

<br/>

**Hemant Paul**
Full Stack Developer · KIIT University, Bhubaneswar
*Available for opportunities*

</div>

---

<div align="center">

© 2025 Hemant Paul · All Rights Reserved

*Source code is private and protected. This repository is a showcase only.*

</div>

# JIT ACM Student Chapter

<div align="center">

  <img src="public/images/jit-acm-logo.png" alt="JIT ACM Logo" width="100" />

  # JIT ACM Student Chapter
  ### Jhulelal Institute of Technology, Nagpur

  <p><strong>Advancing Computing. Building People.</strong></p>

  <p>
    The official website of the JIT ACM Student Chapter, presenting the chapter's technical initiatives, student projects, marquee events, and collaborative computing community.
  </p>

  <p>
    <a href="https://jit-acm.vercel.app">
      <img src="https://img.shields.io/badge/Live_Website-jit--acm.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Live Website" />
    </a>
    &nbsp;
    <a href="https://github.com/pranjalisantani/ACM_OFFICIAL_WEBSITE">
      <img src="https://img.shields.io/badge/Repository-ACM__OFFICIAL__WEBSITE-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Repository" />
    </a>
  </p>

  <p>
    <a href="https://nextjs.org"><img src="https://img.shields.io/badge/Next.js-16.3.5-000000?style=flat-square&logo=next.js&logoColor=white" alt="Next.js" /></a>
    <a href="https://react.dev"><img src="https://img.shields.io/badge/React-19.2.8-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React" /></a>
    <a href="https://www.typescriptlang.org"><img src="https://img.shields.io/badge/TypeScript-5.0-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" /></a>
    <a href="https://tailwindcss.com"><img src="https://img.shields.io/badge/Tailwind_CSS-v4.0-38B2AC?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" /></a>
    <a href="https://threejs.org"><img src="https://img.shields.io/badge/Three.js-WebGL-000000?style=flat-square&logo=three.js&logoColor=white" alt="Three.js" /></a>
    <a href="https://gsap.com"><img src="https://img.shields.io/badge/GSAP-3.15-88CE02?style=flat-square&logo=greensock&logoColor=white" alt="GSAP" /></a>
  </p>

</div>

---

## About the Project

The **JIT ACM Student Chapter** is the official computing society at **Jhulelal Institute of Technology (JIT)**, Nagpur, chartered by the **Association for Computing Machinery (ACM)**.

This repository contains the source code for the chapter's official website. Designed with an editorial dark aesthetic and interactive visual systems, the platform serves as the central hub for chapter activities, technical workshops, open-source projects, and student achievements.

---

## Core Features

- **3D Particle Background:** Persistent Three.js WebGL simulation responsive to cursor attraction and scroll velocity, with an automatic Canvas 2D 3D-perspective fallback when WebGL is unavailable.
- **Cinematic Opening Gateway:** Atmospheric particle constellation assembly introducing the chapter brand, accompanied by an ambient audio greeting and Web Speech Synthesis fallback.
- **Floating Capsule Navigation:** Glassmorphic navbar with IntersectionObserver scroll spy, glowing active indicator, mobile drawer, and integrated social links.
- **Marquee Events Showcase:** Timeline of chapter initiatives including competitive hackathons (*HackBlitz Season 3*), developer workshops (*Discover Docker*), and technical masterclasses (*GitHub MasterClass*).
- **Project Case Studies:** Dynamic slug-based routes (`/projects/[slug]`) pre-rendered at build time with technology stacks and external repository links.
- **Interactive Photo Stream:** Continuous horizontal photo reel featuring touch/drag interaction with inertial glide, hover pauses, and embedded metadata overlays.
- **Accessibility & Motion Preferences:** Native compliance with `prefers-reduced-motion` across all GSAP timelines and Three.js simulations, alongside keyboard skip navigation.
- **Technical SEO & Standards:** Edge-rendered OpenGraph cards (`opengraph-image.tsx`), automated XML sitemap (`sitemap.ts`), search directives (`robots.ts`), and Schema.org JSON-LD structured data.

---

## Technology Stack

| Layer | Technology | Version | Purpose |
| :--- | :--- | :--- | :--- |
| **Framework** | [Next.js](https://nextjs.org/) | `16.3.5` | App Router, static generation (SSG), server rendering |
| **UI Library** | [React](https://react.dev/) | `19.2.8` | Component model, React DOM 19, sync external store |
| **3D Graphics** | [Three.js](https://threejs.org/) | `^0.186.0` | 3D WebGL particle simulation and camera orchestration |
| **Animation** | [GSAP](https://greensock.com/gsap/) | `^3.15.0` | ScrollTrigger timelines and choreography |
| **Styling** | [Tailwind CSS](https://tailwindcss.com/) | `^4.0.0` | Utility-first CSS engine via `@tailwindcss/postcss` |
| **Language** | [TypeScript](https://www.typescriptlang.org/) | `^5.0.0` | Static type safety and data models |
| **Linting** | [ESLint](https://eslint.org/) | `^9.0.0` | Code quality enforcement via `eslint-config-next` |
| **Deployment**| [Vercel](https://vercel.com/) | Production | Edge delivery, static asset caching, headers |

---

## Architecture

```
        ┌─────────────────────────────────────────────────────────────┐
        │                     Typed Content Hub                       │
        │    (events.ts, team.ts, projects.ts, gallery.ts, site.ts)   │
        └──────────────────────────────┬──────────────────────────────┘
                                       │
                                       ▼
        ┌─────────────────────────────────────────────────────────────┐
        │                    Next.js 16 App Router                    │
        │   • Server-Side Rendering (SSR) & Static Generation (SSG)   │
        │   • Dynamic Case Study Routes (/projects/[slug])            │
        │   • Edge OpenGraph Previews & Automated XML Sitemap         │
        └──────────────────────────────┬──────────────────────────────┘
                                       │
                                       ▼ (Delivered to browser)
        ┌─────────────────────────────────────────────────────────────┐
        │                        Client Browser                       │
        │                      (Hydration & DOM)                      │
        └───────┬─────────────────────────────────────────────┬───────┘
                │                                             │
                ▼                                             ▼
 ┌─────────────────────────────┐               ┌─────────────────────────────┐
 │   Client Visual Layer       │               │   OpeningExperience & UI    │
 ├─────────────────────────────┤               ├─────────────────────────────┤
 │ • ParticleField (Three.js   │               │ • Opening Gateway Sequence  │
 │   3D WebGL background with  │               │ • Audio Greeting & Speech   │
 │   automatic Canvas fallback)│               │   Synthesis Fallback Engine │
 │ • ComputationalField (2D    │               │ • First-visit localStorage  │
 │   Canvas letter assembly)   │               │ • Floating Capsule Nav & Spy│
 └─────────────────────────────┘               └─────────────────────────────┘
```

<details>
  <summary><strong>Simulation &amp; Runtime Mechanics</strong></summary>
  <br />
  <ul>
    <li><strong>ParticleField:</strong> Runs a persistent 3D WebGL particle simulation reacting to pointer proximity, drag vectors, and scroll velocity. Automatically falls back to a custom Canvas 2D 3D-perspective projection renderer with pre-rendered radial sprites if WebGL is unavailable.</li>
    <li><strong>ComputationalField:</strong> Dedicated 2D Canvas spring-physics simulation powering the cinematic opening gateway, morphing identity particles into "ACM" and "JIT ACM".</li>
    <li><strong>Voice Engine:</strong> Preloads the chapter audio greeting (<code>/audio/acm-welcome.wav</code>) with fallback to the browser's Web Speech Synthesis API, respecting user mute preferences.</li>
  </ul>
</details>

---

## Project Structure

```text
ACM_OFFICIAL_WEBSITE/
├── public/
│   ├── audio/           # Chapter welcome audio (acm-welcome.wav)
│   ├── gallery/         # Event photo assets
│   ├── images/          # Institutional logos and sponsor SVGs
│   └── team/            # Member portraits (4:5 photoshoot crops)
├── src/
│   ├── app/             # Next.js App Router (pages, dynamic routes, SEO)
│   ├── components/      # UI primitives, navigation, opening & visual fields
│   ├── config/          # Opening timeline, population & physics constants
│   ├── content/         # Single-source-of-truth data modules
│   ├── lib/             # Voice engine, motion utilities & class helpers
│   └── types/           # TypeScript interface definitions
├── next.config.ts       # Next.js configuration and cache headers
├── package.json         # Project dependencies and npm scripts
├── tsconfig.json        # TypeScript configuration
└── vercel.json          # Vercel deployment and caching directives
```

<details>
  <summary><strong>Environment &amp; Asset Configuration Details</strong></summary>
  <br />
  <ul>
    <li><code>NEXT_PUBLIC_SITE_URL</code>: Optional override for OpenGraph and sitemap generation (defaults to <code>https://jit-acm.vercel.app</code> or Vercel system URL).</li>
    <li><code>/team/:path*</code>: Production asset caching configured via <code>vercel.json</code> and <code>next.config.ts</code> (<code>max-age=86400, stale-while-revalidate=604800</code>).</li>
  </ul>
</details>

---

## Getting Started

### Prerequisites

- **Node.js:** `^20.9.0` or higher
- **npm:** `^10.0.0` or higher

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/pranjalisantani/ACM_OFFICIAL_WEBSITE.git
   cd ACM_OFFICIAL_WEBSITE
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the local development server:**
   ```bash
   npm run dev
   ```

4. **Open the site:**
   Navigate to [http://localhost:3000](http://localhost:3000) in your browser.

### Available Commands

| Command | Description |
| :--- | :--- |
| `npm run dev` | Starts the development server with Turbopack |
| `npm run build` | Compiles an optimized production build |
| `npm start` | Serves the production build locally |
| `npm run lint` | Runs ESLint checks across the project |
| `npx tsc --noEmit` | Validates TypeScript types across the codebase |

---

## Deployment

The website is continuously deployed to **Vercel** with GitHub integration on pushes to the `main` branch:

- **Production URL:** [https://jit-acm.vercel.app](https://jit-acm.vercel.app)
- **Asset Caching:** HTTP caching headers (`public, max-age=86400, stale-while-revalidate=604800`) are applied via `vercel.json` and `next.config.ts` specifically to static member portraits under `/team/:path*`.

---

## Credits & Connect

Designed & Developed by Pranjali Santani for JIT ACM Student Chapter.

### Official Channels

- **Discord:** [Join Community](https://discord.gg/j3b4gw2QK)
- **LinkedIn:** [JIT ACM Student Chapter](https://www.linkedin.com/in/jit-acm-student-chapter/?isSelfProfile=false)
- **GitHub:** [@jitacm](https://github.com/jitacm)
- **Instagram:** [@acm_jit](https://www.instagram.com/acm_jit/)
- **X (Twitter):** [@jit_acm](https://x.com/jit_acm)
- **Email:** [acm@jitnagpur.edu.in](mailto:acm@jitnagpur.edu.in)

### Institutional Charter

- **Institution:** [Jhulelal Institute of Technology (JIT)](https://www.jitnagpur.edu.in/), Nagpur, India
- **Parent Organization:** [Association for Computing Machinery (ACM)](https://www.acm.org/)

```
ADVANCING COMPUTING. BUILDING PEOPLE.
© 2026 JIT ACM Student Chapter. All rights reserved.
```

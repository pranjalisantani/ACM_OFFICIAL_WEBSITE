# JIT ACM | Official Student Chapter Website

<div align="center">

  <img src="public/images/jit-acm-logo.png" alt="JIT ACM Student Chapter Crest" width="130" />

  # JIT ACM Official Student Chapter Website
  ### Jhulelal Institute of Technology, Nagpur

  <p align="center">
    <strong>Advancing Computing. Building People.</strong>
  </p>

  <p align="center">
    <strong>Designed &amp; Developed by Pranjali Santani for JIT ACM Student Chapter.</strong>
  </p>

  <p align="center">
    The premier digital portal of the Association for Computing Machinery (ACM) Student Chapter at Jhulelal Institute of Technology, Nagpur. Built with Next.js 16, React 19, TypeScript, Tailwind CSS v4, Three.js, and GSAP to deliver an immersive, accessible, and high-performance showcase of student leadership, marquee technical events, open-source projects, and community achievements.
  </p>

  <p align="center">
    <a href="https://jit-acm.vercel.app">
      <img src="https://img.shields.io/badge/Live_Website-jit--acm.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Live Deployment" />
    </a>
    <a href="https://github.com/pranjalisantani/ACM_OFFICIAL_WEBSITE">
      <img src="https://img.shields.io/badge/Repository-ACM__OFFICIAL__WEBSITE-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Repository" />
    </a>
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/Next.js-16.3.5-000000?style=flat-square&logo=next.js&logoColor=white" alt="Next.js" />
    <img src="https://img.shields.io/badge/React-19.2.8-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React" />
    <img src="https://img.shields.io/badge/TypeScript-5.0-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
    <img src="https://img.shields.io/badge/Tailwind_CSS-v4.0-38B2AC?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
    <img src="https://img.shields.io/badge/Three.js-WebGL-000000?style=flat-square&logo=three.js&logoColor=white" alt="Three.js" />
    <img src="https://img.shields.io/badge/GSAP-3.15-88CE02?style=flat-square&logo=greensock&logoColor=white" alt="GSAP" />
    <img src="https://img.shields.io/badge/Deployment-Vercel-000000?style=flat-square&logo=vercel&logoColor=white" alt="Vercel" />
  </p>

  <p align="center">
    <a href="#about-the-project">About</a> •
    <a href="#visual-showcase">Visual Showcase</a> •
    <a href="#architecture--visual-systems">Architecture</a> •
    <a href="#core-features">Features</a> •
    <a href="#technology-stack">Tech Stack</a> •
    <a href="#project-structure">Structure</a> •
    <a href="#getting-started">Getting Started</a> •
    <a href="#content-maintenance-guide">Maintenance</a> •
    <a href="#official-chapter-channels">Connect</a>
  </p>

</div>

---

## About the Project

The **JIT ACM Student Chapter** is the official computing society at **Jhulelal Institute of Technology (JIT)**, Nagpur, operating under charter from the **Association for Computing Machinery (ACM)**.

This repository contains the complete production codebase for the chapter's official website. Conceived, designed, and engineered as a modern digital flagship, the platform highlights the chapter's initiatives across education, technical craftsmanship, open-source innovation, and student mentorship.

### Institutional Identity & Mission Pillars

- **Institution:** Jhulelal Institute of Technology, Nagpur
- **Affiliation:** Association for Computing Machinery (ACM)
- **Motto:** *Advancing Computing. Building People.*
- **Core Pillars:**
  1. **Community:** A collaborative student-led engineering collective bridging computer science theory with practical craftsmanship and peer mentorship.
  2. **Events & Workshops:** Technical masterclasses, competitive hackathons, and industry speaker sessions designed to advance practical engineering competencies.
  3. **Projects:** Production-grade web platforms, developer tooling, and collaborative software projects authored and maintained by chapter members.
  4. **Learning & Mentorship:** Peer code reviews, systems architecture discussions, and career guidance bridging curriculum study with industry technology standards.

---

## Visual Showcase

The website incorporates high-contrast typography, interactive particle mechanics, and real photographic chronicles documenting chapter milestones and events:

| Event Milestone | Visual Record | Focus & Description |
| :--- | :---: | :--- |
| **HackBlitz Season 3** | <img src="public/gallery/evt-hackblitz.jpg" width="360" alt="HackBlitz Season 3 Team Photo" /> | Two-day competitive hackathon (HackBlitz Season 3) bringing together 177 student developers across 45 teams to architect, engineer, and deploy functional software prototypes. |
| **GitHub MasterClass** | <img src="public/gallery/evt-github-masterclass-speaker.jpg" width="360" alt="GitHub MasterClass Speaker Session" /> | Hands-on technical workshop covering distributed version control, branching workflows, collaborative pull requests, and open-source practices. |
| **SHIKHAR Gathering** | <img src="public/gallery/evt-shikhar.jpg" width="360" alt="SHIKHAR Event Photo" /> | Chapter delegates and participants convening at the annual technical summit and competitive showcase. |
| **Chapter Recognition** | <img src="public/gallery/evt-certificate-acm.jpg" width="360" alt="ACM Certificate Presentation" /> | Official chapter recognition ceremony celebrating executive contributions, student excellence, and academic milestones. |

---

## Architecture & Visual Systems

The web experience is organized into decoupled layers ensuring high visual fidelity, seamless animations, and fast initial rendering:

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
        │   • Dynamic OpenGraph Edge Card & Automated XML Sitemap     │
        └──────────────────────────────┬──────────────────────────────┘
                                       │
                                       ▼ (Delivered to)
        ┌─────────────────────────────────────────────────────────────┐
        │                        Client Browser                       │
        │                      (Hydration & DOM)                      │
        └───────┬─────────────────────────────────────────────┬───────┘
                │                                             │
                ▼                                             ▼
 ┌─────────────────────────────┐               ┌─────────────────────────────┐
 │   Client Visual Components  │               │   OpeningExperience & UI    │
 ├─────────────────────────────┤               ├─────────────────────────────┤
 │ • ParticleField (Three.js   │               │ • Opening Gateway Sequence  │
 │   3D WebGL background with  │               │ • Audio Greeting & Speech   │
 │   automatic Canvas fallback)│               │   Synthesis Fallback Engine │
 │ • ComputationalField (2D    │               │ • First-visit localStorage  │
 │   Canvas letter assembly)   │               │ • Floating Capsule Nav & Spy│
 └─────────────────────────────┘               └─────────────────────────────┘
```

### Visual Systems Distinction

1. **`ParticleField` (Three.js WebGL Engine):**
   - Implemented in `src/components/visual/ParticleField/`.
   - Runs a persistent 3D WebGL particle simulation behind the entire viewport.
   - Calculates physics for particle displacement based on cursor proximity, drag vectors, and scroll velocity.
   - Moves the 3D camera dynamically across distinct depth and angle presets as visitors traverse different sections (`#about`, `#events`, `#projects`, `#team`).
   - Includes a built-in Canvas 2D fallback renderer for devices without hardware WebGL support.

2. **`ComputationalField` (Canvas 2D Constellation Simulation):**
   - Implemented in `src/components/visual/ComputationalField/`.
   - A dedicated 2D physics simulation used during the cinematic opening gateway.
   - Points are pulled by spring dynamics toward typographic coordinate targets to form the "ACM" constellation, followed by a morph into "JIT ACM" and the chapter tagline.

3. **Voice Engine & Audio Greeting:**
   - Implemented in `src/lib/audio/voiceEngine.ts`.
   - Preloads and plays the official chapter audio greeting (`/audio/acm-welcome.wav`).
   - Automatically falls back to the browser's native `window.speechSynthesis` API if Web Audio playback is unsupported or blocked.
   - Respects user mute choices (`VOICE ON / VOICE OFF`) and retains preference across sessions.

---

## Core Features

- **Cinematic Opening Gateway:** A 9.0-second timed introductory sequence that assembles constellation points into the chapter brand, accompanied by spoken audio. Controlled via `localStorage` so returning visitors proceed straight to content (replayable anytime via `?opening=1`).
- **Floating Capsule Navbar:** Glassmorphic floating header with real-time IntersectionObserver scroll spy, glowing diamond indicator, desktop navigation, and a responsive mobile drawer.
- **Header Social Cluster:** Quick-access toolbar in the header providing instant links to official GitHub, LinkedIn, X, Instagram, and Discord channels.
- **Marquee Events Timeline:** Interactive exhibition of key chapter events, past and upcoming (*HackBlitz Season 3*, *Discover Docker*, *GitHub MasterClass*, *30DaysDevChallenge*, *ACM Installation*, and *Chapter Orientation*).
- **Projects Showcase & Case Studies:** Interactive portfolio grid linking to dynamic case study routes (`/projects/[slug]`) pre-rendered at build time with `generateStaticParams()`.
- **Executive Leadership Roster:** Comprehensive showcase of the 13 executive committee members featuring uniform 4:5 photoshoot portraits, member biographies, and direct links to GitHub and LinkedIn profiles.
- **Interactive Chapter Gallery:** Horizontally drifting photo wall with mixed aspect ratios (16:9 and 4:3), automatic horizontal drift, pause on hover, drag and touch interaction with inertial glide, and embedded photo metadata with ambient captions.
- **Luminous Webmaster Signature:** Custom canvas particle effect and glowing typography in the footer honoring platform development.
- **Accessibility & Motion Controls:** Full support for `prefers-reduced-motion` media queries across GSAP and Three.js, along with keyboard-accessible skip links (`#about`) and focus traps in dialogs.
- **Institutional Ecosystem Showcase (Prepared):** Dedicated SVG assets and marquee component for verified ACM SIGs (SIGARCH, SIGOPS, SIGPLAN, ACM Digital Library). *Note: The `SponsorsSection` component is staged in the repository and currently disabled in `page.tsx` pending final partner list confirmation.*
- **Production SEO & Web Standards:** Dynamic social preview generation via Next.js Edge OpenGraph (`opengraph-image.tsx`), automated XML sitemap (`sitemap.ts`), search engine directives (`robots.ts`), and Schema.org JSON-LD structured data.

---

## Technology Stack

The project relies strictly on modern, verified dependencies:

| Category | Technology | Version | Purpose |
| :--- | :--- | :--- | :--- |
| **Framework** | [Next.js](https://nextjs.org/) | `16.3.5` | App Router, static generation, Turbopack dev server |
| **UI Library** | [React](https://react.dev/) | `19.2.8` | Component model, React DOM 19, sync external store |
| **3D Graphics** | [Three.js](https://threejs.org/) | `^0.186.0` | 3D WebGL particle simulation & camera orchestration |
| **Animation Engine** | [GSAP](https://greensock.com/gsap/) | `^3.15.0` | ScrollTrigger timelines, typography reveals, marquee |
| **Animation React** | [@gsap/react](https://github.com/greensock/react) | `^2.1.2` | React lifecycle integration for GSAP animations |
| **Styling** | [Tailwind CSS](https://tailwindcss.com/) | `^4.0.0` | Utility-first CSS engine with `@tailwindcss/postcss` |
| **Language** | [TypeScript](https://www.typescriptlang.org/) | `^5.0.0` | Strict static typing across components, configs, and content |
| **Linting** | [ESLint](https://eslint.org/) | `^9.0.0` | Flat configuration with `eslint-config-next` |
| **Class Utilities** | `clsx` + `tailwind-merge` | `^2.1.1` / `^3.7.0` | Conflict-free conditional Tailwind class merging |
| **Hosting Platform** | [Vercel](https://vercel.com/) | Production | Edge deployment, static asset caching, redirects |

---

## Project Structure

```text
ACM_OFFICIAL_WEBSITE/
├── public/
│   ├── audio/
│   │   └── acm-welcome.wav          # Ambient opening greeting audio
│   ├── gallery/                     # High-resolution chapter event photography
│   │   ├── art-github-masterclass-poster.jpg
│   │   ├── evt-certificate-acm.jpg
│   │   ├── evt-github-masterclass-speaker.jpg
│   │   ├── evt-hackblitz.jpg
│   │   └── evt-shikhar.jpg
│   ├── images/
│   │   ├── jit-acm-logo.png         # Official chapter crest & shield
│   │   └── sponsors/                # Institutional ACM & SIG vector logos
│   │       ├── acm.svg
│   │       ├── acm-student-chapter.svg
│   │       ├── acm-sigarch.svg
│   │       ├── acm-sigops.svg
│   │       ├── acm-sigplan.svg
│   │       └── acm-dl.svg
│   ├── team/                        # Executive council portraits (4:5 crops)
│   └── logo.png                     # Chapter crest root alias
├── src/
│   ├── app/
│   │   ├── favicon.ico              # Browser favicon
│   │   ├── globals.css              # Theme tokens, font setups & neon variables
│   │   ├── icon.png                 # App icon
│   │   ├── layout.tsx               # Root layout, Geist fonts, JSON-LD, failsafe shell
│   │   ├── not-found.tsx            # Custom 404 error page
│   │   ├── opengraph-image.tsx      # Dynamic edge OpenGraph social card
│   │   ├── page.tsx                 # Single-page chapter experience
│   │   ├── robots.ts                # Search crawler instructions
│   │   ├── sitemap.ts               # Dynamic XML sitemap
│   │   └── projects/[slug]/
│   │       └── page.tsx             # Static dynamic case study route
│   ├── components/
│   │   ├── navigation/
│   │   │   └── Header.tsx           # Floating pill navbar, section spy & drawer
│   │   ├── opening/
│   │   │   └── OpeningExperience.tsx # Opening cinematic gateway
│   │   ├── sections/                # Main single-page sections
│   │   │   ├── AboutSection.tsx     # Mission pillars and chapter background
│   │   │   ├── EventsSection.tsx    # Chronological timeline of marquee events
│   │   │   ├── FooterSection.tsx    # Footer with luminous signature & links
│   │   │   ├── GallerySection.tsx   # Touch-enabled drifting photo wall
│   │   │   ├── OpeningSection.tsx   # Hero typography & exploration button
│   │   │   ├── ProjectsSection.tsx  # Featured student engineering projects
│   │   │   ├── SponsorsSection.tsx  # Institutional marquee (staged)
│   │   │   └── TeamSection.tsx      # 13-member executive leadership grid
│   │   ├── ui/                      # Atomic UI building blocks
│   │   │   ├── Container.tsx        # Standard viewport wrapper
│   │   │   ├── Diamond.tsx          # Geometric diamond accents
│   │   │   ├── Hairline.tsx         # Precision hairline dividers
│   │   │   ├── Magnetic.tsx         # Magnetic hover button wrapper
│   │   │   ├── Reveal.tsx           # Scroll reveal wrappers
│   │   │   ├── Section.tsx          # Section wrapper primitives
│   │   │   └── TwoToneHeading.tsx   # High-contrast animated headings
│   │   └── visual/
│   │       ├── ParticleField/       # Three.js 3D WebGL particle engine
│   │       └── ComputationalField/  # Canvas 2D attractor simulation
│   ├── config/
│   │   └── opening.ts               # Timeline, particle pools & audio config
│   ├── content/                     # Single source of truth data modules
│   │   ├── alumni.ts                # Alumni roster data
│   │   ├── data.ts                  # Central content re-exporter
│   │   ├── events.ts                # Event schedule & details
│   │   ├── gallery.ts               # Photographic gallery metadata
│   │   ├── placeholders.ts          # Section IDs & navigation descriptors
│   │   ├── projects.ts              # Chapter projects & deep-dive metadata
│   │   ├── site.ts                  # Chapter metadata, pillars & social URLs
│   │   ├── sponsors.ts              # Partner & SIG definitions
│   │   └── team.ts                  # Executive committee member profiles
│   ├── lib/
│   │   ├── audio/
│   │   │   └── voiceEngine.ts       # Web Audio / Speech Synthesis orchestrator
│   │   ├── motion/
│   │   │   ├── gsap.ts              # GSAP plugin registrations
│   │   │   ├── timeline.ts          # Transition timelines
│   │   │   ├── tokens.ts            # Motion tokens & reduced-motion hook
│   │   │   └── typography.ts        # Split-text character utilities
│   │   └── utils.ts                 # Class merging (clsx + twMerge)
│   └── types/
│       └── index.ts                 # Shared TypeScript models and interfaces
├── .env.example                     # Environment template
├── .gitignore                       # Git ignore specifications
├── AGENTS.md                        # Next.js workspace guard rules
├── CLAUDE.md                        # Project instructions reference
├── eslint.config.mjs                # ESLint 9 configuration
├── next.config.ts                   # Next.js build configuration & headers
├── package.json                     # Scripts and dependencies
├── postcss.config.mjs               # PostCSS plugin pipeline
├── tsconfig.json                    # TypeScript compiler options
└── vercel.json                      # Vercel deployment directives & rewrites
```

---

## Getting Started

### Prerequisites

Next.js 16 requires modern Node.js runtimes:
- **Node.js:** `^20.9.0` or higher (LTS recommended)
- **npm:** `^10.0.0` or higher (or compatible package manager)

### Installation & Local Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/pranjalisantani/ACM_OFFICIAL_WEBSITE.git
   cd ACM_OFFICIAL_WEBSITE
   ```

2. **Install project dependencies:**
   ```bash
   npm install
   ```

3. **Start the local development server:**
   ```bash
   npm run dev
   ```

4. **Open the application:**
   Navigate to [http://localhost:3000](http://localhost:3000) in your web browser.

---

## Available Commands

The following scripts are defined in [package.json](package.json):

| Command | Action |
| :--- | :--- |
| `npm run dev` | Starts the Next.js development server with Turbopack fast refresh |
| `npm run build` | Compiles and optimizes the full production build |
| `npm start` | Runs the compiled production build locally |
| `npm run lint` | Runs ESLint checks across the codebase |
| `npx tsc --noEmit` | Validates TypeScript types across the entire project with zero emit |

---

## Environment Variables

No sensitive API secrets or private tokens are required to run the website.

Optional environment configuration can be placed in `.env.local` (modeled after `.env.example`):

| Variable | Description | Default Fallback |
| :--- | :--- | :--- |
| `NEXT_PUBLIC_SITE_URL` | Canonical site URL used for OpenGraph generation, XML sitemaps, and robots directives | `https://jit-acm.vercel.app` (or Vercel system production URL) |

---

## Content Maintenance Guide

Website content is intentionally decoupled from user interface code. Chapter officers can manage content directly within `src/content/`:

### Managing the Executive Team
1. Place a portrait photo cropped to a **4:5 aspect ratio** into `public/team/` (e.g., `firstname-lastname.jpg`).
2. Update `src/content/team.ts`:
   ```typescript
   {
     id: "tm-14",
     name: "Member Name",
     role: "Executive Title",
     bio: "Member background, engineering focus, and chapter responsibilities.",
     photo: "/team/firstname-lastname.jpg",
     placeholder: false,
     links: [
       { label: "GITHUB", url: "https://github.com/username" },
       { label: "LINKEDIN", url: "https://linkedin.com/in/username" },
     ],
   }
   ```

### Publishing New Events
1. Open `src/content/events.ts`.
2. Add a new event entry to `EVENTS_DATA`:
   ```typescript
   {
     slug: "event-name-2026",
     title: "Event Title",
     dateISO: "2026-11-20T09:30:00Z",
     dateLabel: "NOV 20, 2026 · 15:00 IST",
     summary: "Summary of the workshop, contest, or keynote.",
     mode: "Interactive Workshop",
     location: "Campus Lab / Auditorium / Online",
     status: "open", // or "closing-soon" | "closed" | "past" | "tba"
     registerUrl: "https://registration-link.com",
     placeholder: false,
   }
   ```

### Adding Project Case Studies
1. Open `src/content/projects.ts`.
2. Append a new project object to `PROJECTS_DATA`:
   ```typescript
   {
     slug: "project-slug",
     title: "Project Name",
     summary: "Comprehensive overview of the platform, tooling, or library.",
     tags: ["Web", "TypeScript", "Next.js"],
     repoUrl: "https://github.com/jitacm/project-slug",
     url: "https://live-demo.com",
     placeholder: false,
   }
   ```
   *The dynamic case study route at `/projects/[slug]` automatically generates the static page.*

### Adding Event Gallery Photos
1. Add optimized JPEG or PNG images to `public/gallery/`.
2. Register the image in `src/content/gallery.ts`:
   ```typescript
   {
     src: "/gallery/evt-your-image.jpg",
     width: 993,
     height: 745,
     alt: "Descriptive alt text for accessibility",
     caption: "Contextual caption displayed alongside embedded photo metadata.",
     year: "2026",
     placeholder: false,
   }
   ```

### Quality Verification
Before submitting pull requests or pushing updates, verify that all static checks pass:
```bash
npx tsc --noEmit && npm run lint && npm run build
```

---

## Deployment Information

The website is continuously deployed to **Vercel** with automated preview builds for pull requests and instant production deploys on commits to `main`:

- **Production URL:** [https://jit-acm.vercel.app](https://jit-acm.vercel.app)
- **Vercel Project:** `jit-acm`
- **Asset Caching:** Configured via `vercel.json` and `next.config.ts` to apply aggressive HTTP caching (`public, max-age=86400, stale-while-revalidate=604800`) on static team portraits while allowing instantaneous cache bypass during local development.

---

## Official Chapter Channels

Stay connected with the JIT ACM Student Chapter across our official platforms:

| Platform | Channel | Link |
| :--- | :--- | :--- |
| **Discord** | Community Server | [Join Discord](https://discord.gg/j3b4gw2QK) |
| **LinkedIn** | Institutional Profile | [JIT ACM Student Chapter](https://www.linkedin.com/in/jit-acm-student-chapter/?isSelfProfile=false) |
| **GitHub** | Chapter Organization | [@jitacm](https://github.com/jitacm) |
| **Instagram** | Chapter Chronicles | [@acm_jit](https://www.instagram.com/acm_jit/) |
| **X (Twitter)**| Official Updates | [@jit_acm](https://x.com/jit_acm) |
| **Email** | Inquiries &amp; Collaborations | [acm@jitnagpur.edu.in](mailto:acm@jitnagpur.edu.in) |

---

## Attribution & Chapter Credits

- **Designed &amp; Developed by:** **Pranjali Santani** (Web Master) for the **JIT ACM Student Chapter**.
- **Institution:** [Jhulelal Institute of Technology](https://www.jitnagpur.edu.in/), Nagpur, India.
- **Parent Organization:** [Association for Computing Machinery (ACM)](https://www.acm.org/).
- **Executive Committee:** Managed by the 2025–2026 Chapter Executive Council.

```
ADVANCING COMPUTING. BUILDING PEOPLE.
© 2026 JIT ACM Student Chapter. All rights reserved.
```

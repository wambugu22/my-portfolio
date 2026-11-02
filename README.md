# Kevin Wambugu — Software Engineer & Digital Solutions Builder Portfolio

Official multi-page software engineering portfolio and case study platform for **Kevin Gachunji Wambugu**, a Software Engineer and Digital Solutions Builder based in Nairobi, Kenya.

Focused on Kevin's core engineering stack — **HTML5**, **CSS3**, **JavaScript (ES6+)**, **PHP 8**, and **Python** (backed by **MySQL**, **Git & GitHub**, **Vercel**, and **Hostinger**) — the portfolio features a glassmorphic visual system, a perspective-tilted IDE syntax background, interactive 3D card physics, and route-level code splitting for sub-second navigation across Desktop, Laptop, iPad, Tablet, iOS, and Android devices.

---

## 1. Brand Colour Palette & Design System

The interface is built around a custom CSS design token architecture (`src/index.css`):

| Token Role | Colour Name | Hex Code | Usage |
| :--- | :--- | :--- | :--- |
| **Primary Brand** | Deep Navy Blue | `#101D35` | Navigation bar, hero sections, terminal console, footer |
| **Secondary Brand** | Professional Teal | `#087E83` | Primary call-to-action buttons, skill meters, interactive links |
| **Main Background** | Off White | `#F5F7FA` | Frosted light section surfaces and readable content backdrops |
| **Accent** | Aqua | `#39BFC0` | Active navigation indicators, status rings, dark-surface highlights |
| **Surface** | Pure White | `#FFFFFF` | Translucent glassmorphic cards and elevated containers |

---

## 2. Multi-Page Routing Architecture

Unlike single-page scrolling templates, this portfolio implements dedicated routes with automatic scroll restoration and dynamic per-route SEO metadata (`src/components/ScrollToTop.tsx`):

| Page | Route URL | Component | Purpose |
| :--- | :--- | :--- | :--- |
| **Home** | `/` | `src/pages/Home.tsx` | Executive introduction, animated original portrait showcase, rotating specialty ticker, 4 featured project previews, compact stack strip, and contact CTA. |
| **About** | `/about` | `src/pages/About.tsx` | Full biography, Computer Science (Meru University) & Software Engineering (Moringa School) background, 4-pillar engineering philosophy, industry experience timeline, and leadership record. |
| **Projects** | `/projects` | `src/pages/Projects.tsx` | Dedicated software engineering portfolio with category filter tabs, real-time keyword/technology search, compact glass project cards, and a recruiter comparison matrix. |
| **Case Study** | `/projects/:slug` | `src/pages/ProjectDetail.tsx` | Deep-dive engineering case study per system showing Problem Statement, Engineered Solution, Architecture Highlights, Personal Contributions, Impact Metrics, and an interactive Browser-Framed Screenshot Walkthrough with full-screen Lightbox zoom. |
| **Skills** | `/skills` | `src/pages/Skills.tsx` | Interactive 5-category technical competency matrix with animated proficiency bars and an interactive CLI terminal (`kevin-cli`). |
| **Education** | `/education` | `src/pages/Education.tsx` | Academic qualifications and verified professional certifications (IBM Cybersecurity Analyst, UX Design & Research, Project Management, Ethical Hacking). |
| **Contact** | `/contact` | `src/pages/Contact.tsx` | Direct communication channels (one-click email copy, telephone, WhatsApp, GitHub, LinkedIn) and a client-side validated inquiry form. |

---

## 3. Included Software Engineering Case Studies

All project cards and case studies use real screenshots (`public/assets/projects/`) captured directly from the live and local systems:

1. **DevCars & Travel** (`/projects/devcars-and-travel`) — Car Hire, Safari Expeditions, Road Trips & Fleet Management CMS (`PHP 8`, `MySQL`, `JavaScript`).
2. **DevTech Ventures** (`/projects/devtech-ventures`) — Multi-Department Retail Storefront, Dynamic Search & Direct WhatsApp Commerce Platform (`PHP 8`, `MySQL`, `Admin CMS`).
3. **DevCare / DevTech Hospital** (`/projects/devtech-hospital`) — Level 5 Referral Hospital Portal, Consultant Clinic Schedules & Online Appointment Booking (`HTML5`, `CSS3`, `JavaScript`).
4. **iAssistGlobal** (`/projects/iassistglobal`) — Global Academic Consultation, Technical Research & Client Services Platform (Live on Cloudflare Workers).
5. **Jestwell Construction** (`/projects/jestwell-construction`) — Corporate Civil Engineering, Water Infrastructure & Construction Portal (Live on Cloudflare Workers).
6. **DevTech Systems ERP & Invoicing Suite** (`/projects/devtech-systems-erp`) — Full-Stack Enterprise Billing, Inventory, HR & Operations Management Platform (`HTML5`, `CSS3`, `JavaScript`, `PHP`, `MySQL` — Live on Vercel).
7. **School & Academic Management Systems** (`/projects/school-management-systems`) — Academic Opportunity Discovery, Document Analyzer & Student Administration (`HTML5`, `CSS3`, `JavaScript`, `PHP 8`, `Python`, `MySQL`).
8. **Offline-First Multi-Till Retail POS System** (`/projects/offline-first-retail-pos-system`) — Web & PWA Point-of-Sale with IndexedDB Queue & MySQL InnoDB Row-Locked Sync (`HTML5`, `CSS3`, `JavaScript`, `PHP 8`, `MySQL`).

---

## 4. Performance & Responsiveness Architecture

- **Route-Level Code Splitting**: Every secondary page (`About`, `Projects`, `ProjectDetail`, `Skills`, `Education`, `Contact`) is lazy-loaded via `React.lazy` and compiled into `2–5 kB` (gzipped) chunks.
- **Hover & Touch Prefetching**: Navigation links in `src/components/Navbar.tsx` prefetch their target route chunk on `onMouseEnter` and `onTouchStart` for near-zero latency transitions.
- **Critical Asset Preloading**: Hero portrait (`/assets/kevin-wambugu-profile.jpg`) and IDE code background (`/assets/code-bg.jpg`) are preloaded in `index.html`.
- **Cross-Device Compatibility**: Fluid CSS Grid and Flexbox layouts with explicit `-webkit-backdrop-filter` support and dedicated responsive breakpoints for Desktop (`1440px+`), Laptop (`1120px`), iPad/Tablet (`768px–992px`), and iOS/Android Phones (`320px–520px`).

---

## 5. Project Structure

```text
Portfolio 1/
├── public/
│   ├── .htaccess                         # Apache / Hostinger SPA routing rewrite rules
│   ├── favicon.svg                       # Custom KW brand monogram icon
│   └── assets/
│       ├── kevin-wambugu-profile.jpg     # Original profile photograph
│       ├── Kevin_Wambugu_CV_2026.pdf     # Downloadable CV PDF
│       ├── code-bg.jpg                   # Perspective IDE code screen background
│       └── projects/                     # Real screenshots captured from all 8 systems
├── src/
│   ├── components/
│   │   ├── DeveloperBackground.tsx       # Fixed IDE code background & perspective syntax layer
│   │   ├── Footer.tsx                    # Persistent multi-column footer
│   │   ├── InteractiveTerminal.tsx       # Interactive developer CLI console widget
│   │   ├── Navbar.tsx                    # Sticky glass navigation with route prefetching
│   │   ├── ProjectCard.tsx               # Compact 3D tilt-enabled project card
│   │   ├── Reveal.tsx                    # IntersectionObserver scroll-reveal wrapper
│   │   └── ScrollToTop.tsx               # Instant scroll reset & dynamic per-page SEO title/meta
│   ├── data/
│   │   └── portfolioData.ts              # Structured data for profile, 8 case studies, skills & education
│   ├── pages/
│   │   ├── Home.tsx                      # Homepage (/)
│   │   ├── About.tsx                     # Biography & experience (/about)
│   │   ├── Projects.tsx                  # Portfolio & filters (/projects)
│   │   ├── ProjectDetail.tsx             # Individual project case study (/projects/:slug)
│   │   ├── Skills.tsx                    # Technical skills & CLI (/skills)
│   │   ├── Education.tsx                 # Degrees & certifications (/education)
│   │   └── Contact.tsx                   # Contact channels & validated form (/contact)
│   ├── App.tsx                           # Router & lazy route definitions
│   ├── main.tsx                          # React 18 root entry
│   └── index.css                         # Complete glassmorphic & responsive design system
├── index.html                            # Root HTML with SEO meta & preloaded assets
├── vercel.json                           # Vercel SPA routing configuration
├── vite.config.ts                        # Vite bundler & manual vendor chunk splitting config
├── tsconfig.json                         # TypeScript strict configuration
└── package.json                          # Dependencies & build scripts
```

---

## 6. Local Development & Deployment

### Prerequisites
- **Node.js**: v18.0.0 or higher
- **npm**: v9.0.0 or higher

### Run Locally
```bash
# 1. Install dependencies
npm install

# 2. Start the development server at http://localhost:5173
npm run dev
```

### Build for Production
```bash
# Type-check with TypeScript and bundle into dist/
npm run build

# Preview the production build locally
npm run preview
```

### Deployment
- **Vercel**: Connect the GitHub repository or run `npx vercel --prod`. `vercel.json` is pre-configured to route all paths to `index.html`.
- **Hostinger / cPanel (Apache)**: Upload the contents of the compiled `dist/` directory into `public_html/`. The included `public/.htaccess` file automatically copies into `dist/.htaccess` during build to handle clean multi-page URLs.

---

## 7. Author & Contact

**Kevin Gachunji Wambugu**  
*Software Engineer & Digital Solutions Builder — Nairobi, Kenya*

- **Email**: [kevingachunji@gmail.com](mailto:kevingachunji@gmail.com)
- **Phone / WhatsApp**: [+254 718 249 497](https://wa.me/254718249497)
- **GitHub**: [https://github.com/wambugu22](https://github.com/wambugu22)
- **LinkedIn**: [https://www.linkedin.com/in/kevin-wambugu-9a7364210/](https://www.linkedin.com/in/kevin-wambugu-9a7364210/)

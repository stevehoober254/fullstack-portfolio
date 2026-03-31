# 🌐 Fullstack Engineer Portfolio — Stephen Gashoka

> Production-grade web applications with scalable APIs, CI/CD pipelines, and cloud-native hosting. Specialising in Africa-market products — offline-first PWAs, M-Pesa payment integrations, and multilingual interfaces.

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

---

## Projects

### 1. Offline-First POS System for Informal Traders
**Problem:** Small vendors in Kenya operate in areas with intermittent connectivity but need reliable sales records and inventory tracking.

**Architecture:**
- **Next.js** PWA frontend with **IndexedDB** (Dexie.js) for offline data persistence
- **NestJS + PostgreSQL** backend with conflict-resolution sync engine
- **Service Workers** for full offline capability (asset caching + API request queuing)
- **M-Pesa STK Push** integration for mobile payment recording
- **PDF/CSV** daily report export

**Key engineering decisions:**
- Implemented a CRDT-inspired sync strategy: offline mutations are timestamped and merged server-side, with last-write-wins on non-conflicting fields
- IndexedDB chosen over localStorage for structured query support on product catalogue
- Progressive enhancement: app is fully functional offline, enhanced when online

**Stack:** TypeScript · Next.js · NestJS · PostgreSQL · Dexie.js · Service Workers · M-Pesa API

---

### 2. Digital Farmer's Market — E-Commerce for Smallholder Farmers
**Problem:** Kenyan smallholder farmers lack direct-to-consumer online channels and rely on exploitative middlemen.

**Architecture:**
- **FastAPI + PostgreSQL** backend (async, production-ready)
- **Next.js 14 App Router** frontend with server components
- **M-Pesa STK Push** + **Stripe** payment integration
- **Mapbox GL JS** for farm location discovery
- **Africa's Talking SMS API** for order confirmation and delivery alerts
- Deployed on **Railway** (backend) + **Vercel** (frontend)

**Key engineering decisions:**
- Used PostGIS extension for geospatial farm queries ("farms within 50km")
- SMS notifications via Africa's Talking preferred over email (higher rural open rates)
- Separate buyer and farmer dashboards with role-based access

**Stack:** Python · FastAPI · Next.js · PostgreSQL · PostGIS · M-Pesa · Mapbox · Africa's Talking

---

### 3. AI-Powered Resume Matcher & Job Fit Scorer
**Problem:** Hiring managers spend hours manually screening CVs; candidates don't know how well their CV matches a job description.

**Architecture:**
- **Python NLP backend**: sentence-transformers for semantic similarity, spaCy for skill extraction
- **GPT embeddings** for job description → skill graph mapping
- **React + Tailwind CSS** frontend: upload CV + paste JD → see fit score breakdown by skill category
- **FastAPI** serving the ML inference endpoints
- **PDF parsing** via PyMuPDF for structured CV extraction

**Stack:** Python · FastAPI · spaCy · sentence-transformers · OpenAI API · React · TailwindCSS · PyMuPDF

---

## Architecture patterns used
- Clean architecture (domain / application / infrastructure layers)
- Repository pattern for data access
- Event-driven with message queues (Redis Bull for background jobs)
- Containerised with Docker Compose for local dev parity

---

## Skills demonstrated
| Area | Technologies |
|---|---|
| Frontend | React, Next.js, TypeScript, TailwindCSS, PWA/Service Workers |
| Backend | Node.js, NestJS, FastAPI, REST, GraphQL |
| Database | PostgreSQL, PostGIS, Redis, Prisma ORM |
| Payments | M-Pesa STK Push, Stripe, KCB API |
| DevOps | Docker, GitHub Actions CI/CD, Vercel, Railway, AWS |
| Testing | Jest, Playwright (E2E), pytest |

---

> 📌 Also see: [KCB M-Pesa WooCommerce Plugin](https://github.com/stevehoober254/kcb-mpesa-express-wordpress-plugin) — a production WordPress payment plugin with real install base.

📧 stephengachoka57@gmail.com | 🌐 [stephengachoka.co.ke](https://stephengachoka.co.ke) | 📍 Nairobi, Kenya

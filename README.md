# Reggie Johnson
### Principal Engineer · Engineering Manager · Systems Automation

**(408) 813-0924 · regkeys75@gmail.com · Temecula, CA**

> 20+ years of full-stack engineering across enterprise, SaaS, fintech, and e-commerce — including roles at eBay, Boardvantage (acquired by Nasdaq), and GRIN. Currently serving as Principal Engineer at HBX LLC, building production Python automation systems and a full transport CRM, leveraging agentic AI to deliver complete solutions faster than traditional development cycles.

---

## Recent Projects · HBX LLC

### ⚡ Automated Driver Time Correction & Clock-Out System
> Flask · Samsara webhooks · ConnectTeams API · Bidirectional geofence automation · cron reporting · GitHub (private)

A fully automated, bidirectional time management system that handles both ends of every driver shift without any manual intervention.

**How it works:**

**Geofence EXIT → Clock-in time correction**
When a driver departs the HBX LLC base past a prescribed time threshold, the system automatically adjusts their ConnectTeams clock-in time to reflect the actual departure — correcting for late starts in real time, no supervisor action required.

**Geofence ENTRY → Automatic clock-out**
When a driver's vehicle re-enters the HBX LLC geofence at the end of their shift, the system automatically clocks them out of ConnectTeams — eliminating missed or forgotten clock-outs entirely.

Together these two triggers form a self-correcting, end-to-end automated shift time system.

**What I built:**
- Flask webhook listener processing real-time Samsara geofence events (EXIT and ENTRY)
- Business logic layer applying prescribed time thresholds to determine when clock-in adjustments are warranted
- **PostgreSQL database** — all driver activity data (clock-in/out times, corrections, route events) is written to PostgreSQL on every event, creating a permanent queryable record; enables legacy and historical reports to be regenerated on demand at any time
- `DRIVER_MAP` dictionary linking Samsara driver IDs → ConnectTeams driver + clock IDs for 47 drivers
- Automated reporting pipeline — Python scripts query the PostgreSQL database to generate daily and weekly driver activity reports (clock-in/out times, hours worked, route completion), scheduled via Linux cron jobs
- Multi-file architecture: `clockout_service.py`, `connectteams.py`, `samsara_webhook.py`, report scripts, systemd service
- Deployed on Linux with Gunicorn + Nginx + systemd + SSL/Certbot
- Version-controlled in private GitHub repository

**Stack:** `Python` `Flask` `PostgreSQL` `Samsara API` `ConnectTeams API` `Webhooks` `cron` `Linux` `GitHub`  
**Impact:** Eliminated manual clock-out, late clock-in corrections, and manual report generation for all 47 driver shifts — full shift history retained in PostgreSQL for on-demand historical reporting

---

### 🚐 HBX CRM — Transport Management System
> React (JSX) · Django · PostgreSQL · 11 modules · Agentic AI scaffolding

Full transport operations CRM covering client referral through active route assignment.

**What I built:**
- Refactored a legacy 5,800-line React SPA: Clients, Drivers, Vehicles, Programs, Dispatch, Absence Log, Compliance, Import, Users, Activity
- Directed agentic AI to analyze the full JSX codebase and scaffold a complete Django + PostgreSQL backend — 11 apps, 103 Python files, models, admin, REST API layer, role-based auth, and middleware — in a single session
- Data model covers full client lifecycle, driver certifications, fleet compliance, and role-based user access
- Planned migration to Django REST Framework + React SPA with JWT auth

**Stack:** `Python` `Django` `React` `PostgreSQL` `Django REST Framework` `Agentic AI`

---

### 📊 Samsara Route Fetcher & Attendance Reporter
> pandas · Samsara API · Excel automation

- Paginated Samsara `/fleet/routes` client with timezone handling; cross-references TOS helper file per driver-vehicle assignment
- Multi-sheet Excel output: Route Detail, UCI Detail, S1 Route Final
- Iterated across 3 versions (v1 → v2 → v3)

**Stack:** `Python` `pandas` `openpyxl` `Samsara API`

---

### 💰 Operations Data Pipeline Suite
> Billing reconciliation · Absence log parsing · Monthly summary cleaning

- **Billing generator** — UCI # matching across files, 1/0 date columns for all 31 billing days
- **Absence log parser** — ConnectTeams chat export → 156-row structured Excel log with date logic
- **Monthly summary cleaner** — zero blanking, row filtering, UCI # highlight matching, deduplicated reference sheet

**Stack:** `Python` `pandas` `openpyxl`

---

## Technical Skills

| Category | Tools |
|----------|-------|
| **Languages** | Python, PHP, JavaScript / JSX, TypeScript, Java, Bash, HTML5/CSS3 |
| **Frameworks** | Django, DRF, Flask, React, Angular, Laravel, CodeIgniter, Vue, Bootstrap |
| **Data / Databases** | pandas, openpyxl, PostgreSQL, MySQL, SQL, NoSQL |
| **APIs & Integration** | Samsara, ConnectTeams, PayPal, Facebook, Twitter, WebEx, Salesforce, REST/JSON |
| **Automation** | cron scheduling, systemd, webhooks, event-driven geofence pipelines |
| **Cloud / DevOps** | AWS EC2, DigitalOcean, Docker, Gunicorn, Nginx, Apache, LAMP, Git/GitLab, SSL |
| **AI Tooling** | Claude Code (PyCharm), Claude.ai — agentic architecture & code generation |
| **Engineering Mgmt** | Team leadership (up to 18), Agile/Scrum, JIRA, hiring, mentoring, CTO reporting |

---

## How I Work with Agentic AI

With 20+ years of engineering experience, I use agentic AI the way a principal engineer should — as a force multiplier, not a replacement for judgment:

- **Architect first, generate second** — I define system structure, data models, and constraints before any code is written
- **Direct AI against real codebases** — fed a 5,800-line JSX app to Claude, directed it to produce a structured 11-app Django backend with proper model relationships, auth, and deployment config
- **Own all output** — engineering depth means I review, understand, and catch what AI gets wrong
- **Result** — full-stack systems that would take a team weeks are scoped, built, and deployed in days

---

## Professional Experience

**Principal Engineer · HBX LLC** *(2026 – Present · Temecula, CA)*  
Design and deploy bidirectional geofence automation systems connecting Samsara and ConnectTeams — handling clock-in time corrections on route departure and automatic clock-outs on driver return. Architect and develop a full React + Django + PostgreSQL CRM. Build automated reporting pipelines with cron-scheduled execution on Linux servers.

**Software Engineering Manager / Engineer · Nogient** *(Jan 2023 – Present)*  
Architectural design, coding standards, team building across client companies. Stack: PHP/Laravel, Java, MySQL, Vue, JavaScript, TypeScript.

**Software Engineering Manager · GRIN** *(March 2022 – December 2022)*  
Led engineering team building SaaS and mobile applications. Accountable for estimation, budget, and delivery.

**Backend Software Engineer · Mindgruve** *(January 2020 – July 2020)*  
Complex banking solution for multi-account fund integrity. PHP/REST API development.

**Software Engineering Manager · California Community Technical Center** *(2017 – 2019)*  
Managed 18-person team delivering enterprise software to CA Community Colleges. Reported to CTO.

**Full Stack Engineer · eBay** *(2016 – 2017)*  
Enterprise-scale internal web apps; C3 Cloud configuration and deployment; passed internal security audits.

**Senior Lead Web Developer · Boardvantage (acquired by Nasdaq)** *(2012 – 2015)*  
Technical leadership: architecture, framework selection, security, Angular 1 → Angular 2 migration. Recruited staff, mentored developers.

**Earlier:** Nogient Technologies — Lead Engineer (2006–2012) · Prelude Productions — Senior Web Developer (2002–2005) · Silicon Graphics — Web Production Engineer (2001) · 3COM — Webmaster (2000–2001) · Internet Shopping Network — Lead Web Developer (2000)

---

## Education
- Foothill College, California — C/C++ Programming
- Wintec Software Training Institute, California
- Electronic Technical Institute, Ohio

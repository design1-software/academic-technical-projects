# Built With Purpose — Academic & Technical Projects

Live site: [builtwithpurpose.netlify.app](https://builtwithpurpose.netlify.app)
Author: **Julius L. Moore** · WGU Software Engineering · Nurse → Engineer

---

## What this repo is

This is the source for my public portfolio — the landing page where I consolidate the three disciplines I'm deliberately building skills in: **software engineering**, **networking & infrastructure**, and **data engineering**.

Rather than a resume bullet list, the site is structured around *artifacts*:

- a live, enterprise-style **home lab network** I built and run (Cisco C1111-4PWB, 7 VLANs, 4 ACLs, dual managed switch trunks, Pi-hole, UniFi)
- **troubleshooting labs** — real incidents on real hardware, documented step-by-step and mapped to CCNA exam topics
- links out to three production repos covering networking, IoT/data, and a multi-service content automation system

The intent is simple: show, don't tell. Every stat on the page points to something that actually runs.

---

## Repository contents

```
.
├── index.html     # Portfolio landing page (hero, about, network, labs, projects)
├── lab-001.html   # Apple TV connectivity failure after ISP bridge mode cutover
└── lab-002.html   # Tailscale DNS hijack & TCP socket corruption
```

No build step. No framework. Plain HTML/CSS with vanilla JS for the dark/light theme toggle. Deployed on Netlify.

---

## For recruiters — skills demonstrated in this repo

This site is a small piece of a larger portfolio, but even on its own it surfaces a specific set of skills:

### Front-end fundamentals (no-framework mastery)
- Hand-written semantic HTML5 and modern CSS (custom properties, `clamp()`, grid/flex, keyframe animations, `backdrop-filter`)
- Theming system with CSS variables and a persisted light/dark toggle using `localStorage`
- Responsive design with progressive breakpoints (768px / 480px)
- Accessible patterns: `aria-label` on interactive controls, semantic nav/section structure, readable contrast in both themes
- Deliberate choice to avoid a framework where one isn't needed — understanding the platform first

### Technical writing & communication
- The two lab pages are long-form technical writeups: problem statement → hypothesis → evidence → resolution, with CLI output, OSI-layer mapping, and CCNA exam topic tags
- Written for two audiences simultaneously: a hiring manager skimming, and an engineer reading to verify the work
- The index page leads with concrete numbers (78K+ LOC, 7 VLANs, 5,600+ sensor readings) rather than adjectives

### Networking & infrastructure (documented, not claimed)
- Cisco IOS configuration on a C1111-4PWB acting as sole router with a public IP (ISP gateway in bridge mode)
- VLAN design across server / trusted / IoT / automation / household / guest / management segments
- ACL policy enforcement between segments, trunking to managed PoE+ switches, UniFi SSID-to-VLAN mapping
- Troubleshooting depth: NAT/PAT, TCP MSS, DNS resolution paths, DHCP vs static binding, VPN overlays

### Cross-discipline project links
- `git-init-home-lab` — the networking project this site documents
- `closet-monitor` — ESP32 + BME280 → MQTT → Python → SQLite → Streamlit, with rolling z-score anomaly detection (IoT + data engineering)
- `fb-content-system` — multi-repo content automation: MCP server, Remotion video rendering, multi-API orchestration, Railway deployment

### Engineering habits
- Git, GitHub, CI-less static deploy via Netlify
- Every claim on the page is verifiable — live URLs, public repos, documented incidents
- Learning in public: breaking things on purpose, writing up the resolution, and publishing the artifact

---

## Why this project exists

I'm a nurse pursuing a Software Engineering degree at Western Governors University. The degree is the floor, not the ceiling. The gap that gets you hired isn't "I studied networking" vs "I built a network" — it's the work you can point to. This repo is part of how I point to it.

If you're a recruiter or engineering manager and want the longer conversation, the footer of the site has my LinkedIn and GitHub.

---

## Running locally

```bash
git clone https://github.com/design1-software/academic-technical-projects.git
cd academic-technical-projects
open index.html   # or: python3 -m http.server 8000
```

---

© 2026 Julius L. Moore — Built with purpose.

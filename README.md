# Ezzulddin.sys // Minimalist Terminal Portfolio

> High-performance, zero-framework personal terminal portfolio for Ezzulddin Al-Sammarraie. Deployed globally on the edge via Cloudflare Pages.

[![Lighthouse Performance](https://img.shields.io/badge/Lighthouse-100%2F100-00FF66?style=flat-square&logo=googlechrome&logoColor=black)](https://ezzulddin.com)
[![Cloudflare Pages](https://img.shields.io/badge/Cloudflare_Pages-Active-F38020?style=flat-square&logo=cloudflare&logoColor=white)](https://ezzulddin.com)
[![HTML5](https://img.shields.io/badge/Stack-HTML5%20%7C%20CSS3-E34F26?style=flat-square&logo=html5&logoColor=white)](https://ezzulddin.com)

🌐 **Live Production:** [ezzulddin.com](https://ezzulddin.com)

---

## ⚡ Engineering & Architecture Highlights

- **Zero-Framework Architecture:** Handcrafted semantic HTML5 and vanilla CSS3 with zero heavy client-side JavaScript dependencies.
- **100/100 Google Lighthouse:** Verified top-tier scores across Performance, Accessibility, Best Practices, and SEO.
- **QD-OLED Terminal Aesthetic:** Custom high-contrast dark theme with glowing neon status indicators and mobile viewport scaling.
- **Accessible by Default:** Keyboard skip navigation, visible focus states, and reduced-motion support respect visitor preferences without adding JavaScript.
- **Navigable Semantics:** Screen-reader users can jump directly between profile, labs, contributions, and contact sections while the terminal UI remains visually minimal.
- **Social-Ready Sharing:** Custom Open Graph and X card metadata presents a cohesive terminal-themed preview when the portfolio is shared.
- **Search Discovery:** An XML sitemap and crawler policy make the canonical portfolio URL easy for search engines to discover.
- **Structured Profile Data:** Schema.org `Person` metadata connects professional identity, specialties, and verified public profiles for search engines.
- **Security Reporting:** A standard `/.well-known/security.txt` endpoint directs responsible disclosure reports to the published security policy.
- **Terminal Identity:** A custom, dependency-free SVG favicon carries the terminal aesthetic into browser tabs.
- **Edge CI/CD Pipeline:** Automated continuous deployment on Cloudflare Pages triggered on every `git push` to `main`.
- **Agentic AI Ready:** Standard-compliant `llms.txt` and `robots.txt` implementation for structured machine-readable indexing.

---

## 📂 Repository Layout

```text
├── index.html       # Primary terminal UI & verified contribution feed
├── 404.html         # Custom terminal fallback page for broken routes
├── .well-known/
│   └── security.txt # Standard security-contact endpoint
├── assets/           # Social-sharing image assets
├── favicon.svg       # Terminal-inspired browser tab icon
├── llms.txt         # Structured engineering summary for AI web agents
├── robots.txt       # Search engine crawler policies
├── sitemap.xml      # Canonical URL discovery for search engines
├── SECURITY.md      # Vulnerability disclosure policy
└── README.md        # Repository documentation & architecture
```

## Local Preview

No build step or package installation is needed. From the repository root, use Python 3 to serve the static files on your computer:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

On Windows, use `py` instead of `python` if that is how Python is installed. Open [http://127.0.0.1:8000/](http://127.0.0.1:8000/) and press `Ctrl+C` in the terminal when finished.

Use this HTTP preview instead of opening `index.html` directly: root-relative paths such as `/favicon.svg` and the 404 page's home link need a server root to resolve correctly.

Before publishing a change:

- Check the homepage at desktop and narrow mobile widths.
- Use `Tab` to check the skip link and link focus indicators.
- Open `/404.html` to preview the error page and test its home link. Python's server uses its own response for missing URLs; the custom error routing must be checked on Cloudflare Pages.
- Run `git diff --check` to catch whitespace errors, then review the diff.

Pushing to `main` triggers the existing Cloudflare Pages deployment. After deployment, check the live site to confirm the update is served.

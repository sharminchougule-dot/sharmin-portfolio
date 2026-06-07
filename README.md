# Sharmin N. Chougule — Portfolio Website

Personal portfolio for Sharmin N. Chougule, Research Associate at the Institut für das Recht der Digitalisierung (IRDi), University of Marburg, and Doctor Europaeus in Civil Law & Constitutional Legality.

## Live Site

[https://sharminchougule-dot.github.io/sharmin-portfolio/](https://sharminchougule-dot.github.io/sharmin-portfolio/)

---

## Design

**Editorial Scholar** — ink navy · warm ivory · oxblood · brushed gold.

Typography: [Fraunces](https://fonts.google.com/specimen/Fraunces) (display serif) · [Inter](https://fonts.google.com/specimen/Inter) (body) · [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) (labels & tags), loaded via Google Fonts.

---

## Sections

| Section | Description |
|---|---|
| **Hero** | Editorial split-layout with portrait frame, institution wordmark strip (Marburg · Camerino · UNIDROIT · KU Leuven · INATBA · ICLE), and three CTAs |
| **Stat Strip** | Five key credentials at a glance: years in law, publications, research countries, Doctor Europaeus, EU Blue Card |
| **About** | Two-column layout with pull quote, research focus pillars, and info cards |
| **Expertise** | Three-column areas of expertise: Legal, Technology Law, and Additional Skills |
| **Publications** | Featured publication (DG JUST / European Commission) + five-card grid |
| **Affiliations** | Dedicated section for INATBA AAB, UNIDROIT Task Force, ICLE Fellowship, ICSI |
| **Experience** | Tabbed timeline — Research & Academia · Legal Practice · Education |
| **Contact** | Three institutional emails, social links, and EmailJS-powered contact form |

---

## Technologies

- HTML5 / CSS3 (CSS custom properties)
- Vanilla JavaScript
- [EmailJS](https://www.emailjs.com/) — contact form delivery
- Google Fonts — Fraunces, Inter, JetBrains Mono

---

## Project Structure

```
sharmin-portfolio/
├── index.html              # Main page
├── static/
│   ├── css/
│   │   └── style.css       # Full design system stylesheet
│   └── images/             # Profile photo and publication images
├── GITHUB_PAGES_SETUP.md   # GitHub Pages deployment guide
├── IMAGE_SOURCES_GUIDE.md  # Guide for publication cover images
└── README.md               # This file
```

---

## Local Setup

```bash
git clone https://github.com/sharminchougule-dot/sharmin-portfolio.git
cd sharmin-portfolio
# Open index.html in a browser — no build step required
```

---

## Contact Form (EmailJS)

The form uses EmailJS. Credentials are already configured in `index.html`. To update them:

1. Sign up at [emailjs.com](https://www.emailjs.com/)
2. Create an email service and template
3. In `index.html`, update:
   - **Public Key** — `emailjs.init("…")` near line 12
   - **Service ID** and **Template ID** — `emailjs.send(…)` in the form submit handler

See `GITHUB_PAGES_SETUP.md` for full deployment instructions.

---

## Links

- **LinkedIn**: [sharmin-chougule-7723a5109](https://www.linkedin.com/in/sharmin-chougule-7723a5109/)
- **ORCID**: [0000-0002-1732-8235](https://orcid.org/0000-0002-1732-8235)
- **White Bison**: [Author profile](https://www.whitebison.io/author/sharmin-n-chougule)

---

© 2025 Sharmin N. Chougule. All rights reserved.

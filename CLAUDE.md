# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Converting the **Home Alarms v2.9** HTML template into the **SpiceWorx.com** website — a web and mobile development company site. This is a static HTML/CSS/JS project with no build system, bundler, or package manager.

## How to Preview

Open any HTML file directly in a browser, or use a local server:

```bash
# From the template directory
cd home_alarms_v.2.9_template/html
python3 -m http.server 8000
# Then visit http://localhost:8000
```

PHP form handlers (`assets/contact.php`, `quotation-normal_2.php`, `quotation-wizard-send.php`) require a PHP-capable server (e.g., MAMP, XAMPP, or `php -S localhost:8000`).

## Architecture

### Directory Layout

All working files live under `home_alarms_v.2.9_template/html/`. There is no separate `src/` or `dist/` — edits are made directly to these files.

```
home_alarms_v.2.9_template/html/
├── index.html              # Homepage (primary landing page)
├── about.html              # About page
├── service_layout_1.html   # Web Application Development
├── services_layout_2.html  # Mobile Application Development (note: "services" plural)
├── services_layout_3.html  # Web Hosting & Maintenance (note: "services" plural)
├── contacts.html           # Contact page
├── quotation.html          # Project Inquiry Form
├── shop.html               # Repurposed as Hosting Packages
├── blog.html / blog_post.html  # Blog system
├── css/
│   ├── bootstrap.min.css   # Bootstrap 5 (do not edit)
│   ├── style.css           # Main theme styles (~2350 lines) — primary branding file
│   ├── menu.css            # Navigation/menu styles
│   ├── responsive.css      # Media queries
│   ├── custom.css          # Custom overrides (edit this for new styles)
│   ├── carousel_home.css   # Homepage carousel
│   ├── shop.css / blog.css # Section-specific styles
│   ├── skins/              # iCheck checkbox/radio skins
│   ├── elegant_font/       # Elegant Icons font
│   ├── fontello/           # Fontello icon font
│   └── bs-icon-font/       # Bootstrap Icons font
├── js/
│   ├── jquery-3.7.1.min.js # jQuery (do not edit)
│   ├── bootstrap.bundle.min.js  # Bootstrap JS (do not edit)
│   ├── functions.js        # Main site JS (preloader, sticky nav, mobile menu, carousels)
│   ├── common_scripts_min.js    # Bundled common scripts
│   ├── slider.js / slider_func.js  # Hero slider config
│   └── parallax.js, owl.carousel.js, etc.  # Feature-specific scripts
├── img/                    # All images (~60 files), logo.png, favicon.ico
├── assets/                 # PHP form handlers + validation JS
├── layerslider/            # LayerSlider premium plugin (CSS/JS/skins)
└── video/                  # Background video assets
```

### CSS Cascade Order

Styles load in this order (defined in each HTML `<head>`):
1. `bootstrap.min.css` — framework base
2. `style.css` — theme styles and branding colors
3. `menu.css` — navigation
4. `responsive.css` — breakpoints
5. Icon fonts (elegant_font, fontello, bootstrap-icons)
6. Page-specific CSS (carousel_home, shop, blog, etc.)
7. **`custom.css`** — custom overrides (last = highest priority)

**Always add new styles to `custom.css`** to keep template updates safe and maintain override priority.

### Naming Inconsistency

Watch out: `service_layout_1.html` (singular) vs `services_layout_2.html` and `services_layout_3.html` (plural). Internal links must match the exact filenames.

## Branding (from SpiceWorx Brand Guide)

### Brand Personality & Tone

- **Professional but approachable** — not stiff, not corporate-robot
- **Clear and concise** — no jargon, direct language, easy to understand
- **Trusted guide** — a bridge between cultures and between tech & people
- Tone: Warm, precise, confident

### Color Palette (Chili Pepper Inspired)

| Role | Hex | Usage |
|------|-----|-------|
| Primary (Deep Olive Green) | `#3E5E3A` | Brand anchor — headers, buttons, nav bar |
| Background (Warm Gray) | `#F2F2F0` | Softer than white, use as page backdrop |
| Accent CTA (Chili Red) | `#C23B22` | Hover links, icons, micro-accents (NOT body text) |
| Body Text (Charcoal) | `#333333` | Body text — professional and legible |
| Hover Highlight (Sage Green) | `#7A8E72` | Button hover, subtle highlights |
| Divider (Stone Gray) | `#DAD8D3` | Section breaks, subtle contrasts |
| Text on Dark (Ivory) | `#FAFAF5` | Text or icons against green blocks |
| Luxe Accent (Gold) | `#C9A552` | Use VERY sparingly — one section max (e.g., "Why Choose Us" or Awards/Partners) |

CTA button hover: `#A12F1C` (darker chili). Secondary button hover: `#5A8E49` (muted green). Use neutrals (white, grey, black) for balance.

### Typography

- **Headings:** Open Sans Bold (700)
- **Body Text:** Open Sans Regular (400)
- **Quotes:** Open Sans Italic
- Template originally uses Poppins — replace Google Fonts link in all HTML `<head>` sections
- Clean sans-serif for digital use. Avoid decorative fonts — clarity first.

### Logo

- Wordmark: "SpiceWorx" in green text with red "i" (symbolizes chili pepper / bold differentiator)
- `img/spiceworx-logo.png` (428×88 PNG). The original template logo is `img/logo.png` (190×44).
- Use consistently — do not stretch, skew, or recolor.

### Graphic Style

- Simple, direct visuals
- Iconography per service: handshake (cultural workshops), chat bubble (interpretation), browser window (web dev)
- Imagery: professional, real-world (people working, tech in action, cross-cultural moments)

### Services (per Brand Guide)

1. **Interpreter Services** — Japanese–English–Filipino for corporate, industrial, and government contexts
2. **Web Development & Hosting** — smart, secure, user-friendly websites for a global market
3. **Workshops & Training** — Cross-Cultural Business Training, Leadership & Team Workshops

*Note: The website build focuses on 4 primary service pages: Web App Development, Mobile App Development, Web Hosting & Maintenance, and UI/UX Design.*

### Target Audiences

1. **Japanese Corporates/SMEs** — need cultural trust, smooth communication, market understanding
2. **Philippine Organizations** — need credibility with Japanese partners
3. **Global Businesses (SMEs/boutique)** — need cost-efficient, professional, secure web solutions

### Messaging & Positioning

- **Primary tagline:** "Bridging Cultures. Building Solutions."
- **Alternates:** "From Language to Digital — Clarity that Works." / "Your Partner for Cross-Cultural and Digital Growth."
- **Key messages:**
  - "Spiceworx helps Japanese and Philippine businesses connect with clarity and confidence."
  - "Our web solutions serve clients globally — modern, secure, and efficient."
- **Elevator pitch:** "Like a chili pepper — small but powerful — Spiceworx makes a big impact in the spaces where clarity matters most. We provide interpreter services that bridge Japanese, English, and Filipino for corporate and government settings, build smart and secure websites for a global market, and deliver workshops that strengthen cultural understanding, leadership, and team performance."

### Core Values

| Value | What it Looks Like |
|-------|-------------------|
| Clarity | Simplifying complexity in both language and tech |
| Trust | Long-term relationships built on reliability |
| Cultural Fluency | Respect for context and nuance |
| Innovation | Digital-first, always evolving |
| Efficiency | No fluff — solutions that work |

## Page Mapping (Template → SpiceWorx)

| Template Page | SpiceWorx Purpose |
|---|---|
| `index.html` | Homepage |
| `service_layout_1.html` | Web App Development |
| `services_layout_2.html` | Mobile App Development |
| `services_layout_3.html` | Web Hosting & Maintenance |
| `about.html` | About (pivot story) |
| `contacts.html` | Contact |
| `quotation.html` | Project Inquiry Form |
| `shop.html` | Hosting Packages |
| `blog.html` | Blog & Resources |

Pages to ignore/remove: `index_2/3/4.html` (alt homepages), `cart.html`, `checkout.html`, `accessories.html`, `icon_pack_*.html`, `shortcodes.html`, `tips.html`, `contacts_2.html`, `quotation_wizard.html`.

## Existing SpiceWorx Site (Content Reference)

The old spiceworx.com site (Japan-Philippine business consultancy) is stored locally at:

```
/Users/ruelabion/Sites/CodeCommit/spiceworx.com/html/
```

Use this as the source for reusable content (company history, about text, contact details, pivot story) — **do not fetch spiceworx.com online**. Key pages:

| File | Content |
|------|---------|
| `index.html` | Old homepage — company overview, carousel, service highlights |
| `aboutus.html` / `about.html` | Company story, background, mission |
| `services.html` | Old service offerings (consulting, cross-cultural training) |
| `contact-us.html` | Contact form, address, map |
| `members.html` | Team member profiles |
| `projects.html` | Past project showcase |
| `blog.html` | Blog posts (Japanese business manners, etc.) |
| `privacy-policy.html` | Privacy policy text |

The old site's services (cross-cultural training, consulting, interpreter services, leadership development) are being replaced entirely with the new offerings: Web App Development, Mobile App Development, Web Hosting & Maintenance, and UI/UX Design. However, the company history and founding story can be adapted for the About page's pivot narrative.

## Key Modification Patterns

When converting template content to SpiceWorx:

1. **Every HTML file** has an identical header/footer structure — changes to nav links, logo, phone, or footer must be replicated across all kept pages
2. Colors in `style.css` use hex values throughout (no CSS variables) — search-and-replace is the primary rebranding method
3. The template's original blue accent is `#06C` (links) and various blues in `style.css` — these map to the SpiceWorx palette
4. Form `action` attributes point to PHP files in `assets/` or root — update email addresses in those PHP files
5. Google Fonts link in `<head>` needs changing from Poppins to Open Sans across all HTML files

## Company Info (for footers, contact pages, meta tags)

```
SpiceWorx Consultancy, Inc.
Unit 5 Ecoville, Sta. Cruz, Makati 1205
Phone: +632-8899-6784
Email: info@spiceworx.com
Tagline: "Bridging Cultures. Building Solutions."
```

*Note: Brand guide address (Unit 5 Ecoville, Sta. Cruz, Makati 1205) differs from earlier project brief (U7 Ecoville, Metropolitan Ave.). Use the brand guide version as authoritative.*

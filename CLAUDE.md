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
├── service_web-app.html    # Web Application Development
├── service_mobile-app.html # Mobile Application Development
├── service_hosting.html    # Web Hosting & Maintenance
├── service_uiux-design.html # UI/UX Design
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
- ~~Template originally uses Poppins~~ — DONE: Google Fonts link updated to Open Sans in all 26 HTML/PHP files and CSS
- Clean sans-serif for digital use. Avoid decorative fonts — clarity first.

### Logo

- Wordmark: "SpiceWorx" in green text with red "i" (symbolizes chili pepper / bold differentiator)
- Source: `/Users/ruelabion/Sites/CodeCommit/spiceworx.com/html/img/logo.png` (428×88 PNG)
- DONE: Copied to `img/logo.png` and `img/logo-footer.png`, displayed at 214×44 in HTML
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
| `service_web-app.html` | Web App Development |
| `service_mobile-app.html` | Mobile App Development |
| `service_hosting.html` | Web Hosting & Maintenance |
| `service_uiux-design.html` | UI/UX Design |
| `about.html` | About (pivot story) |
| `contacts.html` | Contact |
| `quotation.html` | Project Inquiry Form |
| `shop.html` | Hosting Packages |
| `blog.html` | Blog & Resources |

Pages to ignore/remove: `index_2/3/4.html` (alt homepages), `cart.html`, `checkout.html`, `accessories.html`, `icon_pack_*.html`, `shortcodes.html`, `tips.html`, `contacts_2.html`, `quotation_wizard.html`, `shop-single.html`.

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

1. **Every HTML file** has an identical header/footer structure — changes to nav links, logo, phone, or footer must be replicated across all kept pages (10 files total)
2. Form `action` attributes point to PHP files in `assets/` or root — update email addresses in those PHP files

## Navigation Structure

The site uses a 5-item nav menu, consistent across all 10 kept pages:

| # | Label | Page |
|---|-------|------|
| 1 | Home | `index.html` |
| 2 | Services (dropdown) | |
|   | — Web App Development | `service_web-app.html` |
|   | — Mobile App Development | `service_mobile-app.html` |
|   | — Web Hosting & Maintenance | `service_hosting.html` |
|   | — UI/UX Design | `service_uiux-design.html` |
| 3 | About | `about.html` |
| 4 | Project Inquiry | `quotation.html` |
| 5 | Contact | `contacts.html` |

**Top bar:** Left = "Bridging Cultures. Building Solutions." | Right = +632-8899-6784 + info@spiceworx.com

**Footer:** Col 1 (Logo + description) | Col 2 (Quick Links: Home, About, Services, Project Inquiry, Contact) | Col 3 (Unit 5 Ecoville, Sta. Cruz, Makati 1205) | Social icons | © SpiceWorx Consultancy, Inc. 2026

## Phase 2 Progress (Design Customization)

| Task | Status | Details |
|------|--------|---------|
| Font swap (Poppins → Open Sans) | DONE | 26 HTML/PHP files + 3 CSS files |
| Color scheme replacement | DONE | 87 occurrences across style.css, menu.css, shop.css, blog.css, date_picker.css |
| Logo replacement | DONE | SpiceWorx logo copied to img/logo.png + img/logo-footer.png, 70 HTML references updated |
| Navigation & menu structure | DONE | New 5-item menu, top bar, footer across 10 HTML files; service_uiux-design.html created |
| Icons (security → development) | TODO | Bootstrap Icons library in use; SVG icons in img/svg_icons/ |
| Images (alarm → tech themed) | TODO | Placeholder images in use; full replacements needed |

## Phase 3 Progress (Content Implementation)

| Page | Status | Details |
|------|--------|---------|
| **index.html** (Homepage) | ✅ DONE | 3-slide carousel, 6 feature boxes, "Start Your Project" form replacement, service highlights, CTA section. 514→399 lines. |
| **about.html** (About/Pivot Story) | ✅ DONE | Intro section, pivot timeline (3 boxes), "Why Choose Us" (6 boxes with gold accents), 6 core values, "Who We Serve" (3 audiences), CTA. 230→333 lines. |
| **service_hosting.html** (Web Hosting) | ✅ DONE | Hero intro, "Why Different" (4 feature boxes), "What's Included" (12 items), hosting types (3 tiers), how it works (4 steps), technical stack, migration guarantee, pricing (3 plans), FAQ (7 items), CTA. 302→658 lines. |
| **service_web-app.html** (Web Apps) | ✅ DONE | Hero intro, Why Web Apps Matter, What We Build (3-column), Tech Stack (React/Next.js/Tailwind), 4-Step Process, Why SpiceWorx (3 differentiators), 2 Case Studies, FAQ (6 items), CTA. 301→509 lines. |
| **service_mobile-app.html** (Mobile Apps) | ✅ DONE | Hero intro, Mobile-First World, What We Build (3-column: Native/Cross-Platform/PWA), Tech Stack, 5-Step Process, Why SpiceWorx, Recent Work (3 case studies), Development Philosophy, Platform Support (iOS/Android/Web), FAQ (9 items), CTA. 288→610 lines. |
| **service_uiux-design.html** (UI/UX Design) | ✅ DONE | Hero intro, Design Philosophy, What We Design (3-column), 6-Step Process, 6 Design Principles, Toolkit, Why SpiceWorx, Recent Work (4 case studies), Services with Pricing, Developer Workflow, FAQ (10 items), Our Team, CTA. 250→695 lines. |
| **contacts.html** (Contact Page) | ✅ DONE | Hero, 3-column contact info (address/phone/social), contact form (6 service checkboxes), Google Maps, Why Reach Out (3 boxes), FAQ (7 items), Alternative Contact Options, CTA. 368→486 lines. |
| **quotation.html** (Project Inquiry Form) | ✅ DONE | Hero, 9-section comprehensive form: Contact Info, Services (8 checkboxes), Project Overview (conditional URL field), Features, Design & Branding (7 checkboxes), Technical Details, Timeline & Budget (6 ranges), Additional Context (file uploads), Privacy & Submission. 368→527 lines. |
| **blog.html** (Blog & Resources) | ✅ DONE | Hero, 6 blog categories, featured article, 6 recent articles (3-column grid with category badges), newsletter signup, "Most Read This Month" widget, CTA. 395 lines. |
| **shop.html** (Hosting Packages) | ✅ DONE | Hero, Why Choose SpiceWorx Hosting (4 boxes), 3 pricing tiers (Starter $15/Professional $50/Enterprise Custom), feature comparison table, 5 add-ons, free migration, 3 testimonials, FAQ (8 items), CTA. 602 lines. |

### Content Files Implemented From
- `Homepage_Content_SpiceWorx.md` → index.html
- `About_Content_SpiceWorx.md` → about.html
- `Service_Hosting_Content_SpiceWorx.md` → service_hosting.html
- `WebApp_Content_SpiceWorx.md` → service_web-app.html
- `MobileApp_Content_SpiceWorx.md` → service_mobile-app.html
- `UIUXDesign_Content_SpiceWorx.md` → service_uiux-design.html
- `Contact_Content_SpiceWorx.md` → contacts.html
- `Quotation_Content_SpiceWorx.md` → quotation.html
- `Blog_Content_SpiceWorx.md` → blog.html
- `HostingPackages_Content_SpiceWorx.md` → shop.html

### Custom CSS Additions (css/custom.css)
- Shared: `.about_title`, `.bg_color_1`, `.call_section`, `.process_step`, `.tech_section`, `.add_top_30`, `.add_left_30`, accordion styling
- About page: `.box_feat_about`, `.reason_box`, `.value_box`, `.audience_box`
- Hosting page: `.box_feat_service`, `.feature_hosting`, `.included_service`, `.hosting_type_box`, `.tech_list`, `.guarantee_box`, `.pricing_box`, `.plan_features`, `.badge_featured`
- Web App page: `.case_study_box` (shared with Mobile App)
- Mobile App page: `.approach_box`, `.platform_box`, `.col-lg-2-4` (5-column grid)
- UI/UX Design page: `.principle_box`, `.toolkit_box`, `.service_item_box`
- Contact page: `.contact_box`, `.contact_reason_box`, `.contact_option_box`, contact form styling
- Blog page: Uses existing `.contact_box` for categories, `.box_feat_service` for articles

### Color Mapping Applied

| Old Template | → | New SpiceWorx | Role |
|---|---|---|---|
| `#FF3333` / `#F33` | → | `#C23B22` | Chili Red (CTA, accents) |
| `#e04f67` | → | `#A12F1C` | Darker Chili (hover) |
| `#e34f4f` | → | `#C23B22` | Error/alert |
| `#ed1c24` | → | `#C23B22` | Badge/social |
| `#629976` / `#619979` | → | `#3E5E3A` | Deep Olive Green |
| `#06C` | → | `#3E5E3A` | Links/buttons (was blue) |
| `#555` | → | `#333333` | Body text |
| `rgba(0,37,74,0.8)` | → | `rgba(62,94,58,0.8)` | Dark overlay |
| `#fff` (body bg) | → | `#F2F2F0` | Warm gray background |

## Company Info (for footers, contact pages, meta tags)

```
SpiceWorx Consultancy, Inc.
Unit 5 Ecoville, Sta. Cruz, Makati 1205
Phone: +632-8899-6784
Email: info@spiceworx.com
Tagline: "Bridging Cultures. Building Solutions."
```

*Note: Brand guide address (Unit 5 Ecoville, Sta. Cruz, Makati 1205) differs from earlier project brief (U7 Ecoville, Metropolitan Ave.). Use the brand guide version as authoritative.*

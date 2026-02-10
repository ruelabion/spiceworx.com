# SpiceWorx.com

**SpiceWorx Consultancy, Inc.** — Web and mobile application development company serving clients in the Philippines, Japan, and globally.

## Overview

This is a complete redesign of the **SpiceWorx** website, converting the Home Alarms v2.9 template into a modern, professional web development company site. The project focuses on showcasing SpiceWorx's digital services: Web App Development, Mobile App Development, Web Hosting & Maintenance, and UI/UX Design.

**Tagline:** "Bridging Cultures. Building Solutions."

## Project Status

### Completed (Phase 3 - Content Implementation)
- ✅ **Homepage** (`index.html`, 399 lines) — 3-slide carousel, 6 feature boxes, service highlights, CTA
- ✅ **About Page** (`about.html`, 333 lines) — 18-year pivot story, why choose us, 6 core values, 3 target audiences
- ✅ **Web App Development** (`service_web-app.html`, 509 lines) — 8 sections: hero, why web apps, what we build, tech stack, 4-step process, why SpiceWorx, 2 case studies, FAQ, CTA
- ✅ **Mobile App Development** (`service_mobile-app.html`, 610 lines) — 10 sections: hero, mobile-first world, what we build (3 types), tech stack, 5-step process, why SpiceWorx, 3 case studies, development philosophy, platform support (iOS/Android/Web), FAQ (9 items), CTA
- ✅ **UI/UX Design** (`service_uiux-design.html`, 695 lines) — 13 sections: hero, design philosophy, what we design, 6-step process, 6 design principles, toolkit, why SpiceWorx, 4 case studies, à la carte + bundled services, developer workflow, FAQ, team, CTA
- ✅ **Web Hosting & Maintenance** (`service_hosting.html`, 658 lines) — AWS infrastructure, 4 why different, 12 services, 3 hosting types, 4-step process, technical stack, guarantee, 3 pricing tiers, 7 FAQ items
- ✅ **Contact Page** (`contacts.html`, 486 lines) — 7 sections: hero, 3-column contact info, contact form with 6 service checkboxes, Google Maps, why reach out (3 reasons), FAQ (7 items), alternative contact options, dual CTA
- ✅ **Project Inquiry Form** (`quotation.html`, 527 lines) — 9-section comprehensive form: contact info, services (8 checkboxes), project overview, features, design & branding, technical details, timeline & budget, additional context (file uploads), privacy & submission
- ✅ **Blog & Resources** (`blog.html`, 395 lines) — Hero, 6 blog categories, featured article, latest articles (6 posts with read more), call_section CTA, newsletter signup
- ✅ **Hosting Packages** (`shop.html`, 602 lines) — Hero, Why Choose SpiceWorx Hosting (4 features), 3 hosting tiers with detailed specs, what's included (12 services), 4-step process, AWS technical stack, migration guarantee, FAQ (7 items), dual CTA

### All Pages Complete
All 10 main pages have been implemented with SpiceWorx-branded content. Zero template content remains.

## Quick Start

### Preview the Site

```bash
# From the template directory
cd home_alarms_v.2.9_template/html
python3 -m http.server 8000
# Visit http://localhost:8000
```

For PHP form handlers, use a PHP-capable server:
```bash
php -S localhost:8000
```

## Project Structure

```
home_alarms_v.2.9_template/html/
├── index.html                  # Homepage
├── about.html                  # About/Company Story
├── service_web-app.html        # Web App Development
├── service_mobile-app.html     # Mobile App Development
├── service_hosting.html        # Web Hosting & Maintenance
├── service_uiux-design.html    # UI/UX Design
├── quotation.html              # Project Inquiry Form
├── contacts.html               # Contact Page
├── blog.html                   # Blog & Resources
├── shop.html                   # Hosting Packages
├── css/
│   ├── style.css               # Main theme styles
│   ├── custom.css              # NEW styles (page-specific)
│   ├── menu.css                # Navigation styles
│   ├── responsive.css          # Media queries
│   └── [other stylesheets]
├── js/
│   ├── jquery-3.7.1.min.js
│   ├── bootstrap.bundle.min.js
│   ├── functions.js
│   └── [other scripts]
├── img/
│   ├── logo.png                # SpiceWorx logo
│   ├── logo-footer.png
│   └── [60+ image assets]
└── assets/
    ├── contact.php             # Contact form handler
    └── [form handlers]
```

## Technology Stack

- **Framework:** Bootstrap 5
- **Typography:** Open Sans (Google Fonts)
- **Icons:** Bootstrap Icons, Elegant Icons, Fontello
- **Carousel/Sliders:** Owl Carousel
- **Build:** None — static HTML/CSS/JS (no bundler)

## Branding

### Color Palette
| Color | Hex | Usage |
|-------|-----|-------|
| Primary Green | `#3E5E3A` | Headers, buttons, nav |
| Warm Gray | `#F2F2F0` | Page backgrounds |
| Chili Red | `#C23B22` | CTAs, accents, hover |
| Charcoal | `#333333` | Body text |
| Sage Green | `#7A8E72` | Hover highlights |
| Gold | `#C9A552` | Sparingly (max 1 section) |

### Typography
- **Headings:** Open Sans Bold (700)
- **Body:** Open Sans Regular (400)
- **Quotes:** Open Sans Italic

### Logo
- Green wordmark with red "i" (chili pepper symbol)
- 214×44px in headers/footers
- Source: `img/logo.png`, `img/logo-footer.png`

## Company Info

```
SpiceWorx Consultancy, Inc.
Unit 5 Ecoville, Sta. Cruz
Makati 1205, Philippines

Phone: +632-8899-6784
Email: info@spiceworx.com
```

## Key Features Implemented

### Homepage
- 3-slide hero carousel with CTAs
- 6 feature boxes (Development, Technologies, Mobile-First, Hosting, Support, Communication)
- "Start Your Project in 3 Simple Steps" section
- 3 service highlight boxes with links to service pages
- "Let's Build Something Great" partnership CTA
- Updated footer with Blog link

### About Page
- "Bridging Cultures. Building Solutions." headline
- 18-year company history → digital pivot narrative
- 3-box timeline (Building Trust 2006-2024 → Pattern Recognition → Evolution 2024+)
- 6 "Why Choose Us" boxes with gold accent numbers
- 6 core values (Clarity, Trust, Cultural Fluency, Innovation, Efficiency, Excellence)
- 3 target audiences (Japanese, Philippine, Global)
- Zero-downtime migration guarantee

### Web Hosting Page
- AWS expertise positioning
- 4 "Why Different" feature boxes (Infrastructure, Serverless, Developer Support, Security)
- 12 included services (SSL, CDN, Backups, DNS, Lambda, etc.)
- 3 hosting types (Static $15-50/mo, WordPress $50-150/mo, Enterprise Custom)
- 4-step process (Choose → Configure → Migrate → Launch)
- Technical stack details (S3, CloudFront, Route 53, Lambda, RDS, etc.)
- 3 pricing tiers with feature matrix
- 7 FAQ items
- Zero-downtime migration guarantee

### Web App Development Page
- Hero section: "Modern Web Apps Built for Global Business"
- Why Web Apps Matter (business value positioning)
- What We Build (3-column: Custom Apps, E-Commerce, Customer-Facing Platforms)
- Technology Stack (React, Next.js, Tailwind CSS, Full-Stack)
- 4-Step Process (Discovery, Design, Development, Launch)
- Why SpiceWorx (3 differentiators: Speed, Security, Scalability)
- 6 FAQ items with comprehensive answers
- CTA: "Ready to Build Something Better?" (dual CTAs)

### Mobile App Development Page
- Hero section: "Mobile Apps That Connect Your Customers Anywhere"
- Mobile-First World positioning ("Your Business Moves. Your App Should Too")
- What We Build (3 types: Native iOS/Android, Cross-Platform Solutions, Progressive Web Apps)
- Technology Stack (Swift/Kotlin, Flutter/React Native, Backend & Cloud, Security & Offline-First)
- 5-Step Process (Discovery & Strategy, UX/UI Design, Development, Testing & Optimization, Launch & Ongoing Support)
- Why SpiceWorx (3 differentiators: Performance That Feels Native, Works Everywhere Offline or Not, Global Compliance Built In)
- 3 Detailed Case Studies (Field Operations, Customer Loyalty Platform, B2B Procurement Mobile App)
- Development Approach & Philosophy (Usability, Performance, Reliability, Privacy, Accessibility)
- Platform Support (iOS with device specs, Android with API levels, Web/PWA support)
- 9 FAQ items (app timeline, native vs cross-platform, offline capability, cost, submission, maintenance, feature additions, push notifications, analytics)
- CTA: "Let's Build Your Mobile Future" (Start Your Project + Schedule a Consultation)

### UI/UX Design Page
- Hero section: "Design That Works As Hard As Your Business"
- Great Design Is Invisible (design philosophy positioning)
- What We Design (3 types: Web/App Interfaces, UX Strategy, Design Systems)
- 6-Step Design Process (Research, Strategy, Wireframes, Visual Design, Testing, Handoff)
- 6 Core Design Principles (User-Centered, Clarity, Accessibility, Mobile-First, Performance, Cultural Awareness)
- Our Toolkit & Expertise (Figma, Adobe XD, Sketch, Protopie; User Research Tools; Design Expertise)
- Why SpiceWorx (3 differentiators: User Research, Design Systems, Performance + Beauty)
- 4 Detailed Case Studies (B2B Portal, E-Commerce, SaaS Design System, Mobile Learning App)
- À la Carte Services ($4K-$30K range) — User Research, UX Strategy, Wireframing, Visual Design, Usability Testing, Design Systems
- Bundled Services ($35K-$75K range) — Complete Website/App Design, Design System + Implementation
- How We Work With Developers (6 key deliverables)
- 10 FAQ items covering cost, timeline, process, accessibility, developer handoff
- CTA: "Ready to Design Something Great?" (dual CTAs)

## CSS Custom Styles

All new component styles are in `css/custom.css` to preserve the original template and maintain cascading priority. Organized by page:

**Shared Components:**
- Section title blocks (`.about_title`)
- Alternating backgrounds (`.bg_color_1`)
- CTA sections (`.call_section`)
- Process steps with numbered circles (`.process_step`)
- Accordions (`.accordion`, `.accordion-item`, `.accordion-button`, `.accordion-body`)

**About & Service Pages:**
- Feature boxes (`.box_feat_about`, `.box_feat_service`, `.feature_hosting`)
- Specialty boxes (`.reason_box`, `.value_box`, `.audience_box`)

**Web Hosting Page:**
- Service list items (`.included_service`)
- Hosting type boxes (`.hosting_type_box`)
- Technical stack lists (`.tech_list`)
- Pricing boxes (`.pricing_box`, `.plan_features`, `.badge_featured`)
- Guarantee box (`.guarantee_box`)

**Web App Page:**
- Tech section boxes (`.tech_section`)
- Spacing utilities (`.add_left_30`)

**Mobile App Page:**
- Case study boxes (`.case_study_box`)
- Development approach boxes (`.approach_box`)
- Platform support boxes (`.platform_box`)
- 5-column grid helper (`.col-lg-2-4`)

**UI/UX Design Page:**
- Design principle boxes (`.principle_box`)
- Toolkit boxes (`.toolkit_box`)
- Service item boxes (`.service_item_box`)

**Contact Page:**
- Contact info boxes (`.contact_box`)
- Contact reason boxes (`.contact_reason_box`)
- Contact option boxes (`.contact_option_box`)

**Blog Page:**
- Reuses existing `.contact_box` for blog categories
- Reuses existing `.box_feat_service` for blog articles

## Navigation

Consistent 5-item menu across all pages:
1. **Home** → `index.html`
2. **Services** (dropdown)
   - Web App Development → `service_web-app.html`
   - Mobile App Development → `service_mobile-app.html`
   - Web Hosting & Maintenance → `service_hosting.html`
   - UI/UX Design → `service_uiux-design.html`
3. **About** → `about.html`
4. **Project Inquiry** → `quotation.html`
5. **Contact** → `contacts.html`

**Top bar:** Tagline (left) | Phone + Email (right)
**Footer:** Logo, Quick Links, Contact Info, Social Icons

## Content Specifications

Content for each page is documented in (located in `/Users/ruelabion/Downloads/` and `/Users/ruelabion/Downloads/files/`):
- ✅ `Homepage_Content_SpiceWorx.md` → Implemented in index.html
- ✅ `About_Content_SpiceWorx.md` → Implemented in about.html
- ✅ `Service_Hosting_Content_SpiceWorx.md` → Implemented in service_hosting.html
- ✅ `WebApp_Content_SpiceWorx.md` → Implemented in service_web-app.html
- ✅ `MobileApp_Content_SpiceWorx.md` → Implemented in service_mobile-app.html
- ✅ `UIUXDesign_Content_SpiceWorx.md` → Implemented in service_uiux-design.html
- ✅ `Contact_Content_SpiceWorx.md` → Implemented in contacts.html
- ✅ `Quotation_Content_SpiceWorx.md` → Implemented in quotation.html
- ✅ `Blog_Content_SpiceWorx.md` → Implemented in blog.html
- ✅ `Shop_Content_SpiceWorx.md` → Implemented in shop.html

## Next Steps

1. **Image & Icon Replacements** (Enhancement)
   - Replace alarm/security theme images with tech/development imagery
   - Verify Bootstrap Icons usage across all service pages
   - Optimize SVG icons in img/svg_icons/

2. **Testing & QA** (Validation)
   - Cross-browser testing (Chrome, Safari, Firefox, Edge)
   - Responsive design verification (mobile, tablet, desktop)
   - Form handler testing (PHP contact/quotation forms)
   - Link verification across all pages

3. **SEO & Analytics** (Finalization)
   - Verify all meta tags (title, description, keywords) on every page ✅ Done
   - Add structured data (Schema.org markup)
   - Analytics tracking setup
   - Google Search Console verification

## Development Notes

- **No build system** — Direct HTML/CSS/JS edits
- **All new styles in `custom.css`** — Never edit style.css or other core files
- **Bootstrap 5 responsive grid** — Mobile-first approach
- **Form handlers** — PHP files in `assets/` require PHP server for testing
- **Content sources** — Use `/Users/ruelabion/Sites/CodeCommit/spiceworx.com/html/` as reference for old site content

## Contributing

When updating content or styles:
1. Read `CLAUDE.md` for branding guidelines and architecture
2. Add new CSS to `custom.css` only
3. Keep headers/footers consistent across all pages
4. Update navigation if adding/removing pages
5. Test responsive design on mobile/tablet/desktop
6. Verify all internal links work

---

**Status:** Phase 3 Complete (All 10 main pages completed)
**Last Updated:** February 9, 2026
**Contact:** info@spiceworx.com
**Completion:** 100% — All pages complete: Homepage, About, Web App Development, Mobile App Development, UI/UX Design, Web Hosting & Maintenance, Contact, Project Inquiry Form, Blog & Resources, Hosting Packages

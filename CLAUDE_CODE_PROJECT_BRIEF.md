# SpiceWorx Website Project Brief for Claude Code

## Project Overview
Converting the Home Alarms v2.9 template into the new SpiceWorx.com website focused on web and mobile development services.

## Background Context

### Previous Business (Archive)
- SpiceWorx was a Japan-Philippine business consultancy
- Offered cross-cultural training and consulting services
- Old website: https://www.spiceworx.com (to be archived to legacy.spiceworx.com)

### New Business Direction
- **Primary Services:**
  1. Web Application Development
  2. Mobile Application Development (iOS/Android/Cross-platform)
  3. Web Hosting & Maintenance
  4. UI/UX Design (if offered)

### Target Website Structure
```
SpiceWorx.com (New Site)
├── Homepage - Clear value proposition + service overview
├── Services
│   ├── Web Application Development
│   ├── Mobile Application Development
│   ├── Web Hosting & Maintenance
│   └── UI/UX Design
├── Portfolio/Work - Case studies of completed projects
├── About Us - Company story (mention the pivot)
├── Technologies - Tech stack and expertise
├── Process - How we work (Discovery → Design → Dev → Test → Launch → Support)
├── Blog/Resources - Technical articles and case studies
└── Contact - Project inquiry form
```

## Source Template Analysis

### Template: Home Alarms v2.9
- **Type:** HTML/CSS/JS template for alarm/security systems business
- **Framework:** Bootstrap 5
- **Key Libraries:** jQuery, LayerSlider, Owl Carousel
- **Structure:** Well-organized, responsive, professional quality

### Template Components Available
✅ Multiple homepage variations (index.html, index_2.html, index_3.html, index_4.html)
✅ Service showcase pages (service_layout_1/2/3.html)
✅ About page
✅ Blog system (blog.html, blog_post.html)
✅ Contact forms (contacts.html, contacts_2.html)
✅ Quote request forms (quotation.html, quotation_wizard.html)
✅ Shop/eCommerce pages (can repurpose or remove)
✅ Portfolio/gallery layouts
✅ Team sections
✅ Testimonials

### Assessment Results
- **Suitability:** 85% - Highly Recommended with Modifications
- **Difficulty:** Moderate (3/5)
- **Estimated Effort:** 18-26 hours total
- **Main Challenges:** Content replacement, rebranding, image updates

## Modification Plan

### Phase 1: Setup & Planning (2-3 hours)
- [x] Template extracted and analyzed
- [ ] Map current pages to new structure
- [ ] Create content inventory
- [ ] Identify pages to keep/remove/repurpose

### Phase 2: Design Customization (4-6 hours)
**Color Scheme Changes:**
- Current: Blue/security-focused theme
- New: SpiceWorx brand colors (TBD - need brand guidelines)
- Files to modify: `css/style.css`, `css/custom.css`

**Logo & Branding:**
- [ ] Replace logo files
- [ ] Update favicon
- [ ] Change fonts if needed

**Images:**
- [ ] Replace all security/alarm images with tech/development themed
- [ ] Update hero/banner images
- [ ] Add portfolio project screenshots

**Icons:**
- [ ] Change security icons to development icons
- [ ] Utilize existing icon libraries (Elegant Icons, Fontello, Bootstrap Icons)

### Phase 3: Content Migration (6-8 hours)

**Homepage (index.html):**
- Current: Alarm systems hero section
- New: Web/mobile development value proposition
- Services showcase: Web Dev, Mobile Dev, Hosting
- Call-to-action: "Start Your Project" instead of "Get Quote"

**Service Pages:**
- Convert service_layout_1.html → Web Application Development
- Convert service_layout_2.html → Mobile Application Development  
- Convert service_layout_3.html → Web Hosting & Maintenance
- Add: UI/UX Design page (if needed)

**About Page:**
- Brief mention: "Originally founded as Japan-Philippine consultancy, evolved to meet demand for digital solutions"
- Focus on: Development expertise, team, mission

**Forms:**
- quotation.html → Project Inquiry Form
- Update fields: Project type, budget range, timeline, tech requirements
- Remove alarm-specific fields

**Blog:**
- Keep structure for technical articles
- Repurpose for case studies, dev tips, industry insights

### Phase 4: Feature Customization (4-6 hours)
- [ ] Configure contact forms with new email
- [ ] Remove/repurpose shop section (could be hosting packages)
- [ ] Set up blog categories (Web Dev, Mobile Dev, Case Studies, Tips)
- [ ] Add portfolio filtering (by technology, industry, service type)

### Phase 5: Testing & Launch (2-3 hours)
- [ ] Cross-browser testing
- [ ] Mobile responsiveness check
- [ ] Form functionality testing
- [ ] SEO optimization (meta tags, descriptions)
- [ ] Performance optimization
- [ ] Set up old site archive at legacy.spiceworx.com

## Key Files to Modify

### Priority 1 - Critical
```
index.html                    → Homepage (main landing)
css/custom.css               → Your custom overrides
css/style.css                → Main styling (colors, branding)
about.html                   → Company information
service_layout_1.html        → Web Development service
contacts.html                → Contact page
```

### Priority 2 - Important
```
service_layout_2.html        → Mobile Development service
service_layout_3.html        → Hosting service
blog.html, blog_post.html    → Blog system
quotation.html               → Project inquiry form
img/logo.png                 → Company logo
img/favicon.ico              → Browser icon
```

### Priority 3 - Optional
```
shop.html, shop-single.html  → Repurpose or remove
index_2/3/4.html            → Alternative homepage layouts
coming_soon/                 → Pre-launch page (if needed)
```

## Content Guidelines

### Tone & Voice
- Professional but approachable
- Technical but not jargon-heavy
- Focus on solving client problems
- Emphasize partnership and collaboration

### Key Messages
1. "From concept to launch, we build digital solutions"
2. "Expert web and mobile development for modern businesses"
3. "Your partner in digital transformation"
4. Mention 18+ years of business experience (pivot story)

### SEO Keywords (Target)
- Web application development Philippines
- Mobile app development Manila
- Custom software development
- Web hosting services
- UI/UX design Philippines

## Technical Specifications

### Current Stack (Template)
- HTML5
- CSS3
- Bootstrap 5.x
- jQuery 3.7.1
- LayerSlider (premium slider)
- Owl Carousel
- Magnific Popup
- PHP (for form processing)

### Browser Support
- Chrome, Firefox, Safari, Edge (latest 2 versions)
- Mobile: iOS Safari, Chrome Mobile
- IE11 support: Not required

### Responsive Breakpoints (Bootstrap)
- XS: <576px (mobile)
- SM: ≥576px (mobile landscape)
- MD: ≥768px (tablet)
- LG: ≥992px (desktop)
- XL: ≥1200px (large desktop)

## Contact Information

### Company Details (for footer/contact)
```
SpiceWorx Consultancy, Inc.
U7 Ecoville, Metropolitan Ave.
Makati City, Philippines

Phone: +632-8899-6784
Email: info@spiceworx.com (confirm if still active)

Archive Site: legacy.spiceworx.com (old consultancy site)
```

## Important Decisions Needed

Before proceeding, please confirm:

1. **Brand Colors:** What are the official SpiceWorx brand colors for the new direction?
   - Primary color: (hex code)
   - Secondary color: (hex code)
   - Accent color: (hex code)

2. **Logo:** Do you have a new logo, or keeping the existing one?

3. **Services:** Confirm the exact services to feature:
   - [ ] Web Application Development
   - [ ] Mobile Application Development
   - [ ] Web Hosting & Maintenance
   - [ ] UI/UX Design
   - [ ] Other: _______________

4. **Portfolio:** Do you have project screenshots/case studies ready?

5. **Team:** Include team member photos/bios?

6. **Blog:** Will you actively maintain a blog?

7. **Shop Section:** Keep, remove, or repurpose for hosting packages?

8. **Old Site:** Confirm archive at legacy.spiceworx.com?

## Claude Code Commands to Start

Once you have the template in your project folder, use these commands:

```bash
# Initialize the project
claude-code init

# First assessment
claude-code "Review the template structure and confirm the modification plan from the project brief"

# Start with branding
claude-code "Update the color scheme throughout all CSS files based on our brand colors"

# Homepage first
claude-code "Modify index.html to reflect SpiceWorx as a web/mobile development company"

# Service pages
claude-code "Convert service_layout_1.html to showcase Web Application Development services"
```

## Reference Links

- Old SpiceWorx site: https://www.spiceworx.com
- Template documentation: Check `/documentation/` folder
- Assessment document: See SpiceWorx_Template_Modification_Assessment.md

## Success Criteria

The project is complete when:
- [ ] All pages reflect web/mobile development services (not alarms)
- [ ] Brand colors and logo updated throughout
- [ ] All images replaced with relevant tech/development visuals
- [ ] Forms configured for project inquiries
- [ ] Portfolio section shows development projects
- [ ] Responsive on all devices
- [ ] Contact forms functional
- [ ] Old site archived at legacy.spiceworx.com
- [ ] SEO optimized (meta tags, descriptions)
- [ ] Cross-browser tested

---

**Project Start Date:** February 8, 2026  
**Status:** Planning Phase  
**Next Step:** Provide brand guidelines and begin Phase 2 (Design Customization)

---

## Notes for Claude Code

This project involves converting an alarm systems template to a web development company site. The structure and components are suitable, but every reference to alarms, security, quotes for alarm systems, etc. needs to be replaced with web/mobile development equivalents.

Focus areas:
1. Content transformation (security → development)
2. Visual rebranding (colors, logos, images)
3. Form adaptation (alarm quotes → project inquiries)
4. Service pages (alarm systems → web/mobile services)

The template quality is good, so preserve the structure and just modify content, visuals, and branding.

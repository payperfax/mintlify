# Comprehensive Mintlify Codebase Analysis

## Overall File and Folder Structure

```
/home/adam/mintlify/
├── docs.json                          # Main Mintlify configuration
├── index.mdx                          # Home page
├── faq.mdx                            # FAQ page
├── README.md                          # Project documentation
├── CLAUDE.md                          # Project-specific instructions
├── favicon.svg                        # Site favicon
├── logo/
│   └── ppf_logo.png                  # PayPerFax logo
├── .claude/                           # Claude settings
├── getting-started/
│   ├── quick-start.mdx               # 3-step quick start guide
│   └── how-it-works.mdx              # Service explanation
├── sending-faxes/
│   ├── step-by-step-guide.mdx        # Detailed instructions with screenshots
│   ├── cover-pages.mdx               # Cover page usage guide
│   └── file-requirements.mdx         # Supported formats and specs
├── features/
│   ├── service-features.mdx          # Complete feature overview
│   ├── country-coverage.mdx          # Geographic coverage details
│   ├── browser-extension.mdx         # Tracker extension info
│   └── dropbox-integration.mdx       # Dropbox integration guide
├── pricing/
│   └── pricing.mdx                   # Pricing breakdown
└── troubleshooting/
    ├── common-issues.mdx             # Quick solutions hub
    ├── fax-not-received.mdx          # Delivery troubleshooting
    ├── low-quality-confirmations.mdx # Quality issues
    └── resending-faxes.mdx           # Retry instructions
```

## Navigation Structure (from docs.json)

The documentation is organized into **6 main groups** within a single "Documentation" tab:

1. **Getting Started** (3 pages): index, quick-start, how-it-works
2. **Sending Faxes** (3 pages): step-by-step-guide, cover-pages, file-requirements
3. **Pricing & Payments** (1 page): pricing
4. **Features** (4 pages): service-features, country-coverage, browser-extension, dropbox-integration
5. **Troubleshooting** (4 pages): common-issues, fax-not-received, low-quality-confirmations, resending-faxes
6. **FAQ** (1 page): faq

**Global navigation elements:**
- Navbar links: "About Us" and "Contact" (external links)
- Primary CTA: "Send a Fax" button linking to app
- Toolbar anchors: "PayPerFax Home" and "Send a Fax" links

## Key Patterns and Conventions

### MDX Component Library

The documentation heavily uses Mintlify MDX components:
- **Card & CardGroup**: Feature showcases, quick links, related topics (cols: 2, 3, or auto)
- **Accordion & AccordionGroup**: Expandable detailed explanations
- **Steps**: Sequential processes (quick-start has 3 steps, step-by-step has 7)
- **Callouts**: Info, Tip, Warning, Note boxes
- **Tabs**: Available but not heavily used

### Front Matter (YAML Headers)

All pages follow consistent structure:
```yaml
---
title: "Page Title"
description: "Brief description for SEO/preview"
icon: "fontawesome-icon"  # Optional, shown in navigation
---
```

### Content Architecture Patterns

**Quick Scan Friendly:**
- Short introductory paragraph
- Quick-access cards or accordions for common questions
- Links to detailed explanations elsewhere

**Hub-and-Spoke Model:**
- `common-issues.mdx` acts as a hub linking to specialized troubleshooting pages
- `index.mdx` acts as homepage hub with CardGroup linking to key sections
- Prevents content duplication by directing users to detailed pages

**Cross-Linking Strategy:**
- Heavy use of internal links via Cards (with icons/colors)
- Related topics sections at bottom of pages
- Links to more detailed explanations (e.g., "See [File Requirements](/sending-faxes/file-requirements)")

### Visual Design Conventions

**Color Usage:**
- Primary blue (#2563EB) for main branding
- Green (#16A34A) for positive/success features
- Purple (#7C3AED) for special features
- Amber/Orange for time/availability

**Icon Conventions:**
- Feature pages use descriptive icons (sparkles, globe, lock, etc.)
- Navigation uses Fontawesome icons
- Cards in related topics use topic-relevant icons

**Layout Defaults:**
- CardGroup uses 2-3 columns
- Tables and structured lists in accordions
- Images from payperfax.com domain (no local copies)

### Heading Hierarchy

Standard pattern:
```
## Main Section (H2)
### Subsection (H3, rarely used)
- Detailed content in accordions/cards
- Steps for procedures
- Tables or lists for reference
```

### Copy Tone & Style

- **Conversational**: "Don't worry!", "Just upload..."
- **Action-oriented**: Uses imperatives ("Click", "Enter", "Select")
- **Reassuring**: Emphasizes "no surprises", "guaranteed", "risk-free"
- **Transparent**: Explains payment holds, retry logic, failed faxes clearly
- **Mobile-aware**: Instructions work on "any device"

## Configuration Details

**Theme**: "mint" (Mintlify theme)

**Color Scheme**:
- Primary: #2563EB (blue)
- Light: #60A5FA (light blue)
- Dark: #1E40AF (dark blue)

**Favicon**: Hosted at payperfax.com (no local copy)

**Logo**: Local file `/logo/ppf_logo.png` (used for both light/dark modes)

## Content Sourcing

- Sources: payperfax.com/user-guide/, /faq/, /llms.txt
- Text and images only (no code samples)
- End-user documentation (not developer docs)
- All images use direct payperfax.com URLs (no local copies)

## Key Content Facts

- **Pricing**: "$2.00 for 3 pages, $0.75 per additional page"
- **Trust elements**: SSL, auto-deletion, Trustpilot rating (4.7★)
- **CTA**: "Send a Fax" buttons link to https://fax.payperfax.com
- **No API documentation** - purely end-user/customer-facing

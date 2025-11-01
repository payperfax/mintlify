# PayPerFax Documentation Site

## Project Overview

This is a Mintlify-based documentation site for [PayPerFax.com](https://payperfax.com), a pay-per-use online fax service. The documentation provides user guides, FAQs, troubleshooting, and feature information.

**Key Characteristics:**
- **No API documentation** - This is end-user documentation, not developer docs
- **No code samples** - Text and images only, focused on user instructions
- **Content sources**: payperfax.com/user-guide/, /faq/, /llms.txt

## Documentation Structure

The site is organized into 6 main sections:

1. **Getting Started** - Quick start and "How it works"
2. **Sending Faxes** - Step-by-step guides, cover pages, file requirements
3. **Pricing & Payments** - Single consolidated page (pricing, payment methods, authorization holds)
4. **Features** - Service features, country coverage, browser extension
5. **Troubleshooting** - Hub-and-spoke model with common issues linking to specific guides
6. **FAQ** - Frequently asked questions in accordion format

## User Preferences & Design Principles

Based on user feedback, prioritize:

1. **Reduce user fatigue** - Avoid repetitive explanations across pages
   - First mention: Explain fully
   - Subsequent mentions: Brief with link to detailed explanation
   - Example: Authorization holds explained once in pricing, linked elsewhere

2. **Avoid fragmentation** - Don't split simple answers across multiple pages
   - User preference: "the answer is basically '$2 for first three pages + $0.75', so doesn't need an entire page"
   - Consolidate related topics when the content is straightforward

3. **Liberal use of MDX components** - Make pages visually appealing
   - Use Card, CardGroup, Accordion, AccordionGroup, Steps, Tabs
   - Use Info, Warning, Note, Tip callouts appropriately

4. **Brief integrations** - When merging content, keep it concise
   - User feedback: "go for option b, keeping the merged part brief"

## Technical Details

**Platform:** Mintlify (MDX-based documentation)

**Configuration:** `docs.json`
- Color scheme: Blue (#2563EB primary, #60A5FA light, #1E40AF dark)
- Logo: `/logo/ppf_logo.png`
- Navigation structure defined in `navigation.tabs`

**Images:** All images use direct URLs to payperfax.com website
- No local image copies
- Images automatically stay current with main site

**Key Content Patterns:**
- Authorization holds: Detailed explanation in pricing/pricing.mdx only
- Fax resolution (204×196 dpi): Detailed explanation in troubleshooting/low-quality-confirmations.mdx only
- Automatic retry timing: Detailed explanation in troubleshooting/resending-faxes.mdx only

## Service Details

**PayPerFax Service:**
- Pay-per-use fax service (no registration required)
- $2.00 for first 3 pages, $0.75 per additional page
- Payment: Credit card or PayPal
- Pay-on-success model (authorization hold, only charged if fax succeeds)
- 130+ countries supported
- Supported formats: PDF, DOC, DOCX, TIF, JPEG (max 8MB)
- Fax resolution: 204×196 dpi (international standard)

## Recent Changes

**Documentation Consolidation** (Latest work):
- Merged preview-and-pricing into step-by-step-guide (kept brief)
- Consolidated 3 pricing pages into single pricing/pricing.mdx
- Updated all cross-references throughout documentation
- Structure reduced from 18 pages to 15 pages

## Future Guidance

When working on this documentation:
1. Always check if content already exists elsewhere before adding new explanations
2. Link to detailed explanations rather than repeating them
3. Consider consolidation when answers are simple and straightforward
4. Use MDX components liberally for visual appeal
5. Keep merged content brief unless detailed explanation is warranted
6. Maintain hub-and-spoke model in troubleshooting section

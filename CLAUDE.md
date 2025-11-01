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
3. **Pricing & Payments** - Single consolidated page
4. **Features** - Service features, country coverage, browser extension
5. **Troubleshooting** - Hub-and-spoke model with common issues linking to specific guides
6. **FAQ** - Frequently asked questions in accordion format

## Design Principles

Based on user feedback, prioritize:

1. **Reduce user fatigue** - Avoid repetitive explanations across pages
   - First mention: Explain fully
   - Subsequent mentions: Brief with link to detailed explanation

2. **Avoid fragmentation** - Don't split simple answers across multiple pages
   - Consolidate related topics when the content is straightforward

3. **Liberal use of MDX components** - Make pages visually appealing
   - Use Card, CardGroup, Accordion, AccordionGroup, Steps, Tabs
   - Use Info, Warning, Note, Tip callouts appropriately

4. **Brief integrations** - When merging content, keep it concise

## Technical Details

**Platform:** Mintlify (MDX-based documentation)

**Configuration:** `docs.json`
- Color scheme: Blue (#2563EB primary, #60A5FA light, #1E40AF dark)
- Logo: `/logo/ppf_logo.png`
- Navigation structure defined in `navigation.tabs`

**Images:** All images use direct URLs to payperfax.com website
- No local image copies
- Images automatically stay current with main site

## Future Guidance

When working on this documentation:
1. Always check if content already exists elsewhere before adding new explanations
2. Link to detailed explanations rather than repeating them
3. Consider consolidation when answers are simple and straightforward
4. Use MDX components liberally for visual appeal
5. Keep merged content brief unless detailed explanation is warranted
6. Maintain hub-and-spoke model in troubleshooting section

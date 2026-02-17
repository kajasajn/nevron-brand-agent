# Nevron Document Guide

Rules and templates for creating on-brand documents (PDF, Word, Google Docs).

---

## Page Setup

| Setting | A4 | US Letter |
|---------|------|-----------|
| **Size** | 210 x 297 mm | 8.5 x 11" |
| **Top margin** | 25 mm | 1" |
| **Bottom margin** | 25 mm | 1" |
| **Left margin** | 20 mm | 0.8" |
| **Right margin** | 20 mm | 0.8" |

---

## Header & Footer

### Header
- **Left:** Nevron logo (without tagline, blue variant)
- **Right:** Page number
- **Style:** Logo height ~10mm. Page number in S3 gray, Caption size (12px)
- **Separator:** None (keep it clean) or subtle S5 line

### Footer
- **Left:** `nevron.eu` in S4 gray
- **Center:** Document title or section (optional)
- **Right:** `Confidential` label if needed, in S4 gray
- **Separator:** Thin S5 `#D3D5D6` line, 1pt

### Skip on Cover Page
No header or footer on the cover/title page.

---

## Cover Page

```
┌─────────────────────────────┐
│                             │
│                             │
│     [Logo with tagline]     │  Centered, upper third
│                             │  Blue variant on white bg
│                             │
│                             │
│     Document Title          │  M1 Navy, Display (48px) or H1 (36px)
│     Subtitle (optional)    │  S2 Dark Gray, H3 (22px)
│                             │
│                             │
│                             │
│                             │
│                             │
│     Date | Version          │  S3 Medium Gray, Body Small (14px)
│     Author (optional)       │  Bottom area
│                             │
└─────────────────────────────┘
```

**Rules:**
- Logo: With tagline, blue, centered horizontally
- Title: M1 `#000126`, centered, bold
- No header/footer on this page
- Optional: M3 accent line below title

---

## Typography Hierarchy

| Level | Font Size | Weight | Color | Usage |
|-------|-----------|--------|-------|-------|
| Document Title | 36px (H1) | Bold (700) | M1 `#000126` | Cover page title |
| Section Header | 28px (H2) | SemiBold (600) | M3 `#0067B2` | Major sections |
| Subsection | 22px (H3) | SemiBold (600) | S1 `#080C13` | Subsections |
| Sub-subsection | 18px (H4) | SemiBold (600) | S1 `#080C13` | Minor headers |
| Body | 16px | Regular (400) | S1 `#080C13` | Default text |
| Body Small | 14px | Regular (400) | S2 `#2C3038` | Captions, notes |
| Caption | 12px | Regular (400) | S3 `#6B7077` | Footnotes, labels |

### Paragraph Formatting
- **Line spacing:** 1.15 for dense docs, 1.5 for readable docs
- **Paragraph spacing:** 12px after paragraphs
- **First line indent:** None (use paragraph spacing instead)
- **Alignment:** Left-aligned. Never justify body text (causes uneven spacing)

---

## Content Elements

### Links
- Color: M3 `#0067B2`
- Style: Underlined
- Include full URL in print documents (footnote or inline)

### Bullet Lists
- Bullet character: Round bullet or em dash
- Bullet color: M3 Brand Blue (if customizable)
- Indent: 20px per level
- Max nesting: 2 levels deep

### Numbered Lists
- Number color: M3 Brand Blue (if customizable)
- Same indent rules as bullets

### Blockquotes / Pull Quotes
- Left border: 3px solid M3 `#0067B2`
- Padding left: 16px
- Text: Italic, S2 `#2C3038`
- Font size: Body Large (18px)

### Tables

```
┌────────────────┬──────────────┬──────────────┐
│  Header Cell   │  Header Cell │  Header Cell │  M1 Navy bg, White text, Bold
├────────────────┼──────────────┼──────────────┤
│  Data cell     │  Data cell   │  Data cell   │  White bg, S1 text
├────────────────┼──────────────┼──────────────┤
│  Data cell     │  Data cell   │  Data cell   │  S6 Off White bg (alternating)
├────────────────┼──────────────┼──────────────┤
│  Data cell     │  Data cell   │  Data cell   │  White bg
└────────────────┴──────────────┴──────────────┘
```

**Table rules:**
- Header row: M1 `#000126` background, White text, Bold
- Body rows: Alternating White / S6 `#EFF0F0`
- Borders: S5 `#D3D5D6`, 1px
- Cell padding: 8px vertical, 12px horizontal
- Text alignment: Left for text, right for numbers
- Font size: Body Small (14px) if table is dense

### Code Blocks
- Background: S6 `#EFF0F0`
- Border: 1px S5 `#D3D5D6`
- Border radius: 4px
- Font: Monospace, Body Small (14px)
- Padding: 16px

### Callout Boxes

| Type | Left Border | Background | Icon |
|------|-------------|------------|------|
| Info | M3 `#0067B2` | M6 `#E1F4FF` | i |
| Warning | Orange `#E56600` | Light orange | ! |
| Error | Red `#DA2025` | Light red | x |
| Success | Green `#36A058` | Light green | check |

---

## Document Types

### Proposal / Offer
1. Cover page with client name
2. Table of contents
3. Executive summary
4. Solution overview (with visuals)
5. Pricing / packages
6. Timeline
7. About Nevron
8. Terms & conditions

### Technical Documentation
1. Cover page with version
2. Table of contents
3. Introduction / scope
4. Technical sections with diagrams
5. API references (if applicable)
6. Appendices

### Internal Report
1. Title + date (no full cover needed)
2. Summary / key findings
3. Detailed sections
4. Recommendations
5. Next steps

---

## General Rules

| Rule | Details |
|------|---------|
| **Page numbers** | Always (except cover page) |
| **Widows/orphans** | Avoid single lines at top/bottom of page |
| **Images** | Caption below, S3 color, Body Small size |
| **Diagrams** | Use brand blues (M3, M4, M5) for elements |
| **File naming** | `Nevron_DocumentType_ClientName_YYYY-MM-DD.pdf` |
| **Metadata** | Set author to "Nevron" in document properties |
| **Confidentiality** | Mark confidential docs in footer |

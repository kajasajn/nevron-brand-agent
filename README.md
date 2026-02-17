# Nevron Brand Agent

A standalone Claude Code agent that enforces Nevron brand consistency across all output formats — web, presentations, documents, and print.

## What's Included

```
nevron-brand-agent/
├── agent/
│   └── nevron-brand.md          # The agent (install this)
├── assets/
│   ├── logos/                   # SVG logos (monogram, with/without tagline)
│   └── fonts/
│       └── README.md            # Font licensing info
├── tokens/
│   └── nevron-tokens.css        # CSS custom properties (all brand tokens)
└── examples/
    ├── web-component.html       # Branded feature card demo
    ├── presentation-guide.md    # PowerPoint/Keynote slide templates
    └── document-guide.md        # PDF/Word document formatting
```

## Installation

### 1. Clone the repo

```bash
git clone https://github.com/nevabordev/nevron-brand-agent.git
```

### 2. Install the agent

Copy the agent file to your Claude Code agents folder:

**Windows:**
```bash
cp agent/nevron-brand.md "$HOME/.claude/agents/"
```

**macOS/Linux:**
```bash
cp agent/nevron-brand.md ~/.claude/agents/
```

### 3. Restart Claude Code

Close and reopen Claude Code (or start a new session). The agent will be available immediately.

## Usage

Once installed, Claude will use the Nevron brand agent when you ask for brand-related work. Examples:

**Web design:**
> "Design a hero section for the Nevron website"

**Presentations:**
> "Create a slide layout for a client pitch deck"

**Documents:**
> "Format a proposal document for Hotel Kempinski"

**Brand review:**
> "Review this design for brand consistency"

**Slovenian:**
> "Oblikuj kartico za NevronCore funkcijo"

The agent responds in the user's language (English or Slovenian).

## CSS Tokens

Drop `tokens/nevron-tokens.css` into any web project for instant access to all brand values:

```html
<link rel="stylesheet" href="path/to/nevron-tokens.css">
```

Then use the custom properties:

```css
.my-button {
  background-color: var(--nevron-color-primary);
  color: var(--nevron-color-white);
  font-family: var(--nevron-font-family);
  padding: var(--nevron-space-3) var(--nevron-space-6);
  border-radius: var(--nevron-radius-md);
  transition: background-color var(--nevron-transition-base);
}
```

## Logo Assets

Six SVG logo variants included in `assets/logos/`:

| File | Variant | Use for |
|------|---------|---------|
| `nevron-logo-icon.svg` | Monogram (blue) | Favicons, small avatars |
| `nevron-logo-icon-white.svg` | Monogram (white) | Dark backgrounds |
| `nevron-logo-no-tagline-blue.svg` | Logo (blue) | Headers, navigation |
| `nevron-logo-no-tagline-white.svg` | Logo (white) | Dark headers |
| `nevron-logo-tagline-blue.svg` | Full logo (blue) | Hero sections, covers |
| `nevron-logo-tagline-white.svg` | Full logo (white) | Dark hero sections |

## Brand Colors

| Token | Hex | Role |
|-------|-----|------|
| M1 | `#000126` | Navy (dark backgrounds) |
| M2 | `#00317A` | Dark Blue |
| M3 | `#0067B2` | Brand Blue (primary) |
| M4 | `#009CDE` | Medium Blue |
| M5 | `#7BCAED` | Light Blue |
| M6 | `#E1F4FF` | Pale Blue |
| S1-S6 | Gray scale | Text and UI |
| Red | `#DA2025` | Errors |
| Orange | `#E56600` | Warnings |
| Yellow | `#F6A900` | Caution |
| Green | `#36A058` | Success |

## Updating

Pull the latest version and re-copy the agent:

```bash
git pull
cp agent/nevron-brand.md ~/.claude/agents/
```

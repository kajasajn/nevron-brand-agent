# Nevron Brand Agent

A standalone Claude Code agent that enforces Nevron brand consistency across all output formats — web, presentations, documents, and print.

Works in both the **Claude Code CLI** (terminal) and the **Claude Code desktop app**.

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

### 1. Open your terminal

**Windows:** Open Git Bash, Command Prompt, or Terminal
**macOS/Linux:** Open Terminal

You can also use the built-in terminal in the **Claude Code desktop app**.

### 2. Clone the repo to your home folder

```bash
cd ~
git clone https://github.com/kajasajn/nevron-brand-agent.git
```

This creates a `nevron-brand-agent` folder in your home directory (e.g. `C:\Users\YourName\nevron-brand-agent` on Windows, `~/nevron-brand-agent` on Mac/Linux).

### 3. Create the agents folder (if it doesn't exist)

```bash
mkdir -p ~/.claude/agents
```

### 4. Copy the agent file

```bash
cp ~/nevron-brand-agent/agent/nevron-brand.md ~/.claude/agents/
```

### 5. Restart Claude Code

Close and reopen Claude Code (or start a new session). The agent will be available immediately.

### Verify it worked

In Claude Code, the agent should appear when you ask for brand-related tasks. Try asking:

> "Design a button using Nevron brand colors. Deploy the nevron-brand agent."

## Auto-Trigger Setup (Recommended)

By default, Claude Code won't automatically call the brand agent — you have to explicitly ask for it each time. To make it **automatic**, paste this prompt into Claude Code and it will configure everything for you:

### Paste this into Claude Code:

> Add the nevron-brand agent to my CLAUDE.md so it auto-triggers for any Nevron brand tasks. Add it to the agents table (or create one if it doesn't exist) with this row:
>
> | **nevron-brand** | Nevron brand colors, typography, logo usage, spacing, brand guidelines, any Nevron-branded design decisions | User asks about Nevron brand, or is building/reviewing anything Nevron-branded |
>
> Also add this to the agent decision flow (or create one): "Nevron brand question / building Nevron UI? → nevron-brand"
>
> Do this for both my global ~/.claude/CLAUDE.md and my project CLAUDE.md if one exists.

That's it. Claude will edit your config files and the brand agent will auto-trigger from now on.

### What this does

With auto-trigger set up, Claude Code will automatically:
- Call the brand agent when you ask about Nevron colors, fonts, or guidelines
- Call the brand agent before building any Nevron-branded component
- Call the brand agent when reviewing designs for brand consistency
- Use correct brand tokens, logo variants, and typography without you having to specify them

---

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
| M2 | `#002391` | Dark Blue |
| M3 | `#1B92FF` | Brand Blue (primary) |
| M4 | `#73C7FF` | Medium Blue |
| M5 | `#C3E9FF` | Light Blue |
| M6 | `#E1F4FF` | Pale Blue |
| S1-S6 | Gray scale | Text and UI |
| Red | `#DA2025` | Errors |
| Orange | `#E56600` | Warnings |
| Yellow | `#F6A900` | Caution |
| Green | `#36A058` | Success |

## Updating

Navigate to the repo folder, pull the latest version, and re-copy the agent:

```bash
cd ~/nevron-brand-agent
git pull
cp agent/nevron-brand.md ~/.claude/agents/
```

Then restart Claude Code to pick up the changes.

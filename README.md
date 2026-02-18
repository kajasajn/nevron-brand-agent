
```
 ███╗   ██╗███████╗██╗   ██╗██████╗  ██████╗ ███╗   ██╗
 ████╗  ██║██╔════╝██║   ██║██╔══██╗██╔═══██╗████╗  ██║
 ██╔██╗ ██║█████╗  ██║   ██║██████╔╝██║   ██║██╔██╗ ██║
 ██║╚██╗██║██╔══╝  ╚██╗ ██╔╝██╔══██╗██║   ██║██║╚██╗██║
 ██║ ╚████║███████╗ ╚████╔╝ ██║  ██║╚██████╔╝██║ ╚████║
 ╚═╝  ╚═══╝╚══════╝  ╚═══╝  ╚═╝  ╚═╝ ╚═════╝ ╚═╝  ╚═══╝
 B R A N D   A G E N T
```

A standalone **Claude Code agent** that enforces Nevron brand consistency across all output formats — web, presentations, documents, and print.

Works in both the **Claude Code CLI** (terminal) and the **Claude Code desktop app**.

---

```
 ╔══════════════════════════════════════╗
 ║  📦  WHAT'S INCLUDED                ║
 ╚══════════════════════════════════════╝
```

```
nevron-brand-agent/
├── agent/
│   └── nevron-brand.md          # The agent (install this)
├── assets/
│   ├── logos/                   # SVG logos (monogram, with/without tagline)
│   ├── icons/                   # Custom Nevron SVG icons
│   ├── illustrations/           # Brand illustrations
│   ├── product-images/          # Hardware product photos
│   ├── screenshots/             # NevronCore app screenshots
│   └── fonts/
│       └── README.md            # Font licensing info
├── tokens/
│   └── nevron-tokens.css        # CSS custom properties (all brand tokens)
└── examples/
    ├── web-component.html       # Branded feature card demo
    ├── presentation-guide.md    # PowerPoint/Keynote slide templates
    └── document-guide.md        # PDF/Word document formatting
```

---

```
 ╔══════════════════════════════════════╗
 ║  ⚡  QUICK START                     ║
 ╚══════════════════════════════════════╝
```

### 1. Clone the repo

```bash
cd ~
git clone https://github.com/kajasajn/nevron-brand-agent.git
```

### 2. Create the agents folder

```bash
mkdir -p ~/.claude/agents
```

### 3. Copy the agent file

```bash
cp ~/nevron-brand-agent/agent/nevron-brand.md ~/.claude/agents/
```

### 4. Restart Claude Code

Close and reopen Claude Code (or start a new session). Done.

### 5. Verify

Try asking:

> "Design a button using Nevron brand colors. Deploy the nevron-brand agent."

---

```
 ╔══════════════════════════════════════╗
 ║  🔁  AUTO-TRIGGER SETUP             ║
 ╚══════════════════════════════════════╝
```

By default, you have to explicitly ask Claude to use the brand agent each time. To make it **automatic**, paste this prompt into Claude Code:

```
Add the nevron-brand agent to my CLAUDE.md so it auto-triggers for any Nevron brand tasks. Add it to the agents table (or create one if it doesn't exist) with this row:

| **nevron-brand** | Nevron brand colors, typography, logo usage, spacing, brand guidelines, any Nevron-branded design decisions | User asks about Nevron brand, or is building/reviewing anything Nevron-branded |

Also add this to the agent decision flow (or create one): "Nevron brand question / building Nevron UI? → nevron-brand"

Do this for both my global ~/.claude/CLAUDE.md and my project CLAUDE.md if one exists.
```

That's it. Claude handles the config. The brand agent will auto-trigger from now on.

**What changes:**
- Ask about Nevron colors/fonts/guidelines → brand agent called automatically
- Build any Nevron-branded component → brand agent called first
- Review a design for brand consistency → brand agent consulted
- Correct tokens, logos, and typography used without you specifying them

---

```
 ╔══════════════════════════════════════╗
 ║  💬  USAGE EXAMPLES                 ║
 ╚══════════════════════════════════════╝
```

**Web design**
> "Design a hero section for the Nevron website"

**Presentations**
> "Create a slide layout for a client pitch deck"

**Documents**
> "Format a proposal document for Hotel Kempinski"

**Brand review**
> "Review this design for brand consistency"

**Slovenian**
> "Oblikuj kartico za NevronCore funkcijo"

The agent responds in the user's language (English or Slovenian).

---

```
 ╔══════════════════════════════════════╗
 ║  🎨  BRAND COLORS                   ║
 ╚══════════════════════════════════════╝
```

### Primary Blues

```
 M1  ██████  #000126   Navy — dark backgrounds, text on light
 M2  ██████  #002391   Dark Blue — secondary dark, accents
 M3  ██████  #1B92FF   Brand Blue — primary CTAs, links ★
 M4  ██████  #73C7FF   Medium Blue — interactive states
 M5  ██████  #C3E9FF   Light Blue — backgrounds, decorative
 M6  ██████  #E1F4FF   Pale Blue — light backgrounds, cards
```

### Secondary Grays

```
 S1  ██████  #080C13   Near Black — body text
 S2  ██████  #353941   Dark Gray — secondary text
 S3  ██████  #707379   Medium Gray — tertiary text, borders
 S4  ██████  #B4B6B9   Gray — disabled, placeholders
 S5  ██████  #E0E1E2   Light Gray — borders, dividers
 S6  ██████  #EFF0F0   Off White — subtle backgrounds
```

### Supporting (functional only — never decorative)

```
 🔴  ██████  #DA2025   Red — errors, destructive actions
 🟠  ██████  #E56600   Orange — warnings, attention
 🟡  ██████  #F6A900   Yellow — caution, highlights
 🟢  ██████  #36A058   Green — success, confirmation
```

---

```
 ╔══════════════════════════════════════╗
 ║  🏷️  LOGO ASSETS                    ║
 ╚══════════════════════════════════════╝
```

Six SVG variants in `assets/logos/`:

```
 LIGHT BACKGROUNDS                      DARK BACKGROUNDS
 ─────────────────                      ────────────────
 nevron-logo-icon.svg          ←→       nevron-logo-icon-white.svg
 (monogram, blue)                       (monogram, white)

 nevron-logo-no-tagline-blue.svg  ←→   nevron-logo-no-tagline-white.svg
 (headers, navigation)                  (dark headers)

 nevron-logo-tagline-blue.svg     ←→   nevron-logo-tagline-white.svg
 (hero sections, covers)               (dark hero sections)
```

**Quick pick:**
```
 Small space (< 80px)?        → Monogram/Icon
 First impression (hero)?     → With tagline
 Navigation / repeated?       → Without tagline
 Dark background?             → White variant
 Light background?            → Blue variant
```

---

```
 ╔══════════════════════════════════════╗
 ║  🔤  CSS TOKENS                     ║
 ╚══════════════════════════════════════╝
```

Drop `tokens/nevron-tokens.css` into any web project:

```html
<link rel="stylesheet" href="path/to/nevron-tokens.css">
```

Then use custom properties:

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

---

```
 ╔══════════════════════════════════════╗
 ║  🔄  UPDATING                       ║
 ╚══════════════════════════════════════╝
```

```bash
cd ~/nevron-brand-agent
git pull
cp agent/nevron-brand.md ~/.claude/agents/
```

Then restart Claude Code to pick up the changes.

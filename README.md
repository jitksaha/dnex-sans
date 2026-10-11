# Dynex Sans

<p align="center">
  <strong>The Official Dynime Typeface</strong><br>
  <em>One Brand. One Typeface. One Identity.</em>
</p>

<p align="center">
  <a href="#weights--styles">Weights</a> •
  <a href="#quick-installation">Installation</a> •
  <a href="#web--framework-integration">Integration</a> •
  <a href="#license">License</a>
</p>

---

## Overview

**Dynex Sans** is a proprietary-engineered neo-grotesque geometric typeface crafted to express the **Dynime** brand identity across products, platforms, and digital experiences worldwide. 

Engineered with calibrated legibility, sharp optical balance, and modern proportions, Dynex Sans delivers an authoritative aesthetic from high-impact display headlines to dense user interface data.

---

## Weights & Styles

The Dynex Sans core family includes 6 production weights and italics:

| File | Weight / Style | CSS `font-weight` | Ideal Usage |
| :--- | :--- | :--- | :--- |
| **`DynexSans-Light.otf`** | Light | `300` | Subtitles, delicate captions, secondary metadata |
| **`DynexSans-LightItalic.otf`** | Light Italic | `300` | Accents, soft emphasis, quotes |
| **`DynexSans-Regular.otf`** | Regular | `400` | Core UI copy, paragraphs, form fields, tables |
| **`DynexSans-Italic.otf`** | Regular Italic | `400` | In-body emphasis, placeholders |
| **`DynexSans-Bold.otf`** | Bold | `700` | Primary headlines (H1–H3), CTAs, buttons, badges |
| **`DynexSans-BoldItalic.otf`** | Bold Italic | `700` | High-energy marketing callouts |

---

## Quick Installation

### Desktop (Figma, Adobe, macOS, Windows)

1. Clone or download this repository:
   ```bash
   git clone https://github.com/jitksaha/dnex-sans.git
   ```
2. Select all `.otf` files:
   - **macOS:** Double-click and click **Install Font** in Font Book.
   - **Windows:** Right-click and choose **Install for all users**.
3. In Figma, Photoshop, Illustrator, or Sketch, search for:  
   `Dynex Sans`

---

## Web & Framework Integration

Dynex Sans supports all modern web and mobile frameworks. For exhaustive configuration code across **Next.js, Tailwind CSS (v3 & v4), React, Vue, Svelte, Flutter, React Native, iOS (SwiftUI), Android (Jetpack Compose), and Python**, see:

👉 **[INTEGRATION.md](./INTEGRATION.md)**

### CSS Quickstart

```css
@font-face {
  font-family: 'Dynex Sans';
  src: url('./DynexSans-Regular.otf') format('opentype');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Dynex Sans';
  src: url('./DynexSans-Bold.otf') format('opentype');
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

body {
  font-family: 'Dynex Sans', -apple-system, BlinkMacSystemFont, sans-serif;
}
```

### Tailwind CSS

```javascript
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      fontFamily: {
        dynex: ['"Dynex Sans"', 'sans-serif'],
      },
    },
  },
}
```

---

## Contributing

We welcome contributions, bug reports, and suggestions. Please check out:
- [CONTRIBUTING.md](./CONTRIBUTING.md)
- [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md)

---

## License

Dynex Sans is distributed under the [SIL Open Font License 1.1](./LICENSE).  
Copyright (c) 2026 Dynime. All Rights Reserved.

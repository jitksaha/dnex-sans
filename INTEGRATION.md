# Dynex Sans — Universal Integration Presets
> **The Official Dynime Typeface**  
> *"One Brand. One Typeface. One Identity."*

This guide provides copy-paste ready font configuration and calling presets for every major web, mobile, desktop, and backend framework worldwide.

---

## Table of Contents
1. [Font Overview & Weights](#1-font-overview--weights)
2. [Vanilla Web (HTML & CSS / SCSS)](#2-vanilla-web-html--css--scss)
3. [Tailwind CSS (v3 & v4)](#3-tailwind-css-v3--v4)
4. [Next.js (App Router & Pages Router)](#4-nextjs-app-router--pages-router)
5. [React (Vite / Create React App)](#5-react-vite--create-react-app)
6. [Vue 3 & Nuxt 3](#6-vue-3--nuxt-3)
7. [Svelte & SvelteKit](#7-svelte--sveltekit)
8. [Astro](#8-astro)
9. [Angular](#9-angular)
10. [React Native (iOS & Android)](#10-react-native-ios--android)
11. [Flutter (Dart)](#11-flutter-dart)
12. [iOS (Swift & SwiftUI)](#12-ios-swift--swiftui)
13. [Android (Kotlin & Jetpack Compose)](#13-android-kotlin--jetpack-compose)
14. [Python (Pillow, Matplotlib, ReportLab)](#14-python-pillow-matplotlib-reportlab)
15. [Desktop Design (Figma, Adobe, Canva, Sketch)](#15-desktop-design-figma-adobe-canva-sketch)

---

## 1. Font Overview & Weights

| File Name | Style | PostScript Name | CSS `font-weight` |
| :--- | :--- | :--- | :--- |
| `DynexSans-Light.otf` | Light | `DynexSans-Light` | `300` (also covers 100–300) |
| `DynexSans-LightItalic.otf` | Light Italic | `DynexSans-LightItalic` | `300` (italic) |
| `DynexSans-Regular.otf` | Regular | `DynexSans-Regular` | `400` (also covers 400–500) |
| `DynexSans-Italic.otf` | Italic | `DynexSans-Italic` | `400` (italic) |
| `DynexSans-Bold.otf` | Bold | `DynexSans-Bold` | `700` (also covers 600–900) |
| `DynexSans-BoldItalic.otf` | Bold Italic | `DynexSans-BoldItalic` | `700` (italic) |

- **Official Family Name:** `Dynex Sans`

---

## 2. Vanilla Web (HTML & CSS / SCSS)

Place the font files in your `fonts/` directory:

```css
/* ==========================================================================
   Dynex Sans Web Integration
   ========================================================================== */

/* Light (300) */
@font-face {
  font-family: 'Dynex Sans';
  src: url('./fonts/DynexSans-Light.otf') format('opentype');
  font-weight: 300;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Dynex Sans';
  src: url('./fonts/DynexSans-LightItalic.otf') format('opentype');
  font-weight: 300;
  font-style: italic;
  font-display: swap;
}

/* Regular (400) */
@font-face {
  font-family: 'Dynex Sans';
  src: url('./fonts/DynexSans-Regular.otf') format('opentype');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Dynex Sans';
  src: url('./fonts/DynexSans-Italic.otf') format('opentype');
  font-weight: 400;
  font-style: italic;
  font-display: swap;
}

/* Bold (700) */
@font-face {
  font-family: 'Dynex Sans';
  src: url('./fonts/DynexSans-Bold.otf') format('opentype');
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Dynex Sans';
  src: url('./fonts/DynexSans-BoldItalic.otf') format('opentype');
  font-weight: 700;
  font-style: italic;
  font-display: swap;
}

/* Usage */
:root {
  --font-family-primary: 'Dynex Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}

body {
  font-family: var(--font-family-primary);
  font-weight: 400;
}
```

---

## 3. Tailwind CSS (v3 & v4)

### Tailwind CSS v3
In `tailwind.config.js`:
```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ['./src/**/*.{js,ts,jsx,tsx}'],
  theme: {
    extend: {
      fontFamily: {
        dynex: ['"Dynex Sans"', 'sans-serif'],
        sans: ['"Dynex Sans"', 'sans-serif'], // Sets Dynex Sans as default sans font
      },
    },
  },
  plugins: [],
}
```

### Tailwind CSS v4 (CSS Theme Variables)
In `app.css` / `globals.css`:
```css
@import "tailwindcss";

@theme {
  --font-dynex: "Dynex Sans", sans-serif;
  --font-sans: "Dynex Sans", sans-serif;
}
```

**Usage in HTML / JSX:**
```html
<h1 class="font-dynex font-bold text-4xl">Dynime Header</h1>
<p class="font-dynex font-light text-gray-400">Subtext in Dynex Light</p>
```

---

## 4. Next.js (App Router & Pages Router)

### Next.js 13+ / 14+ / 15+ (App Router)
Save fonts to `public/fonts/`. In `app/layout.tsx`:

```tsx
import localFont from 'next/font/local';
import './globals.css';

export const dynexSans = localFont({
  src: [
    {
      path: '../public/fonts/DynexSans-Light.otf',
      weight: '300',
      style: 'normal',
    },
    {
      path: '../public/fonts/DynexSans-LightItalic.otf',
      weight: '300',
      style: 'italic',
    },
    {
      path: '../public/fonts/DynexSans-Regular.otf',
      weight: '400',
      style: 'normal',
    },
    {
      path: '../public/fonts/DynexSans-Italic.otf',
      weight: '400',
      style: 'italic',
    },
    {
      path: '../public/fonts/DynexSans-Bold.otf',
      weight: '700',
      style: 'normal',
    },
    {
      path: '../public/fonts/DynexSans-BoldItalic.otf',
      weight: '700',
      style: 'italic',
    },
  ],
  variable: '--font-dynex',
  display: 'swap',
});

export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="en" className={dynexSans.variable}>
      <body className="font-dynex antialiased">{children}</body>
    </html>
  );
}
```

---

## 5. React (Vite / Create React App)

In `src/index.css`:
```css
@import './fonts.css'; /* Contains the @font-face rules from Section 2 */

body {
  font-family: 'Dynex Sans', sans-serif;
}
```

In `src/App.tsx`:
```tsx
import React from 'react';

export const App = () => {
  return (
    <div style={{ fontFamily: 'Dynex Sans, sans-serif' }}>
      <h1>Dynex Sans Identity</h1>
    </div>
  );
};
```

---

## 6. Vue 3 & Nuxt 3

### Nuxt 3 (`nuxt.config.ts`)
```typescript
export default defineNuxtConfig({
  css: ['~/assets/css/fonts.css'],
})
```

### Vue 3 Single File Component (`App.vue`)
```vue
<template>
  <main class="brand-container">
    <h1>Dynime Platform</h1>
  </main>
</template>

<style scoped>
.brand-container {
  font-family: 'Dynex Sans', sans-serif;
}
</style>
```

---

## 7. Svelte & SvelteKit

In `src/routes/+layout.svelte`:
```svelte
<script>
  import '../app.css';
</script>

<slot />

<style>
  :global(body) {
    font-family: 'Dynex Sans', sans-serif;
  }
</style>
```

---

## 8. Astro

In `src/layouts/Layout.astro`:
```astro
---
import '../styles/fonts.css';
---

<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Dynime</title>
  </head>
  <body class="font-dynex">
    <slot />
  </body>
</html>
```

---

## 9. Angular

In `angular.json`:
```json
"assets": [
  "src/favicon.ico",
  "src/assets",
  {
    "glob": "**/*",
    "input": "src/assets/fonts",
    "output": "/assets/fonts"
  }
],
"styles": [
  "src/styles.scss"
]
```

In `src/styles.scss`:
```scss
@font-face {
  font-family: 'Dynex Sans';
  src: url('/assets/fonts/DynexSans-Regular.otf') format('opentype');
  font-weight: 400;
}

body {
  font-family: 'Dynex Sans', sans-serif;
}
```

---

## 10. React Native (iOS & Android)

1. Put the fonts into `assets/fonts/`.
2. Configure `react-native.config.js`:
```javascript
module.exports = {
  project: {
    ios: {},
    android: {},
  },
  assets: ['./assets/fonts/'],
};
```
3. Run `npx react-native-asset` to link them.
4. Usage in components:
```typescript
import { StyleSheet, Text, View } from 'react-native';

export const Header = () => (
  <View>
    <Text style={styles.title}>Dynex Sans Mobile</Text>
  </View>
);

const styles = StyleSheet.create({
  title: {
    fontFamily: 'DynexSans-Bold', // Use PostScript name on Android & iOS
    fontSize: 24,
  },
});
```

---

## 11. Flutter (Dart)

1. Copy fonts to `fonts/` in your Flutter project root.
2. In `pubspec.yaml`:
```yaml
flutter:
  fonts:
    - family: Dynex Sans
      fonts:
        - asset: fonts/DynexSans-Light.otf
          weight: 300
        - asset: fonts/DynexSans-LightItalic.otf
          weight: 300
          style: italic
        - asset: fonts/DynexSans-Regular.otf
          weight: 400
        - asset: fonts/DynexSans-Italic.otf
          weight: 400
          style: italic
        - asset: fonts/DynexSans-Bold.otf
          weight: 700
        - asset: fonts/DynexSans-BoldItalic.otf
          weight: 700
          style: italic
```
3. Usage in Dart:
```dart
Text(
  'Dynime Experience',
  style: TextStyle(
    fontFamily: 'Dynex Sans',
    fontWeight: FontWeight.w700,
    fontSize: 28,
  ),
);
```

---

## 12. iOS (Swift & SwiftUI)

1. Add `DynexSans-*.otf` files to your Xcode project under "Copy Bundle Resources".
2. In `Info.plist`, add key `Fonts provided by application`:
   - `DynexSans-Light.otf`
   - `DynexSans-Regular.otf`
   - `DynexSans-Bold.otf`
3. Usage in SwiftUI:
```swift
import SwiftUI

struct ContentView: View {
    var body: some View {
        Text("Dynex Sans in SwiftUI")
            .font(.custom("DynexSans-Bold", size: 24))
    }
}
```

---

## 13. Android (Kotlin & Jetpack Compose)

1. Put `.otf` files in `res/font/` (lowercase naming, e.g. `dynex_sans_regular.otf`).
2. In Jetpack Compose `Type.kt`:
```kotlin
val DynexSans = FontFamily(
    Font(R.font.dynex_sans_light, FontWeight.Light),
    Font(R.font.dynex_sans_regular, FontWeight.Normal),
    Font(R.font.dynex_sans_bold, FontWeight.Bold)
)

val Typography = Typography(
    bodyLarge = TextStyle(
        fontFamily = DynexSans,
        fontWeight = FontWeight.Normal,
        fontSize = 16.sp
    )
)
```

---

## 14. Python (Pillow, Matplotlib, ReportLab)

### Image Generation (Pillow)
```python
from PIL import Image, ImageDraw, ImageFont

font = ImageFont.truetype("DynexSans-Bold.otf", size=40)
img = Image.new("RGBA", (600, 200), (10, 12, 18, 255))
draw = ImageDraw.Draw(img)
draw.text((40, 75), "Dynime Identity", font=font, fill=(255, 255, 255))
img.save("dynex_specimen.png")
```

### Data Visualization (Matplotlib)
```python
import matplotlib.pyplot as plt
import matplotlib.font_manager as fm

font_prop = fm.FontProperties(fname="DynexSans-Regular.otf")
plt.figure(figsize=(8, 4))
plt.title("Dynex Typography Chart", fontproperties=fm.FontProperties(fname="DynexSans-Bold.otf", size=16))
plt.xlabel("X Axis", fontproperties=font_prop)
plt.show()
```

---

## 15. Desktop Design (Figma, Adobe, Canva, Sketch)

1. **Installation:**
   - **macOS:** Select all 6 `.otf` files, double-click, and click **Install**.
   - **Windows:** Right-click the `.otf` files and choose **Install for all users**.
2. **In Design Apps:**
   - In Figma, Adobe Illustrator, Photoshop, or Sketch, search for:  
     `Dynex Sans`
   - All weights (`Light`, `Regular`, `Bold` + `Italics`) will automatically appear grouped under this single family dropdown.

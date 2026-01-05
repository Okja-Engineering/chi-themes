# @okja/chi-themes

Ready-to-use CSS themes for applications. Import one file and get a complete, accessible design system.

## Installation

```bash
npm install @okja/chi-themes
```

## Quick Start

```css
@import '@okja/chi-themes/default.css';
```

Or in HTML:

```html
<link rel="stylesheet" href="node_modules/@okja/chi-themes/dist/default.css">
```

That's it. You get a CSS reset, design tokens, typography, and base styles.

## Available Themes

| Theme | Use Case |
|-------|----------|
| `default.css` | Grayscale - wireframing, prototyping |
| `blue.css` | Corporate blue - healthcare, enterprise |
| `purple.css` | Creative purple - consumer apps |
| `reset.css` | Reset only - bring your own styles |

## Using Tokens

All themes include design tokens you can use in your components:

```css
.card {
  background: var(--color-surface-container);
  padding: var(--space-4);
  border-radius: var(--radius-md);
  box-shadow: var(--shadow-2);
}

.button {
  background: var(--color-primary);
  color: var(--color-on-primary);
  padding: var(--space-2) var(--space-4);
  border-radius: var(--radius-sm);
  transition: opacity var(--duration-short2) var(--easing-standard);
}
```

## What's Included

### Base Styles
- **Typography** - Body text, responsive sizing
- **Headings** - h1-h6 with proper hierarchy
- **Links** - Primary color with focus states
- **Code** - Monospace font, subtle background
- **Lists** - Proper list styling restored
- **Focus states** - Accessible focus rings

### Utility Classes

```html
<div class="elevation-1">Subtle shadow</div>
<div class="elevation-3">Medium shadow</div>
<div class="elevation-5">Strong shadow</div>
```

## Dark Mode

Dark mode works automatically via `prefers-color-scheme`. All colors adapt with no extra configuration.

## Customization

### Scaling

```html
<body data-scaling="110">
```

Options: `90`, `95`, `100` (default), `105`, `110`

### Border Radius

```html
<body data-radius="large">
```

Options: `none`, `small`, `medium` (default), `large`

## Architecture

Each theme uses CSS Cascade Layers:

```css
@layer reset, tokens, base;
```

- **reset** - Normalize browser defaults
- **tokens** - Design tokens (colors, spacing, etc.)
- **base** - Typography, links, headings

Your application styles layer on top, giving you full cascade control.

## License

MIT

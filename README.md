# @okja/chi-themes

Pre-composed CSS themes built on Chi Design System tokens. Import one file and get reset, tokens, and base styles.

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

## Available Themes

| Theme | Description |
|-------|-------------|
| `default.css` | Grayscale - wireframing, prototyping |
| `blue.css` | Corporate blue - healthcare, enterprise |
| `purple.css` | Creative purple - consumer apps |
| `reset.css` | Reset only - bring your own tokens |

## Using Tokens

All themes include design tokens:

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
  font-family: var(--font-sans);
  padding: var(--space-2) var(--space-4);
  border-radius: var(--radius-sm);
  transition: opacity var(--duration-short2) var(--easing-standard);
}
```

### Available Tokens

**Colors** (auto light/dark via `prefers-color-scheme`)
- `--color-primary`, `--color-on-primary`
- `--color-secondary`, `--color-on-secondary`
- `--color-tertiary`, `--color-on-tertiary`
- `--color-error`, `--color-on-error`
- `--color-surface`, `--color-on-surface`
- `--color-surface-container`, `--color-surface-container-high`
- `--color-background`, `--color-outline`

**Spacing** (9-step scale)
- `--space-1` (4px) through `--space-9` (64px)

**Typography**
- `--font-sans`, `--font-serif`, `--font-mono`
- `--font-size-1` (12px) through `--font-size-9` (60px)
- `--font-weight-light`, `--font-weight-regular`, `--font-weight-medium`, `--font-weight-bold`
- `--line-height-1` through `--line-height-9`

**Border Radius**
- `--radius-none`, `--radius-xs`, `--radius-sm`, `--radius-md`, `--radius-lg`, `--radius-xl`, `--radius-full`

**Shadows**
- `--shadow-0` (none) through `--shadow-5`

**Motion**
- `--duration-short1` (50ms) through `--duration-extra-long4` (1000ms)
- `--easing-standard`, `--easing-emphasized`, `--easing-linear`

## Dark Mode

Colors adapt automatically via `prefers-color-scheme`. No configuration needed.

## Customization

### Scaling

```html
<html data-scaling="110%">
```

Options: `90%`, `95%`, `100%` (default), `105%`, `110%`

### Border Radius

```html
<html data-radius="large">
```

Options: `none`, `small`, `medium` (default), `large`

## Architecture

Each theme uses CSS Cascade Layers:

```css
@layer reset, tokens, base;
```

- **reset** - Normalize browser defaults
- **tokens** - Design tokens from @okja/chi-tokens
- **base** - Typography, links, focus states

Your styles layer on top, giving you full cascade control.

## License

MIT

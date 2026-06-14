---
name: StackLens Canary IconFix 6
colors:
  surface: '#0b1326'
  surface-dim: '#0b1326'
  surface-bright: '#31394d'
  surface-container-lowest: '#060e20'
  surface-container-low: '#131b2e'
  surface-container: '#171f33'
  surface-container-high: '#222a3d'
  surface-container-highest: '#2d3449'
  on-surface: '#dae2fd'
  on-surface-variant: '#bdc8d1'
  inverse-surface: '#dae2fd'
  inverse-on-surface: '#283044'
  outline: '#87929a'
  outline-variant: '#3e484f'
  surface-tint: '#7bd0ff'
  primary: '#8ed5ff'
  on-primary: '#00354a'
  primary-container: '#38bdf8'
  on-primary-container: '#004965'
  inverse-primary: '#00668a'
  secondary: '#b9c8de'
  on-secondary: '#233143'
  secondary-container: '#39485a'
  on-secondary-container: '#a7b6cc'
  tertiary: '#ffc176'
  on-tertiary: '#472a00'
  tertiary-container: '#f1a02b'
  on-tertiary-container: '#613b00'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#c4e7ff'
  primary-fixed-dim: '#7bd0ff'
  on-primary-fixed: '#001e2c'
  on-primary-fixed-variant: '#004c69'
  secondary-fixed: '#d4e4fa'
  secondary-fixed-dim: '#b9c8de'
  on-secondary-fixed: '#0d1c2d'
  on-secondary-fixed-variant: '#39485a'
  tertiary-fixed: '#ffddb8'
  tertiary-fixed-dim: '#ffb960'
  on-tertiary-fixed: '#2a1700'
  on-tertiary-fixed-variant: '#653e00'
  background: '#0b1326'
  on-background: '#dae2fd'
  surface-variant: '#2d3449'
typography:
  display-sm:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.02em
  headline-sm:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
    letterSpacing: -0.01em
  body-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
    letterSpacing: 0em
  body-sm:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '400'
    lineHeight: 18px
    letterSpacing: 0em
  label-md:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.02em
  data-mono:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
    letterSpacing: 0em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  unit: 4px
  container-padding: 16px
  gutter: 12px
  stack-compact: 4px
  stack-default: 8px
  section-gap: 24px
---

## Brand & Style
The design system is engineered for high-density operational environments where data clarity and system reliability are paramount. The brand personality is **Deterministic, Reliable, and Data-Centric**, prioritizing functional utility over aesthetic flair. 

The visual style follows a **Modern Corporate** approach with a "Dense but Calm" execution. It utilizes a restrained palette and systematic grid to ensure that even with high information density, the user feels in control. Every pixel is dedicated to surfacing system health and operational metrics, eliminating "marketing fluff" in favor of precision.

## Colors
This design system utilizes a **Dark Mode** default to reduce eye strain during prolonged monitoring sessions. The palette is anchored in Deep Navy and Slate to create a stable, professional backdrop.

- **Primary**: A precise sky blue used sparingly for active states and primary actions.
- **Neutrals**: A range of slates (`#94A3B8`) and navies (`#0F172A`) to define hierarchy and surface elevation.
- **Semantic Palette**: Strict adherence to status colors:
    - **Emerald**: System healthy / Operational.
    - **Amber**: Warnings / Latency thresholds.
    - **Crimson**: Critical errors / Risk events.
- **Contrast**: High contrast is maintained for text readability, while UI chrome (borders, backgrounds) maintains low contrast to keep the focus on the data.

## Typography
The typography system uses **Inter** for all UI elements to ensure maximum legibility at small sizes. **JetBrains Mono** is introduced specifically for tabular data, timestamps, and log entries to ensure character alignment and rapid scanning of numerical values.

- **Hierarchy**: Use `label-md` in all-caps for section headers to distinguish them from interactive content.
- **Density**: Line heights are kept tight (1.2x to 1.4x) to support the high-density requirement without sacrificing readability.
- **Data focus**: Use the `data-mono` role for any system-generated output, IDs, or metrics.

## Layout & Spacing
The layout uses a **Fluid Grid** model optimized for wide-screen monitoring. A 12-column grid is standard, but the primary rhythm is dictated by a 4px base unit.

- **Density**: A "Compact" spacing model is applied. Gutters between data widgets are kept at 12px to maximize screen real estate.
- **Margins**: A consistent 16px padding is applied to the main viewport.
- **Alignment**: Hard-edge alignment is required. Elements should snap to the grid to maintain the "deterministic" feel. 
- **Reflow**: On smaller desktop widths, sidebars collapse to icon-only views, and data tables prioritize horizontal scrolling over column dropping to preserve data integrity.

## Elevation & Depth
Depth is communicated through **Tonal Layers** rather than shadows. This minimizes visual noise and keeps the interface "flat" and focused.

- **Level 0 (Canvas)**: Background (`#0F172A`).
- **Level 1 (Card/Widget)**: Surface (`#1E293B`) with a subtle 1px border (`#334155`).
- **Level 2 (Interaction/Popovers)**: Slightly lighter surface (`#334155`) with a very soft, low-opacity shadow (0px 4px 12px rgba(0,0,0,0.5)) to separate it from the grid.
- **Outlines**: Use 1px solid borders for all containers. Avoid gradients or blurs.

## Shapes
The shape language is **Soft (0.25rem)**. This provides just enough rounding to prevent the UI from feeling aggressive while maintaining a precise, engineered appearance.

- **Small Components**: Checkboxes, tags, and small buttons use a 4px radius.
- **Large Components**: Cards and dashboard widgets use an 8px (0.5rem) radius.
- **Pills**: Use only for status indicators (Canary healthy, etc.) to distinguish them from interactive buttons.

## Components
- **Buttons**: Use a solid fill for primary actions and a "ghost" style with a border for secondary actions. Padding should be 4px 12px for high density.
- **Status Chips**: Small, high-contrast badges using the semantic palette. Text should be uppercase `label-md`.
- **Data Tables**: Zero-border on sides, 1px horizontal dividers only. Row height should be fixed at 32px or 36px. Use `data-mono` for numeric columns.
- **Input Fields**: Dark backgrounds (`#0F172A`) with a subtle border. The active state is signaled by a primary-colored 1px border.
- **Cards/Widgets**: Every widget must have a header row with a `label-md` title and optional action icons (refresh, expand).
- **Checkboxes**: Square with a 2px radius. When checked, use the Primary Sky Blue fill.
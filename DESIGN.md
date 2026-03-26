# Design System Document

## 1. Overview & Creative North Star: "The Ethereal Sanctuary"

This design system is a digital translation of holistic energy work—a space defined by breath, light, and restoration. Moving away from the rigid, segmented layouts of traditional therapy websites, our Creative North Star is **"The Ethereal Sanctuary."** 

We achieve this through an editorial approach that favors intentional asymmetry, fluid layering, and expansive negative space. Instead of boxing content into restrictive grids, the UI acts as a canvas where elements float with a sense of purposeful weightlessness. By utilizing high-contrast typography scales (the authoritative Serif vs. the modern Sans-Serif) and overlapping imagery, we create a premium experience that feels both professional and deeply personal.

---

## 2. Colors & Atmospheric Depth

The palette is rooted in muted, earth-toned pinks and sophisticated grays, designed to lower the user's cognitive load and heart rate.

### Surface Hierarchy & The "No-Line" Rule
To maintain a high-end editorial feel, **1px solid borders for sectioning are strictly prohibited.** Structure must be defined through tonal shifts and background nesting:
- **Surface Layering:** A section utilizing `surface-container-low` (#f3f4f5) should sit atop a `surface` (#f8f9fa) background. 
- **Nesting:** Important content blocks (like booking modules) should use the `surface-container-lowest` (#ffffff) to appear naturally "raised" against a slightly darker background.

### Signature Textures & Glassmorphism
- **The Glass Effect:** For floating navigation bars or overlay modals, use a background of `surface_container` (#edeeef) at 70% opacity with a `24px` backdrop-blur. This softens the transition between the UI and the underlying imagery.
- **Soulful Gradients:** For Hero backgrounds and Primary CTAs, use a subtle linear gradient from `primary` (#795558) to `primary_container` (#e8b9bd). This adds a "glow" that flat colors cannot replicate, mimicking the flow of energy.

---

## 3. Typography: Editorial Authority

We use a high-contrast pairing to balance heritage with modernity.

- **The Serif (Noto Serif):** Used for all `display` and `headline` levels. It conveys wisdom, history, and the "human touch" of holistic work.
- **The Sans-Serif (Plus Jakarta Sans):** Used for `title`, `body`, and `label` levels. It provides a clean, modern clarity that ensures medical-grade readability.

**Scale Strategy:**
- **Display-LG (3.5rem):** Reserved for hero emotional statements. Use generous letter-spacing (-0.02em) to maintain a premium look.
- **Body-MD (0.875rem):** The workhorse for therapy descriptions. Increase line-height to 1.6 to ensure the text "breathes" on the page.

---

## 4. Elevation & Depth: Tonal Layering

Traditional shadows and borders create visual "clutter" that contradicts a sense of tranquility.

- **The Layering Principle:** Depth is achieved by stacking `surface-container` tiers. A `surface-container-highest` (#e1e3e4) element placed on a `surface-dim` (#d9dadb) background creates a tactile lift without a single line of code for shadows.
- **Ambient Shadows:** Where a shadow is necessary (e.g., a floating appointment card), use the **"Aura Shadow"**: 
  - `box-shadow: 0 12px 40px rgba(80, 68, 69, 0.06);` 
  - The shadow color is a 6% opacity version of the `on_surface_variant` to mimic natural light dispersion.
- **The "Ghost Border":** If accessibility requires a stroke, use `outline_variant` (#d4c2c3) at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons
- **Primary:** Filled with the `primary` (#795558) color. Use `Roundedness-xl` (0.75rem) for a soft, approachable feel. No sharp corners.
- **Tertiary (Ghost):** No background or border. Uses `primary` text with a subtle underline that expands on hover.

### Cards & Content Blocks
- **The "No-Divider" Rule:** Horizontal rules are forbidden. Use `Spacing-10` (3.5rem) or `Spacing-12` (4rem) to separate content themes.
- **Image Treatment:** Images should never be simple rectangles. Apply `Roundedness-xl` or use an asymmetrical "organic" mask to blend the photography into the white space.

### Input Fields
- **State:** Active inputs use a `primary_container` (#e8b9bd) background with a `primary` label. 
- **Style:** Underline-only inputs are preferred for a clean "journaling" feel, using a `Ghost Border` transition on focus.

### Additional Signature Components
- **Floating Navigation:** A glassmorphic bar that anchors to the top, allowing the website's soft colors to bleed through as the user scrolls.
- **The "Breathe" Loader:** A custom loading state using a pulsating `primary_container` circle to set the pace of the user's experience before content fades in.

---

## 6. Do’s and Don'ts

### Do:
- **Use Asymmetry:** Place a `headline-lg` on the left and a supporting image shifted slightly to the right to create an organic, non-templated flow.
- **Embrace Whitespace:** If a section feels "full," double the padding using `Spacing-20` (7rem).
- **Layer Text over Imagery:** Use `surface_container` with glassmorphism to place text partially over high-quality, soft-focus photography.

### Don’t:
- **Don’t use 100% Black:** Never use #000000. Use `on_surface` (#191c1d) for text to maintain a soft, professional contrast.
- **Don’t use Grid-heavy Boxes:** Avoid putting services in three equal boxes with borders. Instead, stagger them vertically with varying background tints.
- **Don't use Standard Shadows:** Avoid "drop shadows" that look like dark grey smudges. Stick to the "Aura Shadow" or tonal shifts.
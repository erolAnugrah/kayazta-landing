# Design System Strategy: The Elevated Editorial SaaS

## 1. Overview & Creative North Star
**Creative North Star: "The Modern Architect"**
This design system moves away from the "template-heavy" SaaS aesthetic toward a high-end, editorial experience. We achieve this through **The Modern Architect** philosophy: a focus on structural integrity, vast breathing room, and intentional asymmetry. 

Instead of boxed-in layouts, we use expansive white space and "floating" content blocks. The system rejects the rigidity of standard grids in favor of a dynamic, layered composition. We communicate "Trust" through precise typography and "Efficiency" through a lack of visual clutter. This is not just a tool; it is a premium workspace.

---

## 2. Colors & Tonal Depth
Our palette is rooted in the clarity of `surface_container_lowest` (#ffffff) and the depth of Indigo. We utilize tonal shifts rather than lines to define the architecture.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders for sectioning or containers. 
*   **The Alternative:** Boundaries must be defined solely through background shifts. For example, a `surface_container_low` (#f2f4f6) section should sit directly against a `surface` (#f7f9fb) background.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of fine paper. 
*   **Base:** `surface` (#f7f9fb)
*   **Sectioning:** `surface_container_low` (#f2f4f6) for large content areas.
*   **Focus Elements:** `surface_container_highest` (#e0e3e5) for sidebars or utility panels.
*   **Elevated Cards:** Always use `surface_container_lowest` (#ffffff) to "lift" the content off the tinted background.

### Signature Textures: Glass & Gradients
To inject "soul" into the efficiency, use:
*   **The Cyan-Indigo Drift:** Use a linear gradient (135°) from `primary` (#4648d4) to `secondary_container` (#57dffe) for primary CTAs and hero highlights.
*   **The Frosted Pane:** For floating navigation or modal overlays, use `surface_container_lowest` at 80% opacity with a `24px` backdrop blur.

---

## 3. Typography: Editorial Authority
We use **Inter** exclusively, but we treat it with editorial intent. The contrast between massive `display` scales and tight `label` scales creates an authoritative hierarchy.

*   **Display (lg/md):** Reserved for high-impact hero moments. Set with -0.02em letter spacing to feel "tight" and professional.
*   **Headline (sm/md):** Use `on_surface` (#191c1e). These should be the "anchors" of your page.
*   **Body (md):** Our workhorse. Ensure a line height of 1.6 to maintain the "Modern Architect" breathability.
*   **Label (sm):** All-caps with +0.05em tracking when used for category headers to provide a technical, "SaaS-native" feel.

---

## 4. Elevation & Depth: The Layering Principle
Hierarchy is achieved through **Tonal Layering**, not shadows.

*   **The Layering Principle:** Place a `surface_container_lowest` card on a `surface_container_low` background. The subtle contrast (pure white vs. light grey) provides a sophisticated, "silent" elevation.
*   **Ambient Shadows:** If an element must float (e.g., a dropdown), use a shadow: `0px 12px 32px rgba(25, 28, 30, 0.04)`. The shadow color is a tinted version of `on_surface`, never pure black.
*   **The "Ghost Border" Fallback:** If accessibility requires a border, use `outline_variant` (#c7c4d7) at 20% opacity. It should feel like a suggestion of a line, not a boundary.

---

## 5. Components

### Buttons
*   **Primary:** A gradient fill (Indigo to Cyan). 8px radius. White text. No border.
*   **Secondary:** `primary_fixed` (#e1e0ff) background with `on_primary_fixed` (#07006c) text.
*   **Tertiary:** Ghost style. No background. `primary` text.

### Cards & Lists
*   **The "No-Divider" Rule:** Forbid 1px dividers between list items. Instead, use 12px–16px of vertical whitespace or a hover state that utilizes `surface_container_high` (#e6e8ea).
*   **Card Styling:** 8px (`DEFAULT`) radius. Background: `surface_container_lowest`. No border.

### Input Fields
*   **State:** Background should be `surface_container_low`. On focus, transition background to `surface_container_lowest` and apply a 1px `primary` ghost border.
*   **Labels:** Use `label-md` in `on_surface_variant` (#464554) placed 8px above the field.

### Glass Tooltips
*   **Style:** `surface_container_highest` at 90% opacity with `blur(8px)`. This keeps the user grounded in the interface while providing necessary context.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical margins (e.g., 64px left, 128px right) for hero sections to create a custom, high-end feel.
*   **Do** leverage `primary_container` (#6063ee) for subtle background "glows" behind key data points.
*   **Do** prioritize the Spacing Scale (8px increments) to ensure the "Efficient" personality is felt in the rhythm of the page.

### Don't:
*   **Don't** use 100% black (#000000) for text. Always use `on_surface` (#191c1e) to maintain a soft, premium appearance.
*   **Don't** use standard "drop shadows" with high opacity. They break the "Modern Architect" cleanliness.
*   **Don't** cram content. If a section feels full, increase the `surface` padding. Space is a luxury; use it.
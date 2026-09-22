# Tegra Soluciones — Design System

> Una integradora y desarrolladora tecnológica mexicana.
> Prevenir cualquier evento para facilitar su resolución y buscar soluciones oportunas sin importar el grado de complejidad.

This repository codifies the visual identity, voice, and reusable UI of **Tegra Soluciones**: a Mexico City–based technology integrator founded in September 2013, specializing in engineering, electrical, communications and information security solutions for strategic installations across the public, private and governmental sectors.

The system is designed to look **formal but modern** — confident, restrained, technically competent. Surfaces are predominantly white; the brand red (`#AF282F`) is reserved for accents and load-bearing moments; the secondary gray (`#6F6F6F`) carries most of the structural work.

---

## Brand context

| | |
|---|---|
| **Company** | Tegra Soluciones |
| **Founded** | September 2013 |
| **Country** | México |
| **Sector** | Technology integration & development; physical/digital security |
| **Purpose** (Propósito) | _"Prevenir cualquier evento para facilitar su resolución y buscar soluciones oportunas sin importar el grado de complejidad."_ |
| **Audience** | Gubernamental, empresarial, social — strategic installations at any level. |
| **Primary language** | Español (México) |
| **Logo** | `assets/logo.png` — wordmark + isotype. The isotype reads as a stylized phoenix/eagle in 2D linework; symbolizes vigilance and protection. |

### Sources provided

- `uploads/logo.png` — full lockup (isotype + wordmark).
- `uploads/icon.svg` — isotype only, 1000×1000, originally unfilled. Re-colored variants live in `assets/icon{,-red,-white,-dark}.svg`.
- `uploads/LEMONMILK-{Bold,BoldItalic,Light,LightItalic}.otf` — display family.
- `uploads/Inter-VariableFont_opsz,wght.ttf` — body family.
- Brand notes from the founder: _"blanco de fondo, énfasis rojo `#AF282F`, secundario gris `#6F6F6F`, formal pero moderna."_

No codebase, Figma file, or sample product screens were provided. The UI kit in this system is therefore a **brand-aligned recreation** of a typical Tegra surface (corporate marketing site) — not a copy of an existing product. If a real product exists, please attach the codebase or Figma so we can replace the placeholders with the real components.

---

## Index

| File / Folder | What's in it |
|---|---|
| `colors_and_type.css` | All color, type, spacing, radii, shadow, motion CSS variables and semantic classes. The single source of truth. |
| `fonts/` | LEMON MILK (display) and Inter (body) font files. |
| `assets/` | Logo, isotype variants (`icon.svg`, `icon-red.svg`, `icon-white.svg`, `icon-dark.svg`). |
| `preview/` | Cards rendered in the Design System tab (color, type, spacing, components, brand). |
| `ui_kits/website/` | High-fidelity recreation of Tegra's corporate website (navbar, hero, services grid, footer). |
| `SKILL.md` | Agent Skill manifest — load this to design **as** Tegra. |
| `README.md` | This file. |

---

## CONTENT FUNDAMENTALS

### Language & tone

- **Primary language: Spanish (México).** Headlines, navigation, and product copy default to Spanish. English appears only in technical jargon when there is no good Spanish equivalent.
- **Tone: formal, sober, competent.** Tegra works with government and enterprise security — the brand sounds like an engineer who has done this a hundred times, not like a startup. No hype, no exclamation marks, no jokes.
- **Voice: third-person collective ("nosotros").** The company speaks as a team: _"Somos…", "Integramos…", "Atendemos…"_. Avoid first-person singular; avoid speaking directly _at_ the reader ("you / tú") in marketing copy — keep the distance respectful and professional.
- **Formal "you" only when needed.** If you must address the reader, use **"usted"** (never "tú"). Most pages won't need to.
- **No emoji. No exclamation marks. No marketing exclamations** like _"¡Increíble!"_ or _"¡Descúbrelo!"_. Calls-to-action stay neutral: _"Conocer más", "Contactar", "Solicitar propuesta", "Agendar diagnóstico"_.

### Casing

- **Headlines and section labels: Title Case** in Spanish style — first word and proper nouns capitalized; everything else lowercased. _"Soluciones de seguridad integral"_, not _"Soluciones De Seguridad Integral"_.
- **Eyebrow / overline labels: ALL CAPS** with letter-spacing (`--tracking-over`). _"PROPÓSITO"_, _"NUESTRO ENFOQUE"_, _"CASOS DE ESTUDIO"_.
- **Buttons: Sentence case.** _"Solicitar diagnóstico"_, not _"Solicitar Diagnóstico"_.
- **Navigation: Sentence case, single word when possible.** _"Servicios"_, _"Nosotros"_, _"Casos"_, _"Contacto"_.

### Vocabulary

The brand vocabulary leans toward the technical-engineering register Tegra actually works in. Prefer:

- _Soluciones_, _integración_, _diseño de ingeniería_, _instalaciones estratégicas_, _continuidad operativa_, _diagnóstico_, _atención_, _resolución_, _prevención_, _capital humano_, _eficiencia_, _crisis_, _oportuno_, _complejidad_.

Avoid:

- Generic SaaS-ese: _platform_, _ecosystem_, _seamless_, _empower_, _unlock_.
- Spanish marketing slop: _innovador líder_, _de vanguardia_, _experiencia única_, _solución 360°_.

### Sample copy

| Surface | Example |
|---|---|
| Hero headline | _"Soluciones de seguridad para instalaciones estratégicas."_ |
| Hero subhead | _"Integramos capital humano y diseños tecnológicos eficientes para atender crisis a cualquier nivel social, gubernamental y empresarial."_ |
| Section overline | _"PROPÓSITO"_ |
| Service card title | _"Diseño de ingeniería eléctrica"_ |
| Service card body | _"Planeación, especificación y supervisión de sistemas eléctricos para sitios críticos."_ |
| CTA primary | _"Solicitar diagnóstico"_ |
| CTA secondary | _"Conocer el método"_ |
| Footer tagline | _"Prevenir. Atender. Resolver."_ |

---

## VISUAL FOUNDATIONS

The visual system is built around a single instinct: **make the page look like an engineering document that happens to be on a screen.** Confident type, lots of white space, a thin red rule where attention is earned.

### Colors

- **Primary brand red — `#AF282F`.** Used sparingly: the underline beneath the active nav item, the primary button background, the accent rule under section overlines, the dot in a status pill, a single icon stroke on a hero illustration. Never as a full background of a section — too aggressive. When red is needed at scale, use `--tegra-red-soft` (`#E8C7CA`) or `--tegra-red-wash` (`#FBF2F3`) instead.
- **Secondary gray — `#6F6F6F`.** The brand's true workhorse. It's the color of the wordmark, of secondary copy, of icons, of borders at full strength. It does the structural lifting so red doesn't have to.
- **Neutral scale (0 → 1000).** A near-neutral warm-gray ladder. Use `--neutral-50/100` for sunken surfaces and alternating rows; `--neutral-200/300` for borders; `--neutral-600/700` for body text on white; `--neutral-900` for headings.
- **Semantic / feedback colors — not currently used.** Per brand direction (May 2026), the system **does not** apply success / warning / info colors today. When a status must be expressed visually, use a neutral pill or the brand red. The only "feedback" color in active use is `--danger`, which is just the brand red. Placeholder tokens for the others remain commented out in `colors_and_type.css` for future reactivation.
- **No gradients.** Tegra does not use gradients as a stylistic device. The only acceptable gradient is a black-to-transparent _protection scrim_ over a photo to keep white text legible.

### Typography

- **Two-family system: LEMON MILK Bold + Inter — Inter does most of the work.** Per brand direction (May 2026), LEMON MILK is reserved for a small set of brand moments; everything else is Inter.
  - **LEMON MILK Bold (`--font-display`)** — used **only** for:
    1. The wordmark / lockup ("TEGRA SOLUCIONES").
    2. The hero headline (the single biggest type moment on a page).
    3. Section overlines (the small uppercase eyebrow label above an H2).
    4. Large numeric display moments — stat numbers ≥ 32px.
  - **Inter (`--font-ui`)** — everything else: H2 / H3 / H4 section heads, lede, body, captions, hints, buttons, form inputs, nav links, status pills, tags, table cells, footer columns, case-study metadata.
  - Rule of thumb: **if it's NOT the wordmark, the hero headline, an overline, or a big number — it's Inter.**
- **Inter weights:** 400 for paragraph body, 500 for nav links and small UI labels, 600 for H2 / H3 / H4 and emphasized UI. Never use 700 in Inter — that weight is LEMON MILK's job.
- **Section heads use Inter 600 with negative letter-spacing** (`-0.02em` on H2) to feel modern and tight, not corporate.
- **No light / italic mixing.** LEMON MILK Light + italic files are present in `fonts/` but not in active rotation.
- **Mono:** system mono stack (`ui-monospace`, SF Mono, Menlo). Used for codes, IDs, timestamps, annotation labels.
- **Hierarchy by size & color, not weight.** Red is never used to colorize body type.

### Spacing & rhythm

- **4-px base.** All spacing tokens are multiples of 4.
- **Section vertical rhythm:** 96px (`--space-9`) between major sections on desktop, 64px (`--space-8`) on tablet, 48px (`--space-7`) on mobile.
- **Generous margins.** The brand prefers white space over decoration. A typical hero leaves 30–40% of the viewport empty.

### Borders, radii, cards

- **Corners are sharp or barely softened.** `--radius-sm` (2px) is the default for buttons and inputs. `--radius-lg` (8px) for cards and modals. **No pill buttons.** No 24-px-radius blob shapes.
- **Borders are hairline (1px) and quiet.** `--border` (#E3E3E3) for most boundaries. A **red 3px bottom rule** is the brand's signature accent — it appears under section overlines and as the active state of the nav.
- **Cards are flat by default.** A card is white-on-white-bg, defined by a 1px `--border`, no shadow. Shadow appears only on lift (hover) or on floating UI (menus, modals). When a shadow appears it is neutral and small (`--shadow-md`).
- **No colored left-border accent cards.** Anti-trope.

### Shadows & elevation

Restrained four-step ladder, all using `rgba(10,10,10,...)` so they never tint warm/cool.

| Token | Use |
|---|---|
| `--shadow-xs` | Inputs at rest. |
| `--shadow-sm` | Hovered cards, dropdown triggers. |
| `--shadow-md` | Floating cards, popovers, lifted modals. |
| `--shadow-lg` | Full modals, command palette. |
| `--shadow-focus` | Red 28% tint, 3px — focus ring on all interactive controls. |

### Imagery

- **Photography is desaturated and cool-leaning.** Photos of control rooms, datacenters, transmission towers, security installations — shot in available light, not over-color-graded. Apply a very subtle desaturation (`filter: saturate(0.85)`) when you can't reshoot.
- **No stock-art people-laughing-at-laptops.** If people appear, they're at work in PPE, in operations rooms, in real environments.
- **No hand-drawn illustration.** Tegra is not an illustrative brand. When a hero needs a graphic, prefer a photograph at 16:9 or 21:9, full-bleed, with a black-to-transparent scrim from the bottom-left.
- **No texture / pattern overlays.** Backgrounds are flat white or flat near-black. The single decorative element allowed is the **isotype mark** at low opacity (`opacity: 0.06–0.10`) as a corner watermark on dark CTA bands.

### Backgrounds

- **Default: pure white** (`--bg`). Body of every page.
- **Sunken:** `--neutral-50` for alternating sections, table headers, code blocks.
- **Inverse:** `--neutral-900` (near-black, not pure black) for the footer and for high-emphasis CTA bands.
- **Full-bleed photos:** allowed in heroes; always with a left-aligned dark scrim so headline text is on solid dark.

### Animation & motion

- **Easing:** `cubic-bezier(0.22, 0.61, 0.36, 1)` (`--ease-out`) for entry/exit; `cubic-bezier(0.65, 0, 0.35, 1)` (`--ease-in-out`) for state transitions.
- **Durations:** 120ms (`--dur-fast`) for hover, 200ms (`--dur-base`) for most state transitions, 320ms (`--dur-slow`) for modals / drawers.
- **No bounce.** No spring physics. No looping logo animations. Movement is short, decisive, engineering-quiet.
- **Allowed motions:** fade + 4px translate-up on scroll-reveal; underline grow on link hover; subtle scale (0.98) on button press.

### Interactive states

| State | Effect |
|---|---|
| Hover (button, primary) | Background goes from `--tegra-red` → `--tegra-red-deep`. No size change. |
| Hover (button, ghost) | Background goes from transparent → `--neutral-100`. |
| Hover (card) | Border shifts to `--border-strong`; `--shadow-sm` appears. No translate. |
| Hover (link) | Color shifts to `--tegra-red`; underline already present, no change. |
| Press / active | `transform: scale(0.98)` for 80ms then snap back. |
| Focus | `--shadow-focus` ring (3px, brand-red 28% alpha) + 2px solid `--tegra-red` outline on dark surfaces. |
| Disabled | `opacity: 0.4`; `cursor: not-allowed`; no hover changes. |

### Transparency, blur, scrims

- **Blur is reserved for sticky surfaces** — the navbar uses `backdrop-filter: blur(12px)` over a `rgba(255,255,255,0.82)` fill.
- **Protection scrims, not capsules.** When text sits over a photo, use a gradient scrim from `rgba(0,0,0,0.65)` at the text edge to transparent at the opposite edge. Never wrap text in a translucent pill — it cheapens the composition.
- **Glass / frosted panels are not part of the system.**

### Layout rules

- **Max content width: 1280px.** Hero / full-bleed sections still go edge-to-edge; inner content is constrained.
- **Grid: 12-column, 24-px gutter** at desktop. Layouts snap to 4 / 6 / 8 / 12 column groupings.
- **Section anatomy:** overline (uppercase, red 3px rule under) → H2 → optional lede paragraph → content. This rhythm is the brand's most recognizable pattern.

### Iconography

See the **ICONOGRAPHY** section below.

---

## ICONOGRAPHY

Tegra does not have a proprietary icon library. The system uses **[Lucide](https://lucide.dev)** as the canonical icon set — chosen for its consistent 1.5px stroke, generous 24×24 grid, and engineering-neutral feel that pairs cleanly with LEMON MILK.

> **Substitution flagged:** No icon set was provided with the brand assets. Lucide is a stand-in. If Tegra uses a proprietary set internally (e.g. in the operations dashboards), please share the SVG sources or sprite file and we'll swap them in.

### Usage rules

- **Stroke icons only.** Filled icons clash with the linework of the brand isotype.
- **Stroke weight: 1.5px** at 24×24. Never re-weight.
- **Color: `--fg-muted`** (`#6F6F6F`) by default. `--tegra-red` only when the icon _is_ the brand accent on the page (single instance), or for `danger`/`critical` semantic icons.
- **Sizes:** 16, 20, 24, 32. 16 only for inline-with-text use; 24 for buttons and lists; 32 for feature cards.
- **No emoji** anywhere in the UI. Not in product, not in marketing. The brand is too formal for the visual register emoji introduces.
- **No unicode "icons"** (✓, ✗, →, ★). Use the real Lucide glyph: `check`, `x`, `arrow-right`, `star`.

### Brand isotype

The isotype (`assets/icon.svg`) is a stylized phoenix/eagle in horizontal-line geometry, with two small red triangular accents (head + tail). It exists in four prepared variants:

| File | Use |
|---|---|
| `assets/icon.svg` | Two-color (red + gray) — default; sits on white. |
| `assets/icon-red.svg` | All-red — when the surrounding context is neutral and the mark needs to read as brand. |
| `assets/icon-white.svg` | All-white — for use on dark or photographic backgrounds. |
| `assets/icon-dark.svg` | All-near-black — for monochrome compositions and watermarks. |

### Loading Lucide

Add to the document head:

```html
<script src="https://unpkg.com/lucide@latest"></script>
<script>lucide.createIcons();</script>
```

Use in markup as `<i data-lucide="shield-check"></i>`.

---

## CAVEATS / WHAT'S MISSING

- **No real product was provided.** The UI kit recreates a plausible Tegra corporate website. If there is an existing site, app, dashboard, or Figma file — please share so we can replace the placeholder with the real thing.
- **Lucide is a substitution** for an unknown internal icon set. See above.
- **All fonts are present** (LEMON MILK + Inter); no Google Fonts fallback was needed.
- **Photography is referenced but not bundled.** Hero blocks use solid-color blocks where photos would go; this avoids inventing imagery. Please supply real photos when ready.

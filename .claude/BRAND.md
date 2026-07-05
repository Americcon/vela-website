# Vela Brand & Design System

Compiled from the Vela Dashboard React app. Use this as the authoritative reference when editing any Vela website or UI.

---

## Brand Identity

- **Name**: Vela (always capitalized, never all-caps)
- **Tagline**: "Second home, first-class care"
- **Product**: Premium concierge/property management for Mediterranean second-home owners
- **Regions**: Ibiza, Costa del Sol
- **Tone**: Quiet luxury — professional, trusted, warm. Not corporate. Not playful. Confident and approachable.
- **Aesthetic**: Sun-washed Mediterranean + Scandinavian minimalism. Glass surfaces, natural warmth, depth through layers.

---

## Color System

### Brand Colors
| Token | Hex | Use |
|-------|-----|-----|
| `--vela-green` | `#118A68` | Primary CTAs, active states, accents, brand mark |
| `--vela-green-dark` | `#0e7458` | Hover/pressed states |
| `--vela-green-light` | `#17a07b` | Gradient starts |
| `--vela-green-glow` | `rgba(17,138,104,0.4)` | Glow shadows on green elements |
| `--tint` | `#E6F4EF` | Soft mint, selection highlight, tinted backgrounds |
| `--surface` | `#FDFBF7` | Warm cream page background (sun-washed) |

### Neutrals
| Hex | Tailwind | Use |
|-----|----------|-----|
| `#0f172a` | `slate-900` | Dark mode page bg, primary dark text |
| `#1e293b` | `slate-800` | Dark mode primary text |
| `#3B4552` | custom `--ink` | Primary body text (light mode) |
| `#475569` | `slate-600` | Secondary text, form labels |
| `#64748b` | `slate-500` | Descriptive/muted text |
| `#94a3b8` | `slate-400` | Inactive icons, placeholders |
| `#e5e7eb` | `gray-200` | Card borders, dividers |
| `#f3f4f6` | `gray-100` | Subtle backgrounds |
| `#f9fafb` | `gray-50` | Input backgrounds |

### Semantic
| Color | Hex | Use |
|-------|-----|-----|
| Success | `#16a34a` / `#10b981` | Confirmations, active status |
| Warning | `#f59e0b` | Pending states, badges |
| Error | `#f43f5e` / `#dc2626` | Destructive actions, errors |

### Plan Tier Accents
| Plan | Accent |
|------|--------|
| Essential | `#118A68` |
| Basic | `#9A7B4F` (warm tan) |
| Plus | `#6B7280` (silver) |
| Premium | `#B8962E` (gold) |

---

## Typography

### Font
- **Primary**: `Plus Jakarta Sans` — geometric, modern, friendly
- **Fallback**: system sans-serif
- **Note**: Avoid Inter, Roboto, Arial. Plus Jakarta Sans is the definitive Vela font.

### Type Scale
| Role | Size | Weight | Notes |
|------|------|--------|-------|
| Hero H1 | `clamp(2.5rem, 5vw, 4rem)` | 800 | Tight tracking |
| Section H2 | `text-2xl`–`text-3xl` | 700 | |
| Card Title | `text-lg`–`text-xl` | 700 | |
| Body | `text-sm`–`text-base` | 500 | |
| Caption/Label | `text-xs` | 600–700 | Uppercase + `tracking-wide` |
| Micro Label | `text-[10px]` | 700 | Uppercase + `tracking-wider` |

### Letter Spacing
- Headings: `tracking-tight` (`-0.025em`)
- Brand name/logo: `-0.01em`
- Uppercase labels: `tracking-wide` (`0.025em`)
- Body: default

---

## Glassmorphism (Core Surface Pattern)

### Light Mode Glass Panel
```css
background: rgba(255, 255, 255, 0.72);
backdrop-filter: blur(24px);
-webkit-backdrop-filter: blur(24px);
border: 1px solid rgba(255, 255, 255, 0.6);
box-shadow: 0 4px 20px -2px rgba(0, 0, 0, 0.05);
```

### Dark Mode Glass Panel
```css
background: rgba(30, 41, 59, 0.72);
border: 1px solid rgba(51, 65, 85, 0.6);
box-shadow: 0 4px 20px -2px rgba(0, 0, 0, 0.3);
```

### Glass Hover Lift
```css
transition: all 0.4s cubic-bezier(0.25, 0.8, 0.25, 1);
&:hover {
  background: rgba(255, 255, 255, 0.85);
  border-color: rgba(255, 255, 255, 0.9);
  transform: translateY(-2px);
  box-shadow: 0 15px 35px -5px rgba(0, 0, 0, 0.08);
}
```

### Green-Edged Glass (Signup/Featured Cards)
```css
/* Outer wrapper */
background: linear-gradient(180deg, rgba(255,255,255,0.75), rgba(17,138,104,0.28));
box-shadow: 0 18px 52px rgba(3,7,18,0.28);
padding: 1px; /* creates gradient border effect */
/* Inner */
background: linear-gradient(to bottom right, rgba(255,255,255,0.78), rgba(255,255,255,0.56));
backdrop-filter: blur(22px) saturate(1.08);
```

---

## Buttons

### Primary (Vela Green Pill)
```css
background: #118A68;
color: white;
border-radius: 9999px; /* rounded-full */
padding: 0.75rem 1.25rem;
font-weight: 700;
box-shadow: 0 10px 15px rgba(0,0,0,0.1);
transition: all 200ms ease;

&:hover {
  background: #0e7458;
  transform: translateY(-2px);
  box-shadow: 0 20px 25px rgba(0,0,0,0.1);
}
&:active { transform: scale(0.95); }
```

### Secondary (White/Outlined)
```css
background: rgba(255,255,255,0.8);
border: 1px solid #e5e7eb;
color: #475569;
border-radius: 0.75rem; /* rounded-xl */
font-weight: 700;

&:hover { background: #ffffff; border-color: #d1d5db; }
```

### Ghost (Icon)
```css
padding: 0.5rem;
border-radius: 9999px;
background: transparent;
&:hover { background: rgba(0,0,0,0.05); }
```

---

## Border Radius
| Use | Value |
|-----|-------|
| Buttons (primary) | `rounded-full` |
| Buttons (secondary) | `rounded-xl` |
| Form inputs | `rounded-xl` |
| Cards (standard) | `rounded-2xl` (mobile) / `rounded-3xl` (desktop) |
| Feature/hero cards | `rounded-[1.5rem]` (mobile) / `rounded-[2.5rem]` (desktop) |
| Service tiles | `rounded-[1.25rem]` (mobile) / `rounded-[2rem]` (desktop) |
| Badges | `rounded-full` |

---

## Shadows
| Name | Value | Use |
|------|-------|-----|
| glass | `0 8px 32px rgba(31,38,135,0.07)` | Glass panels |
| glass-hover | `0 12px 40px rgba(31,38,135,0.12)` | Glass panels on hover |
| island | `0 8px 30px rgba(0,0,0,0.12)` | Floating/modal elements |
| green-glow | `0 4px 12px rgba(17,138,104,0.4)` | Green CTAs, active indicators |
| card | `0 1px 2px rgba(0,0,0,0.05)` | Resting cards |

---

## Animations

### Core Keyframes
```css
@keyframes breathe {
  0%, 100% { transform: scale(1); box-shadow: 0 4px 20px -2px rgba(17,138,104,0.1); }
  50% { transform: scale(1.01); box-shadow: 0 10px 25px -3px rgba(17,138,104,0.25); }
}
/* Use: Featured/CTA cards — 4s ease-in-out infinite */

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

@keyframes scaleIn {
  from { opacity: 0; transform: scale(0.95); }
  to { opacity: 1; transform: scale(1); }
}

@keyframes shimmer {
  0% { background-position: -200% 0; }
  100% { background-position: 200% 0; }
}
/* Use: Loading skeletons */

@keyframes hueShift {
  0%, 100% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
}
/* Use: Animated gradient backgrounds — 15s ease infinite */
```

### Timing Guidelines
- Button feedback: `200ms ease`
- Card hover: `300–500ms ease`
- Tab/nav transitions: `280ms cubic-bezier(0.4, 0, 0.2, 1)`
- Page entrance: `300–500ms ease-out`
- Theme transitions: `300ms ease`
- Always respect `prefers-reduced-motion`

---

## Spacing & Layout
- Base unit: 4px (Tailwind default)
- Page container: `max-w-7xl mx-auto` (marketing) / `max-w-[1600px]` (dashboard)
- Page padding: `px-6` (desktop) / `px-4` (mobile)
- Section spacing: `space-y-10` (desktop) / `space-y-6` (mobile)
- Card padding: `p-6` (desktop) / `p-4` (mobile)

---

## Form Inputs
```css
border-radius: rounded-xl;
padding: px-4 py-3;
background: rgba(255,255,255,0.5) or #f9fafb;
/* Border via inset box-shadow */
box-shadow: inset 0 0 0 1px rgb(226 232 240);
transition: box-shadow 200ms ease;

/* Focus */
box-shadow: 0 0 0 3px rgb(17 138 104 / 0.25), inset 0 0 0 1px rgb(226 232 240);
outline: none;

/* Label */
font-size: text-xs; font-weight: bold; text-transform: uppercase; letter-spacing: tracking-wide; color: slate-600;
```

---

## Status / Badges
```css
/* Pill badge */
border-radius: rounded-full;
padding: px-3 py-1.5;
font-size: text-[10px];
font-weight: bold;
text-transform: uppercase;
letter-spacing: tracking-wide;
background: rgba(255,255,255,0.9);
backdrop-filter: blur;

/* Pulsing live dot */
/* Outer: animate-ping, emerald-400, opacity-75 */
/* Inner: emerald-500 */
```

---

## Design Principles (from Dashboard)

1. **Clarity** — purpose-driven elements, obvious visual hierarchy
2. **Quiet luxury** — restraint over decoration; no gratuitous gradients, no busy patterns
3. **Glass depth** — layered frosted surfaces create richness without noise
4. **Warmth** — cream backgrounds (#FDFBF7), organic greens, never cold/clinical
5. **Confidence** — bold typography, not tentative sizing or color choices
6. **Precision** — every spacing decision matters, especially in minimalist areas
7. **Trust** — clean, consistent, professional; no cheap effects or gimmicks

---

## What to Avoid

- Generic AI fonts: Inter, Roboto, Arial, system fonts
- Purple gradients on white backgrounds
- Cookie-cutter hero layouts (centered headline + two buttons + stock photo)
- Flat, buttonless design (no depth or shadow)
- Too many animations competing for attention
- Inconsistent border-radius mixing (commit to a style per component)
- Heavy drop shadows without blur (looks cheap)
- Plain white or pure gray backgrounds — always use `#FDFBF7` warm surface

---

## Marketing Site vs Dashboard

The dashboard is the product (used daily by owners after login). The marketing site (index.html) is the first impression — it must convey:

- **Trust**: This is a real, premium service
- **Clarity**: What is Vela, what do they get, how much does it cost
- **Aspiration**: Mediterranean lifestyle, second-home fantasy
- **Action**: Sign up / get in touch CTA

The website should feel like the *lobby of a luxury hotel* — not like a SaaS landing page template.

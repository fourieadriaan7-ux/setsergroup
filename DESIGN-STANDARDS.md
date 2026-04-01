# Design Standards

Use this file as the baseline when standardizing page design across the site.

## Core Rules

- Reuse shared patterns before inventing a one-off version.
- Keep nav styling consistent across all pages.
- Keep hero typography and overlays aligned to the established hero system unless there is a strong reason not to.
- Major section headings should use one consistent style across a page.
- Avoid decorative gradients inside content cards unless they serve a clear purpose.

## Typography

### Hero Heading

Use the same scale and rhythm as the About hero:

```css
font-size: clamp(32px, 4.5vw, 64px);
font-weight: 600;
line-height: 1.12;
letter-spacing: -0.025em;
```

### Section Kicker

Use for small uppercase labels above sections:

```css
font-size: 12px;
font-weight: 600;
letter-spacing: 0.1em;
text-transform: uppercase;
color: var(--navy);
```

### Section Heading

Use for major H2s like content sections, support sections, and partner sections:

```css
font-size: clamp(24px, 2.8vw, 38px);
font-weight: 600;
line-height: 1.15;
letter-spacing: -0.025em;
color: #1a2332;
```

For highlighted words:

```css
font-style: normal;
color: var(--navy);
```

### Body Copy

Use for primary section paragraphs:

```css
font-size: 15px;
line-height: 1.85;
color: #6b7a82;
```

## Hero System

### Hero Background

Match the About page structure:

1. Solid dark blue base layer
2. Separate background image layer
3. Shared overlay gradient

Reference pattern:

```css
background-color: #0a1a40;
background-image: url(...);
background-size: cover;
background-position: center;
background-repeat: no-repeat;
opacity: .68;
```

Overlay:

```css
background: linear-gradient(
  135deg,
  rgba(10,18,40,.72) 0%,
  rgba(0,40,130,.48) 60%,
  rgba(0,63,99,.32) 100%
);
```

### Hero Layout

- Keep hero copy centered when the product/image mockup is the focal point.
- If using a dashboard or laptop mockup, let it be the main visual anchor.
- The next section can overlap the mockup, but the overlap should feel intentional and not create dead space.

## Cards

### Content Cards

Preferred default:

```css
background: #fff;
border: 1px solid #dbe3ea;
border-radius: 16px;
```

Avoid:

- soft decorative gradients inside informational cards
- different card surfaces for cards that serve the same purpose

### Glass / Overlay Chips

Use only when the card sits over an image or hero background. Prioritize contrast over effect.

Preferred direction:

```css
background: rgba(9,21,43,.82);
border: 1px solid rgba(154,196,255,.22);
color: rgba(255,255,255,.92);
```

## Navigation

- Navigation is a shared site component.
- Do not redesign it per page unless the whole site is being updated.
- Match existing spacing, logo treatment, button styling, and scroll behavior.

## Spacing

### Standard Section Padding

Desktop:

```css
padding: 60px 60px;
```

Tablet:

```css
padding: 72px 40px;
```

Mobile:

```css
padding: 60px 24px;
```

### First Section After Hero

- If the hero image overlaps into the next section, place the extra offset on the first real content section.
- Do not use a temporary spacer section unless it contains actual content.

## Consistency Checklist

When reviewing a page, check:

- Do all major section H2s use the same style?
- Does the hero feel like the same product family as About/Home?
- Is the nav unchanged from the shared site standard?
- Are card surfaces flat and consistent?
- Are accent colors used sparingly and intentionally?
- Does the mockup/image overlap feel deliberate rather than accidental?

## Recommended File Workflow

When standardizing another page:

1. Match the hero system first.
2. Normalize all H2 section headings.
3. Normalize card surfaces and borders.
4. Remove one-off gradients and decorative exceptions.
5. Verify responsive spacing last.

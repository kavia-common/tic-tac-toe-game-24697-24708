# Ice Cream Landing Page — Design Notes

Source: screen_5-2.png

Overview
- Type: Single-page marketing landing page for an ice cream brand.
- Layout: Stacked vertical sections with high-contrast hero, promotional band, product grid, feature band, testimonials/USP band, and footer.
- Visual style: Bold, playful, rounded shapes; bright warm gradient backgrounds; large, uppercase headings; rounded cards and buttons; floating accent shapes (confetti/doodles).

Assumed Base
- Canvas width: ~1440px desktop design
- Content container max-width: 1200px (centered)
- Grid: 12-column, 24px gutters (inferred); section paddings vary.
- Layout method: Flexbox + CSS Grid for product cards.

Color Tokens (CSS variables)
- --bg-canvas: #FF6A67 (warm coral background across sections)
- --bg-hero-overlay: linear-gradient(140deg, #FF7B6E 0%, #FF4F79 60%, #FFB34E 100%) [used as hero gradient blocks and promo bands]
- --bg-card: #FFFFFF
- --bg-chip: #FFD9A4 (pill labels)
- --bg-badge: #FEEBE1 (light salmon badge behind price/labels)
- --bg-yellow-gradient: linear-gradient(140deg, #FFB84D 0%, #FF9A3D 100%) [promo band]
- --primary-text: #FFFFFF
- --heading-text: #FFFFFF
- --subheading-text: #FFE8E8
- --body-text: #5F2D3B (dark plum-brown for body, labels)
- --muted-text: #9B5B5B
- --accent-pink: #FF4F79
- --accent-coral: #FF6A67
- --accent-yellow: #FFCD59
- --accent-green: #7ED957
- --button-primary-bg: #FFFFFF
- --button-primary-text: #FF4F79
- --button-secondary-bg: rgba(255,255,255,0.2)
- --button-secondary-text: #FFFFFF
- --price-text: #FFCD59
- --chip-text: #A34A2B
- --divider: rgba(255,255,255,0.25)
- --footer-bg: #E4585D

Typography
- Base font: "Helvetica Neue", Arial, sans-serif (assumed)
- Headings: Bold, uppercase, tight tracking
  - H1 hero: 64–72px, 800, letter-spacing: 0.5px, line-height: 1.05
  - H2 section titles: 44–56px, 800, letter-spacing: 0.5px, line-height: 1.1
  - H3 product card titles: 20–22px, 700, line-height: 1.2
- Body:
  - Lead/eyebrow: 14–16px uppercase, 700
  - Paragraph: 16–18px, 400–500, line-height: 1.6
- Buttons: 16–18px, 700 uppercase
- Price: 20–22px, 800 (highlight color)

Spacing Scale
- 4, 8, 12, 16, 20, 24, 32, 40, 48, 56, 64, 80
- Section padding (desktop): 80–96 top/bottom
- Container horizontal padding: 24–32
- Card padding: 20–24
- Gaps: grids 24–32; inline 8–16

Borders & Radius
- Global rounded corners: 16–24px on large blocks/sections
- Cards & buttons: 12–16px radius
- Pills/Chips: 9999px (full)

Shadows (subtle)
- Cards: 0 10px 30px rgba(0,0,0,0.08)
- Floating images: stronger soft shadow 0 20px 50px rgba(0,0,0,0.15)

Iconography
- Minimal: small arrows, hearts, stars; likely SVG
- Social icons in footer (assumed): monochrome on brand background

Images
- Hero ice cream cones/cups: large photoreal renders with soft shadows
- Product cards: isolated product renders with drop shadows
- Alt text: descriptive of flavor/product

Header (Global)
- Position: sticky top (optional), on brand background
- Structure:
  - Left: Brand logo wordmark (text “CORN”/brand) and possible small mascot/emblem
  - Center: Primary nav (Home, Menu, Shop, About, Contact) – uppercase links
  - Right: CTA button “Buy Now” or “Order” + maybe cart icon
- Spacing:
  - Height: 72–80px
  - Horizontal padding: 32px
  - Gap between nav items: 24px
- States:
  - Nav hover: underline or color shift to --primary-text with slight opacity change
  - CTA hover: elevate shadow, slight scale 1.02

Hero Section
- Background: large diagonal gradient block with floating abstract shapes
- Left block:
  - Eyebrow chip: “CORN” pill, background --bg-chip (#FFD9A4), text --chip-text; padding 6px 12px; radius 9999px; uppercase 12–14px bold
  - Heading H1: “ENJOY YOUR EVERY BITE” (split across lines); white, bold, uppercase, 64–72px
  - Subtext: short line ~18px, light pink/white
  - Primary CTA: “Buy Now” (Button) – white bg, pink text, 16–18px bold, radius 12–16px, padding 14px 24px
  - Secondary CTA: text/link or ghost button with white border or translucent bg
- Right block:
  - Hero image: tall ice cream cone angled; height ~520–580px; offset to the right with overlap; strong shadow
  - Floating pill buttons vertically stacked (right edge):
    - Pink rounded rectangles with white icon/text (e.g., heart/like, cart, share). Radius ~16px; padding 10–12; spacing 12–16px; subtle drop shadow.

Section: Feature Highlight (left image circle + right text)
- Left: Circular image container (mask) with product cup centered; 320–360px diameter; subtle decorative doodles
- Right:
  - H2: “ENJOY YOUR EVERY BITE” styled similar to hero but smaller (48–56px)
  - Paragraph: 16–18px, light white text
  - Button: “Read More” or “Shop Now” pink/white variant; prominent

Section: Popular Ice Cream (Product Grid)
- Title Row:
  - Left: H2 “POPULAR ICE CREAM”
  - Right: Small filters/tabs chip (e.g., “All”) – pill with icon
- Cards (3-up):
  - Card container: white bg (#FFFFFF), radius 16px, padding 20–24, drop shadow
  - Product image: centered, larger than title, with shadow; slightly overlapping top margin
  - Title: 20–22px bold; dark text
  - Rating row: small star icons + rating number (optional)
  - Price + Add button:
    - Price: highlighted in --price-text (#FFCD59) or dark; bold
    - Add button: small circular button with + icon; pink bg (--accent-pink); white icon; 40–44px size
- Gaps: 24–32 between cards

Promo Band (Yellow Gradient)
- Full-width rounded rectangle band with gradient --bg-yellow-gradient
- Left: Eyebrow chip “Discount” pill
- Main text: “BUY 2 GET 1 FREE” large white bold, uppercase (48–56px)
- Right: Large product image (single scoop cup) overlapping bottom edge
- CTA optional (not very prominent)

Section: USPs / Feature Icons
- Card-style band on coral background
- Two or three rounded blocks:
  - Each block: white bg, radius 16px, padding 24
  - Icon (e.g., delivery, quality) in a rounded square
  - Title: 18–20px bold
  - Description: 14–16px muted
- Sample content: “Fast and Best Quality Ice Cream”, etc.

Footer
- Background: darker coral --footer-bg #E4585D
- Columns: 3–4 columns with headings and links
  - Column headings: 14–16px bold uppercase; white
  - Links: 14–16px, white with reduced opacity; hover: full white
- Bottom bar: copyright, terms, social icons
- Padding: 48 top/bottom

Responsive Behavior
- Breakpoints:
  - ≥1200px: 12-col grid; product grid 3-up
  - 992–1199px: product grid 2-up; hero stacks image right but smaller
  - ≤768px: single-column stack; paddings reduced to 24; font sizes scale down (H1 40–44px, H2 32–36px)
- Floating right-side action pills collapse/stack to bottom-right fixed fab on mobile.

Component Specs

1) Button Primary
- Background: --button-primary-bg (#FFFFFF)
- Text: --button-primary-text (--accent-pink)
- Padding: 14px 24px
- Radius: 14px
- Font: 700 16px uppercase
- Hover: transform: translateY(-2px); shadow elevation + subtle pink border

2) Button Secondary (Ghost)
- Background: --button-secondary-bg (rgba(255,255,255,0.2))
- Border: 1px solid rgba(255,255,255,0.5)
- Text: #FFFFFF
- Padding: 12px 20px
- Radius: 14px
- Hover: background rgba(255,255,255,0.3)

3) Product Card
- Container: bg #FFFFFF; radius 16px; padding 20–24; shadow (0 10px 30px rgba(0,0,0,0.08))
- Image: 220–260px tall; margin-top: -24 (overlap optional)
- Title: 20–22px bold; color --body-text
- Meta row: star icons + rating (optional)
- Price row:
  - Price: 20–22px 800; color --accent-yellow (#FFCD59)
  - Add button: 40–44px circular; bg --accent-pink; icon white

4) Chip
- Background: --bg-chip (#FFD9A4)
- Text: --chip-text
- Padding: 6px 12px
- Radius: 9999px
- Text: 12–14px bold uppercase

5) Header/Nav
- Height: 80px; container padding 0 32px
- Logo left (text or image)
- Nav center: 5–6 links; gap 24px
- CTA right: Primary button

6) Floating Action Stack (Right of hero)
- Vertical stack of 3 pill buttons
- Size: 44–48px height x auto; radius 14–16px
- Background: --accent-pink or white with contrast; shadow

Exact Section-by-Section Layout (Desktop)

Header
- Wrapper: height 80; display: flex; align-items: center; justify-content: space-between
- Max width: 1200; centered; padding: 0 32

Hero
- Section padding: 96 0
- Container: display: grid; grid-template-columns: 1.2fr 1fr; gap: 48
- Left:
  - Chip (top): margin-bottom: 16
  - H1: margin: 12 0 16
  - Body: margin-bottom: 24
  - Actions: flex; gap: 16
- Right:
  - Hero image aligned end, max-height: 560px
  - Floating stack: position: absolute; right: 24; top: 50%; gap 12

Feature Split
- Grid: 1fr 1fr; gap: 48
- Left: circle image (diameter 340); decorative shapes absolute
- Right: H2, paragraph, button; stacked with 16–20 gap

Popular Products
- Header row: flex space-between; align-center; margin-bottom: 24
- Grid: 3 columns; gap: 24–32; cards as spec above

Promo Yellow Band
- Wrapper: background: --bg-yellow-gradient; radius: 20; padding: 32–40; display: grid; grid-template-columns: 1.4fr 1fr; align-center
- Title large white; chip left/top
- Right: product image large with shadow; overflows bottom slightly

USP/Feature Band
- Grid: 2 or 3 feature cards; gap: 24
- Each card: white bg, padding 24; icon + title + body; center-aligned

Footer
- Top grid: 3–4 columns; gap 24–32; links stacked; padding 48 0
- Bottom bar: 1px divider; small text

Accessibility
- Contrast: Ensure text on gradients meets contrast; use text shadows subtly if needed
- Focus rings: 2px outline with --accent-pink on focusable elements
- Alt text: Descriptive for product images and icons

Notes on Assets
- Icons: prefer inline SVG for crispness
- Images: export as webp with transparent background where overlapping cards

End of design notes.

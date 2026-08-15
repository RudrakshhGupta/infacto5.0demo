<div align="center">
✦ INFACTO: THE FIFTH EDITION ✦
Official Landing Page

The flagship debate & public speaking event of The Orator Club, IIIT Nagpur

Show Image Show Image Show Image Show Image Show Image

</div>
Overview

A cinematic, single-page landing website built for Infacto: The Fifth Edition — the annual debate and public speaking event organised by The Orator Club, IIIT Nagpur. The page is designed to communicate prestige, tradition, and intellectual excellence through a grand Medieval European aesthetic, blending gothic architecture motifs with modern web animation.

┌─────────────────────────────────────────┐
│         [ Orator ] ─── [ IN ] ─── [ IIIT ]   │  Logo row
│                                         │
│     ◈ REGISTRATIONS OPENING SOON ◈      │  Pulse badge
│                                         │
│         The Orator Club · IIIT Nagpur · Presents
│                                         │
│  ██████████████████████████████████     │
│  ██   I N F A C T O               ██   │  Hero title
│  ██████████████████████████████████     │  (shimmer gold)
│               The Fifth Edition         │
│                                         │
│    ── ◆ ──  Registrations Starting Soon ── ◆ ──
│                                         │
│            [ Stay Informed ]            │  CTA
│                                         │
│  ▓▓▓▓▓▓ Castle Silhouette ▓▓▓▓▓▓▓▓▓▓▓  │  SVG silhouette
└─────────────────────────────────────────┘
Features

Visual Design

Full-screen hero with an animated HTML5 Canvas background — 90 floating gold particles with realistic fade, drift, and lifecycle behaviour
Hand-crafted SVG gothic arch frame that frames the hero title
SVG castle silhouette with battlements, towers, and lancet windows built entirely in-code (no image assets required)
Cinzel + Cormorant Garamond + EB Garamond type stack for a medieval-manuscript feel
background-clip: text shimmer animation on the main title using a moving gradient
Soft ambient glow pulse on the hero title using a requestAnimationFrame loop

Animations

Staggered entrance sequence: logo row → badge → eyebrow → title → divider → subtitle → CTA, timed across 2.5 seconds
Parallax scrolling: castle drifts at 0.18× scroll speed, arch at 0.08×, creating depth
IntersectionObserver scroll-reveal on all below-fold sections
Pillar cards staggered at 120ms offsets on reveal
Animated scroll-line indicator (CSS scaleY loop)

Sections

Hero — full-screen proclamation with all logos, badge, title, and CTA
About — oratory tradition copy with ornamental rule divider
Four Pillars — Debate, Rhetoric, Leadership, Excellence; hover reveals gold top border
Notification form — email capture with a polished inline response message
Footer — mirrored logo row with copyright

Technical

Zero dependencies, zero npm, zero build step — one .html file
Vanilla JS only (Canvas API, IntersectionObserver, requestAnimationFrame)
Google Fonts loaded via <link> with rel="preconnect" for speed
prefers-reduced-motion respected via CSS media query
Semantic HTML5 with ARIA labels on interactive and decorative elements
Fully responsive from 320px mobile to 4K desktop
Colour Palette
Name	Hex	Usage
Royal Gold	
#D4AF37	Primary accent, borders, title shimmer
Gold Light	
#F0D060	Hover states, subtitle accent
Antique Ivory	
#F8F1E5	Body text, general foreground
Deep Burgundy	
#4A0E0E	Radial gradient overlays
Deep Navy	
#0F1F3D	Side gradient overlays
Dark Charcoal	
#1B1B1B	Card and UI element base
Near Black	
#0A0A0F	Page background
Typography
Role	Family	Weight
Display / Title	Cinzel	900
Subheadings / Labels	Cinzel	400–600
Pull quotes / Subtitles	Cormorant Garamond	300 italic
Body copy	EB Garamond	400–500
Getting Started

No build tools required. Clone and open.

bash
git clone https://github.com/your-org/infacto-5.git
cd infacto-5
open infacto5.html   # macOS
# or: start infacto5.html (Windows)
# or: xdg-open infacto5.html (Linux)

For local development with live reload:

bash
npx serve .
# visit http://localhost:3000
Logo Setup

The page references three image files. Place them in the same directory as infacto5.html:

File	What it is
event-logo.png	Infacto 5.0 event logo
orator-logo.png	The Orator Club logo
iiitn-logo.png	IIIT Nagpur institutional logo

All three have onerror fallbacks — the page renders gracefully if any are missing, showing a styled placeholder instead.

Connecting the Notification Form

The email capture form currently shows a client-side confirmation message. To wire it to a real backend, replace the handleNotify function in the <script> block:

Option A — Formspree (easiest)

html
<form class="notify-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">

Option B — Mailchimp embedded form
Replace the form action with your Mailchimp list subscription endpoint.

Option C — Custom backend

js
async function handleNotify(e) {
  e.preventDefault();
  const email = e.target.querySelector('input[type="email"]').value;
  await fetch('/api/notify', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ email })
  });
  document.getElementById('notify-msg').textContent =
    'Your name has been entered in the rolls.';
  e.target.reset();
}
Deployment

The entire site is a single .html file with no external JS dependencies beyond Google Fonts. It can be deployed anywhere:

GitHub Pages — push to a gh-pages branch or enable Pages from main
Netlify / Vercel — drag and drop the file, or connect the repo
Any static host — upload infacto5.html + the three logo PNGs
Project Structure
infacto-5/
├── infacto5.html        # Entire site — HTML, CSS, JS in one file
├── event-logo.png       # Infacto 5.0 logo (add your own)
├── orator-logo.png      # The Orator Club logo (add your own)
├── iiitn-logo.png       # IIIT Nagpur logo (add your own)
├── README.md
└── docs/
    └── preview.png      # Add a screenshot here
Customisation

Change event details — Edit the hero eyebrow, tagline, and About section body copy directly in the HTML.

Swap fonts — Replace the Google Fonts <link> href and update the font-family declarations in :root and the relevant CSS classes.

Adjust particle count/behaviour — In the Canvas script, change NUM_PARTICLES (default 90) and the speed/size ranges inside the Particle constructor.

Add more sections — Each section follows the pattern of [data-reveal] on the wrapper for automatic scroll animation. Copy a section block and it animates in for free.

Credits

Designed and developed for The Orator Club, IIIT Nagpur.

	
Event	Infacto: The Fifth Edition
Organiser	The Orator Club
Institution	Indian Institute of Information Technology, Nagpur
Type	Debate & Public Speaking
<div align="center">

"Where Reason Meets Rhetoric — Where Champions Are Forged"

⚜ Infacto: The Fifth Edition ⚜

</div>

# Nexora

Marketing site for a web development & custom CRM studio. Single static page
(`index.html`) styled with a pre-compiled Tailwind build and animated with
self-hosted GSAP — no runtime CDN dependency except Google Fonts.

## Structure

- `index.html` — the entire site (nav, hero, services, CRM showcase, process,
  work, testimonials, pricing, contact, footer).
- `assets/css/tailwind.css` — compiled Tailwind utilities (see `assets/README.md`
  to rebuild after editing markup classes).
- `assets/css/custom.css` — hand-written CSS (glassmorphism, gradient blobs,
  marquee, reveal-animation base styles).
- `assets/js/gsap.min.js`, `assets/js/ScrollTrigger.min.js` — self-hosted GSAP,
  driving entrance/scroll-reveal/counter animations (all `prefers-reduced-motion`
  aware).

## Editing

It's plain HTML/CSS/JS — open `index.html` in a browser to preview, or serve the
folder with any static file server. Swap the placeholder brand name ("Nexora"),
copy, pricing, portfolio items and testimonials for the real business before
launch, and point the contact form at a real endpoint (it currently falls back
to a `mailto:` submit).

# Assets

Self-hosted so the site has zero runtime CDN dependency (only Google Fonts, which is
fetched for the `Plus Jakarta Sans` typeface).

- `css/tailwind.css` — Tailwind CSS, pre-compiled and purged for `index.html`.
  Rebuild after changing classes in `index.html`:
  ```
  npm i -D tailwindcss@^3
  npx tailwindcss -i <input.css with @tailwind base/components/utilities> \
    -o assets/css/tailwind.css --minify \
    --content index.html
  ```
  (Reuse the color/font tokens under `theme.extend` — see git history for the config
  used to generate the current build.)
- `css/custom.css` — hand-written CSS for effects Tailwind doesn't cover (glass
  panels, gradient blobs, the marquee, reveal-animation base styles).
- `js/gsap.min.js`, `js/ScrollTrigger.min.js` — GSAP 3, self-hosted (free under
  GreenSock's standard "no charge" license as of 2024). Used for the entrance,
  scroll-reveal, floating-mockup and counter animations in `index.html`. All
  animation respects `prefers-reduced-motion`.

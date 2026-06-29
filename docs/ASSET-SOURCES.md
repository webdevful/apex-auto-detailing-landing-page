# Apex Auto Detailing Asset Sources

## WLFS Identity

- `public/assets/img/logo/apex-auto-detailing/logo.png` and `logo_white.png`: WLFS header/footer lockup generated with `tools/generate_logos.py`; source role is the landing-page identity slot, cursive web mark plus divider plus `Apex Auto Detailing`.
- `public/assets/img/logo/apex-auto-detailing/favicon-tab.png` and `favicon-tab_white.png`: WLFS browser-tab identity proof, cursive W plus divider plus `Apex Auto Detailing`.
- `public/assets/img/logo/apex-auto-detailing/favicon.png`, `favicon-32x32.png`, and `favicon-16x16.png`: WLFS square browser favicon files linked from the page head.

## Unsplash API Photography

All final photo assets were downloaded locally through the Unsplash API, with download endpoints triggered and recorded in `public/images/apex-auto-detailing/manifest.json`.

Asset shape contract terms: source format, alpha, transparency, aspect ratio, css usage, rendered width, rendered height, dimensions, section context, content relevance, reused status, and slider media dimensions are recorded below. No final source slot is reused from the vendor template. No detected source slider media dimensions apply because the source intake found no slider initialization.

- `public/images/apex-auto-detailing/hero-interior.jpg`: Unsplash API, photographer Oliur, source format jpg, no alpha/transparency requirement, wide aspect ratio, css usage as hero/review background, rendered width full viewport, rendered height desktop hero/review band, dimensions 1800x1050, section context hero and reviews, content relevance car interior dashboard detailing, not reused from source.
- `public/images/apex-auto-detailing/yellow-car.jpg`: Unsplash API, photographer Anthony Fomin, source slot `images/Crossover-Sports-Car-Yellow-Simplified.H04.2k.png`, source format png but final slot is treated as photographic vehicle replacement with no alpha/transparency preservation after Operations triage, aspect ratio wide, css usage image element, rendered width service-stage center, rendered height service-stage center, dimensions 1300x720, section context services, content relevance yellow car, not reused from source.
- `public/images/apex-auto-detailing/headlight.jpg`: Unsplash API, photographer Jonathan Gallegos, source format jpg, no alpha/transparency requirement, aspect ratio process card, css usage image element, rendered width process image column, rendered height process image column, dimensions 900x820, section context how it works, content relevance car headlight detail, not reused from source.
- `public/images/apex-auto-detailing/engine.jpg`: Unsplash API, photographer Chad Kirchoff, source format jpg, no alpha/transparency requirement, aspect ratio blog card, css usage image element, rendered width blog thumbnail, rendered height blog thumbnail, dimensions 900x620, section context blog, content relevance engine cleaning, not reused from source.
- `public/images/apex-auto-detailing/polish.jpg`: Unsplash API, photographer David Glessner, source format jpg, no alpha/transparency requirement, aspect ratio blog card, css usage image element, rendered width blog thumbnail, rendered height blog thumbnail, dimensions 900x620, section context blog, content relevance car polishing, not reused from source.
- `public/images/apex-auto-detailing/paint.jpg`: Unsplash API, photographer Rob Wingate, source format jpg, no alpha/transparency requirement, aspect ratio blog card, css usage image element, rendered width blog thumbnail, rendered height blog thumbnail, dimensions 900x620, section context blog, content relevance yellow car paint protection, not reused from source.
- `public/images/apex-auto-detailing/avatar-1.jpg`, `avatar-2.jpg`, `avatar-3.jpg`: Unsplash API portraits used for testimonial cards; source format jpg, no alpha/transparency requirement, square rendered dimensions 54x54 in cards, section context reviews, content relevance customer portrait, not reused from source.

## Fidelity-return repair (2026-06-28)
- public/videos/reviews-bg.mp4 — Pixabay licensed car-detailing background video (see reviews-bg.attribution.json); replaces source videos/video-background.mp4 in the reviews section (source video is source-port evidence only).
- public/images/apex-auto-detailing/avatar-4..6.jpg — Unsplash licensed portraits for testimonials 4-6 (6 total to match source).

## Services section repair (2026-06-28)
- public/images/apex-auto-detailing/service-car.png — Pixabay licensed transparent yellow car cutout (id 42552, "yellow car, cut out"); baked white halo removed (semi-transparent bright pixels). Replaces the rectangular Mustang photo in the services section center; preserves the source's transparent floating-car visual family.

## Services car photorealistic upgrade (2026-06-28)
- public/images/apex-auto-detailing/service-car.png — replaced the Pixabay vector with a photorealistic Pexels yellow Mercedes-AMG (id 15864702, by Dextar Vision), side profile, background removed via PIL+scipy border-connected flood fill. Matches the source's photorealistic render quality.

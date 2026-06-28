# Apex Auto Detailing Design Contract

## Source Baseline

- Source URL: `https://axemobile.widagdos.net/?storefront=envato-elements`
- Capture: `/Volumes/WDF-NAS-01/04-Projects/Internal-Projects/Codebases/webdevful-astro-main/captures/axemobile-widagdos-net/desktop/screenshot-fullpage.png`
- Structure: one-page car-detailing template with sticky dark header, hero, three-card feature strip, about text split, service cards around a yellow vehicle image, why-choose card, three-step process, testimonial grid, pricing cards, centered CTA, FAQ, blog cards, and footer.
- Runtime: source uses Bootstrap, AOS, CSS transitions, hover card lifts, FAQ tabs, and no detected sliders.

## Tokens

```json
{
  "color": {
    "ink": "#0b0c0b",
    "panel": "#181a18",
    "panelSoft": "#151715",
    "line": "rgba(255,255,255,0.08)",
    "paper": "#f7f7ef",
    "muted": "#cfd0c6",
    "accent": "#fff326",
    "accentInk": "#12130f",
    "steel": "#5f6c67"
  },
  "typography": {
    "sourceBody": "Public Sans / Libre Franklin family",
    "finalBody": "Inter, Arial, sans-serif",
    "heroDesktop": "4.5rem",
    "heroTablet": "3.3rem",
    "heroMobile": "2.45rem",
    "sectionDesktop": "2.7rem",
    "bodyLineHeight": "1.72"
  },
  "shape": {
    "cardRadius": "8px",
    "buttonRadius": "999px",
    "desktopContainer": "1180px",
    "mobileGutter": "20px"
  }
}
```

## LPF Adaptation Notes

- WLFS generated the header/footer logo and favicon bundle for `Apex Auto Detailing`.
- Final photographic slots use local Unsplash API downloads recorded in `docs/ASSET-SOURCES.md`.
- Source reveal behavior is implemented as visible-by-default CSS transitions and hover states so content never renders blank without JavaScript.
- Source FAQ tab content is adapted to accessible native `details` panels.

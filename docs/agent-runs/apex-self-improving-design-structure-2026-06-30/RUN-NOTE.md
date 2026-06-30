# Apex Auto Detailing Self-Improving Design/Structure Run

Date: 2026-06-30
Ticket: `LPF_REPAIR-apex-auto-detailing-2026-06-30`
Order: `#2`
Agent badge: `Codex: Apex Auto Detailing Self-Improving Repair / thread codex-app-current-2026-06-30`

## Assignment

Owner returned Apex Auto Detailing from owner-review into the self-improving LPF
design/structure repair loop and assigned Codex as the active worker.

Source: `https://axemobile.widagdos.net/?storefront=envato-elements`
Live demo: `https://apex-auto-detailing-landing-page.pages.dev/`
Local preview during repair: `http://127.0.0.1:4372/`

## Preflight

- `npm run factory:lpf:stopline` passed. Apex is a page rebuild candidate by ticket count, but the rebuild/self-improving loop is acknowledged.
- `npm run qa:lpf-memory-loop -- --ticket docs/factory-orders/2026-06-30-lpf-repair-apex-auto-detailing.md` passed with stamp `400c2861`.
- `npm run qa:lpf-dispatch-preflight -- --ticket docs/factory-orders/2026-06-30-lpf-repair-apex-auto-detailing.md` passed with stamp `eb9f6953`.
- `npm run qa:factory-orders -- docs/factory-orders/2026-06-30-lpf-repair-apex-auto-detailing.md` passed.

## First Repair Pass

- Restored the source-like yellow emphasis in the About heading.
- Restored the source-like "Customer experiences" and FAQ heading accent treatments.
- Changed the pricing intro from centered marketing copy to a source-like two-column heading plus explanatory paragraph.
- Changed FAQ styling from boxed cards toward the source's horizontal-rule accordion rows.
- Brightened and outlined the How It Works media card so the yellow headlight/grille visual slot reads closer to the source.
- Stabilized the `90%` counter so visual evidence cannot capture the enhancement mid-animation as `1%`.

## Footer Return Repair

Owner returned the ticket again because the footer was the most visible remaining
source-fidelity failure: wrong font feel/sizes, missing footer titles, missing
horizontal underline rules, and missing source-like title separation.

Source footer facts confirmed from the captured AxeMobile markup:

- Footer uses a dark `#1B1B1B` to `#111111` gradient band.
- Footer has a compact brand/logo/copy/contact column.
- Footer title set is `Navigation`, `Visit Our Office`, and `Contact Info`.
- Each footer title is immediately followed by a horizontal `hr.border-2`
  underline.
- Navigation links are stacked, and visit/contact blocks are separated.
- Copyright row sits below the footer columns.

Repair applied:

- Rebuilt the footer into a source-like brand/nav/contact grid with mobile stack.
- Added the missing `Navigation`, `Visit Our Office`, and `Contact Info`
  headings.
- Added 2px horizontal underline rules under every footer heading.
- Loaded and used Public Sans / Libre Franklin for the footer typography.
- Set desktop footer headings to about 20px and mobile headings to about 19px.
- Preserved Webdevful-owned Apex identity, copy, and contact details.

## Second Footer Return Repair

Owner returned the ticket again because the footer still did not match the
original design and structure. Root cause: the prior footer repair described the
source topology, but a generic `footer nav` rule had higher/equal practical
priority than the intended `.footer-nav` rules. The rendered result centered the
Navigation title and link list inside the column, left the Contact Us CTA as a
small inline button, collapsed tablet structure too aggressively, and allowed
the active Homepage state to lose its source yellow color after selector
tightening.

Repair applied:

- Scoped footer navigation rules as `.site-footer .footer-nav` so the source
  left-aligned heading, underline, active link, and list share the same edge.
- Changed the brand-column CTA to the source-like full-width 342px outline pill
  with 56px height.
- Adjusted footer brand logo/copy proportions and made brand copy white/bold
  like the source footer block.
- Restored tablet topology: brand spans the first row, Navigation and Contact
  sit in two columns, then mobile stacks below 700px.
- Scoped `.site-footer .footer-nav a.active` so the Homepage active state stays
  acid yellow.
- Added mechanical source-contract checks for the footer selectors and topology
  strings so the same mistake is visible in the next conversion-contract pass.

## Validation

- Product `npm run design:lint`: pass with existing YAML warning only.
- Product `npm run build`: pass.
- Root `python3 tools/check_lpf_conversion_contract.py --project-root /Volumes/WDF-NAS-01/02-Webdevful-Factory/05-Production-Department/Product-Lines/Landing-Page-Line/01-Product-Repos/apex-auto-detailing/repo --capture-dir /Volumes/WDF-NAS-01/04-Projects/Internal-Projects/Codebases/webdevful-astro-main/captures/axemobile-widagdos-net/desktop`: pass with expected source animation/logo evidence warnings.
- Root `npm run qa:lpf-rendered-output -- --url http://127.0.0.1:4372/ --forbid-placeholder --output-dir qa/lpf-rendered-output/apex-auto-detailing-self-improving-local`: pass.
- Root `npm run qa:lpf-rendered-output -- --url http://127.0.0.1:4372/ --forbid-placeholder --output-dir qa/lpf-rendered-output/apex-auto-detailing-footer-repair-local`: pass.
- Root `npm run qa:lpf-visual-diff -- --slug apex-auto-detailing --write-results`: pass for desktop/tablet/mobile, with advisories that section vertical rhythm still needs human review.
- Root `npm run qa:lpf-rendered-output -- --url http://127.0.0.1:4372/ --forbid-placeholder --output-dir qa/lpf-rendered-output/apex-auto-detailing-footer-return-local`: pass from production preview.
- Root `npm run qa:lpf-visual-diff -- --slug apex-auto-detailing --write-results`: pass from production-preview output evidence; low band-correlation advisories remain non-failing.
- Root `npm run factory:lpf:stopline`: pass.
- Root `npm run qa:lpf-memory-loop -- --ticket docs/factory-orders/2026-06-30-lpf-repair-apex-auto-detailing.md`: pass with stamp `400c2861`.
- Root `npm run qa:lpf-dispatch-preflight -- --ticket docs/factory-orders/2026-06-30-lpf-repair-apex-auto-detailing.md`: pass with stamp `eb9f6953`.
- Footer computed-metrics proof: desktop headings render at `20.48px`,
  mobile headings render at `18.88px`, headings use `"Libre Franklin",
  "Public Sans", Inter, Arial, sans-serif`, and footer underline rules render as
  `2px` horizontal borders.
- Second footer return computed proof: Navigation column computes
  `align-items: flex-start`; Navigation heading, rule, list, and active Homepage
  link share the same left edge; brand-column CTA renders `342x56`; active
  Homepage link computes `rgb(255, 243, 38)`; tablet footer renders brand
  full-width above two nav/contact columns.

## Evidence

- Direct local full-page screenshot: `qa/lpf-visual-fidelity/apex-auto-detailing/screenshots/output/demo-desktop-output-direct-2026-06-30.png`
- Standard refreshed output screenshots:
  - `qa/lpf-visual-fidelity/apex-auto-detailing/screenshots/output/demo-desktop-output.png`
  - `qa/lpf-visual-fidelity/apex-auto-detailing/screenshots/output/demo-tablet-output.png`
  - `qa/lpf-visual-fidelity/apex-auto-detailing/screenshots/output/demo-mobile-output.png`
- Rendered-output evidence: `qa/lpf-rendered-output/apex-auto-detailing-self-improving-local/`
- Footer return screenshots:
  - `qa/lpf-visual-fidelity/apex-auto-detailing/footer-repair-2026-06-30/footer-desktop.png`
  - `qa/lpf-visual-fidelity/apex-auto-detailing/footer-repair-2026-06-30/footer-mobile.png`
- Second footer return evidence:
  - `qa/lpf-visual-fidelity/apex-auto-detailing/footer-return-2026-06-30/source-footer-desktop.png`
  - `qa/lpf-visual-fidelity/apex-auto-detailing/footer-return-2026-06-30/current-footer-previous.png`
  - `qa/lpf-visual-fidelity/apex-auto-detailing/footer-return-2026-06-30/footer-desktop-after.png`
  - `qa/lpf-visual-fidelity/apex-auto-detailing/footer-return-2026-06-30/footer-tablet-after.png`
  - `qa/lpf-visual-fidelity/apex-auto-detailing/footer-return-2026-06-30/footer-mobile-after.png`
  - `qa/lpf-visual-fidelity/apex-auto-detailing/footer-return-2026-06-30/footer-desktop-production.png`
  - `qa/lpf-visual-fidelity/apex-auto-detailing/footer-return-2026-06-30/footer-tablet-production.png`
  - `qa/lpf-visual-fidelity/apex-auto-detailing/footer-return-2026-06-30/footer-mobile-production.png`
  - `qa/lpf-rendered-output/apex-auto-detailing-footer-return-local/`
- Footer contract facts:
  - `docs/SOURCE-DESIGN-BRIEF.md`
  - `qa/lpf-source-design-contracts/apex-auto-detailing.json`

## Open Design/Structure Notes

- The service foreground vehicle still differs from the source asset shape:
  source is a compact yellow crossover/SUV PNG; current approved local asset is
  a long side-profile coupe cutout. This should be treated as an asset-slot
  replacement decision, not hidden with CSS.
- Visual-diff passes mechanically, but band-profile correlation remains low.
  Continue the human source/current review before release.
- Codify-back gap: Apex-specific video/parallax/background lessons are still
  partly enforced by section-level checks; generalize these if the next pass
  exposes repeatable failure.

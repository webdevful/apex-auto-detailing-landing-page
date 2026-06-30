# Apex Section 9 FAQ Carousel Runtime Repair - 2026-06-30

Ticket: LPF_REPAIR-apex-auto-detailing-section-9-faq-carousel-runtime-2026-06-30
Agent: Codex: Apex Section 9 FAQ Carousel Runtime Repair / thread codex-app-current-2026-06-30
Product repo: `/Volumes/WDF-NAS-01/02-Webdevful-Factory/05-Production-Department/Product-Lines/Landing-Page-Line/01-Product-Repos/apex-auto-detailing/repo`
Source: AxeMobile by Widagdos, captured at `/Volumes/WDF-NAS-01/04-Projects/Internal-Projects/Codebases/webdevful-astro-main/captures/axemobile-widagdos-net/desktop/page.html`

## Defect

The product flattened the source FAQ section into one custom single-column FAQ accordion. The source FAQ is a Bootstrap-style runtime section with three vertical left-side pill tabs and right-side tab panes, each containing five accordion dropdowns. This was a learning-loop failure for interactive source sections: visible text was preserved, but the source runtime shape was not.

The owner-provided screenshots on Desktop could not be read from this Codex session because `/Users/webdevful/Desktop` returned `Operation not permitted`; the repair used the captured source HTML and browser proof instead.

## Repair

- Replaced the single `faqs` list with `faqCategories`: General, Services & Process, and Pricing & Payment.
- Rebuilt Section 9 as a source-like heading row plus two-column FAQ runtime.
- Added `#faq-tabs` vertical `nav-pills` with `data-bs-toggle="pill"` category buttons.
- Added right-side `.tab-content` panes with three `.accordion` groups and 15 Bootstrap `.accordion-collapse` panels.
- Imported Bootstrap `Tab` and `Collapse` modules from the existing dependency stack and initialized them in `startFaq()`.
- Updated `docs/SOURCE-DESIGN-BRIEF.md` and `qa/lpf-source-design-contracts/apex-auto-detailing.json` so QA rejects future flattened FAQ/tab/carousel substitutions.

## Local Validation

- `python3 -m json.tool qa/lpf-source-design-contracts/apex-auto-detailing.json` passed.
- `npm run design:lint` passed with the existing no-YAML warning and 0 errors.
- `npm run build` passed.
- Root LPF conversion contract passed with WLFS/source-brief/asset-shape/source-typography requirements.
- Root asset deletion guard passed.
- Local rendered-output passed at `http://127.0.0.1:4386/`.
- Local FAQ runtime proof passed:
  - three FAQ category tabs,
  - three accordions,
  - 15 collapse panels,
  - Services tab changes the active pane,
  - second Services collapse opens while the first closes,
  - Pricing tab changes the active pane and keeps its first collapse open.
- Local visual-fidelity gate passed.

## Evidence

- Local rendered-output: `/Volumes/WDF-NAS-01/04-Projects/Internal-Projects/Codebases/webdevful-astro-main/qa/lpf-rendered-output/apex-auto-detailing-section-9-faq-carousel-local`
- Local FAQ runtime screenshot: `/Volumes/WDF-NAS-01/04-Projects/Internal-Projects/Codebases/webdevful-astro-main/qa/lpf-rendered-output/apex-auto-detailing-section-9-faq-carousel-local/section-9-faq-carousel-runtime.png`
- Local FAQ runtime proof JSON: `/Volumes/WDF-NAS-01/04-Projects/Internal-Projects/Codebases/webdevful-astro-main/qa/lpf-rendered-output/apex-auto-detailing-section-9-faq-carousel-local/faq-runtime-proof.json`
- Local visual-fidelity rendered output: `/Volumes/WDF-NAS-01/04-Projects/Internal-Projects/Codebases/webdevful-astro-main/qa/lpf-rendered-output/apex-auto-detailing-section-9-faq-carousel-visual-fidelity-local`
- Product commit: `43d0488` (`Repair Apex FAQ tab accordion runtime`)
- Cloudflare Pages deployment: `https://334a310d.apex-auto-detailing-landing-page.pages.dev`
- Canonical live demo: `https://apex-auto-detailing-landing-page.pages.dev/`
- Public rendered-output: `/Volumes/WDF-NAS-01/04-Projects/Internal-Projects/Codebases/webdevful-astro-main/qa/lpf-rendered-output/apex-auto-detailing-section-9-faq-carousel-public-final`
- Public FAQ runtime screenshot: `/Volumes/WDF-NAS-01/04-Projects/Internal-Projects/Codebases/webdevful-astro-main/qa/lpf-rendered-output/apex-auto-detailing-section-9-faq-carousel-public-final/section-9-faq-carousel-runtime-public.png`
- Public FAQ runtime proof JSON: `/Volumes/WDF-NAS-01/04-Projects/Internal-Projects/Codebases/webdevful-astro-main/qa/lpf-rendered-output/apex-auto-detailing-section-9-faq-carousel-public-final/faq-runtime-proof-public.json`
- Public visual-fidelity rendered output: `/Volumes/WDF-NAS-01/04-Projects/Internal-Projects/Codebases/webdevful-astro-main/qa/lpf-rendered-output/apex-auto-detailing-section-9-faq-carousel-visual-fidelity-public`
- Public storefront funnel sync: passed for `apex-auto-detailing` against `https://apex-auto-detailing-landing-page.pages.dev/`

## Learning Loop

New rule: interactive FAQ, slider, carousel, tab, and accordion sections need runtime-shape verification. A source Bootstrap tab/collapse section must not pass as a static or custom single-list approximation. Browser QA must prove category switching and collapse state changes with source-equivalent DOM selectors and third-party runtime classes.

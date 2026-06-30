# Apex Footer Webdevful Branding Repair

Date: 2026-06-30
Agent: Codex
Ticket: LPF_REPAIR-apex-auto-detailing-footer-webdevful-branding-2026-06-30
Product: Apex Auto Detailing
Live demo: https://apex-auto-detailing-landing-page.pages.dev/

## Owner Return

The owner returned Apex Auto Detailing because the footer did not visibly display Webdevful company branding. The footer is part of the landing-page product marketing surface, so Webdevful attribution must remain visible while Apex Auto Detailing remains the product/customer identity.

## Failure

Before this pass, the footer copyright row rendered:

```text
Copyright © 2026 Apex Auto Detailing. All Rights Reserved.
```

That preserved Apex identity, but it omitted Webdevful provider attribution.

## Repair

Updated `src/pages/index.astro` so the copyright row now renders:

```text
Copyright © 2026 Apex Auto Detailing. Powered by Webdevful. All Rights Reserved.
```

The `Webdevful` text is a visible footer link to `https://webdevful.com` and uses the Apex acid-yellow accent so the brand attribution is clear without disrupting the repaired AxeMobile-style footer layout.

Codified the requirement in:

- `docs/SOURCE-DESIGN-BRIEF.md`
- `qa/lpf-source-design-contracts/apex-auto-detailing.json`

## Local Evidence

Evidence folder:

- `/Volumes/WDF-NAS-01/04-Projects/Internal-Projects/Codebases/webdevful-astro-main/qa/lpf-rendered-output/apex-auto-detailing-footer-webdevful-branding-local`

Browser proof:

```json
{
  "text": "Copyright © 2026 Apex Auto Detailing. Powered by Webdevful. All Rights Reserved.",
  "hasWebdevful": true,
  "linkHref": "https://webdevful.com",
  "linkText": "Webdevful",
  "linkVisible": true,
  "linkColor": "rgb(255, 243, 38)",
  "linkFontWeight": "800"
}
```

## Validation

Passed before product commit/deploy:

```bash
python3 -m json.tool qa/lpf-source-design-contracts/apex-auto-detailing.json
npm run design:lint
npm run build
LPF_REQUIRE_WLFS=1 LPF_REQUIRE_SOURCE_BRIEF=1 LPF_REQUIRE_ASSET_SHAPE=1 LPF_REQUIRE_SOURCE_TYPOGRAPHY=1 LPF_LANDING_PAGE_SLUG=apex-auto-detailing python3 tools/check_lpf_conversion_contract.py --project-root /Volumes/WDF-NAS-01/02-Webdevful-Factory/05-Production-Department/Product-Lines/Landing-Page-Line/01-Product-Repos/apex-auto-detailing/repo --capture-dir /Volumes/WDF-NAS-01/04-Projects/Internal-Projects/Codebases/webdevful-astro-main/captures/axemobile-widagdos-net/desktop
npm run qa:lpf-rendered-output -- --url http://127.0.0.1:4384/ --forbid-placeholder --expect-visible-text "Powered by Webdevful" --output-dir qa/lpf-rendered-output/apex-auto-detailing-footer-webdevful-branding-local
```


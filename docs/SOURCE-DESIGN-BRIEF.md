# Apex Auto Detailing Source Design Brief

## Source Facts

- Source: AxeMobile by Widagdos via Envato Elements.
- Business category: mobile car detailing / auto care / car-wash-detailing.
- Visual grammar: black automotive backdrop, acid-yellow accent, rounded pill CTAs, dark service cards, yellow vehicle hero/service imagery, compact testimonial cards, three pricing cards, FAQ list, and blog thumbnails.
- Typography: source CSS records body text in Public Sans and source heading/button/nav/accordion modules in Libre Franklin. Desktop scale is `h1` 72px, `h2` 48px, `h3` 36px, `h4` 25px, `h5` 22px, `h6` 20px, and `p/a` 18px, with source responsive reductions at 1199/991/768px. Source buttons are 18px Libre Franklin with 13px/30px padding and a 56px pill rhythm.
- Section order: header, hero, feature cards, about, services, why choose, process, reviews, pricing, CTA, FAQ, blog, footer.
- Header structure: source header is a 106px dark band using a centered Bootstrap-style nav list, a compact left logo box, 18px Libre Franklin nav links at 600 weight, active yellow Homepage text with no underline rule, `Services` and `Pages` dropdowns sized to a 220px dark rounded menu, and a large 18px outline `Make Appointment` pill at about 226x56px.
- Footer structure: source footer uses a dark gradient band, three desktop columns, compact brand/logo copy, a full-width outline `Contact Us` pill inside the brand column, `Navigation`, `Visit Our Office`, and `Contact Info` headings, 2px horizontal underline rules under each heading, stacked navigation links, separate visit/contact blocks, and a copyright row. The Navigation heading, underline, active Homepage link, and list items are left-aligned; they are not centered inside the column.
- Dependency modernization: Bootstrap/AOS/jQuery source behavior is rebuilt as static Astro, accessible native FAQ panels, CSS transitions, and visible-by-default reveal-safe content.
- Asset replacement: source template images and logos are not shipped; each photo slot maps to local Unsplash API media and each identity slot maps to WLFS.

## Final Build Mapping

- Header/footer identity: WLFS `Apex Auto Detailing` lockup.
- Hero background: source dashboard/interior background mapped to local `hero-interior.jpg`.
- Yellow vehicle service slot: source yellow crossover PNG mapped to local `yellow-car.jpg`.
- Process quote image: source yellow headlight/grille photo mapped to local `headlight.jpg`.
- Reviews: source six-person testimonial grid adapted to three customer cards with local Unsplash portraits.
- Pricing: source Basic/Premium/Ultimate card structure preserved.
- FAQ: source category tabs adapted into accessible FAQ panels while preserving question coverage.
- Header: source dark band, centered nav topology, 18px Libre Franklin link typography, yellow active state without decorative underline, source-sized dark dropdowns, compact WLFS logo footprint, and a 56px-high outline appointment pill are preserved with one-page anchor targets.
- Typography: section h2 headings, card titles, feature titles, accordion triggers, pricing labels, blog titles, CTA text, and footer headings now preserve source-family hierarchy and source-scale sizes instead of the smaller custom scale that drifted to 12px/14px/16px text.
- Footer: source title hierarchy, Public Sans / Libre Franklin typography, heading sizes, underline rules, three-column desktop layout, tablet brand-full/nav-contact-two-column topology, mobile stacking, full-width brand-column CTA, left-aligned footer navigation column, active yellow Homepage link, and copyright row preserved with Webdevful-owned Apex identity/copy.

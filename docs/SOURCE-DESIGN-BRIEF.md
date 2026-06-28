# Mobile Lift Source Design Brief

## Source Facts

- Source: AxeMobile by Widagdos via Envato Elements.
- Business category: mobile car detailing / auto care / home services.
- Visual grammar: black automotive backdrop, acid-yellow accent, rounded pill CTAs, dark service cards, yellow vehicle hero/service imagery, compact testimonial cards, three pricing cards, FAQ list, and blog thumbnails.
- Typography: source CSS records `h1` at 72/64/56/48px across breakpoints, `h2` at 48/40/36/32px, and body/link text at 18/16px with Public Sans and Libre Franklin.
- Section order: header, hero, feature cards, about, services, why choose, process, reviews, pricing, CTA, FAQ, blog, footer.
- Dependency modernization: Bootstrap/AOS/jQuery source behavior is rebuilt as static Astro, accessible native FAQ panels, CSS transitions, and visible-by-default reveal-safe content.
- Asset replacement: source template images and logos are not shipped; each photo slot maps to local Unsplash API media and each identity slot maps to WLFS.

## Final Build Mapping

- Header/footer identity: WLFS `Mobile Lift` lockup.
- Hero background: source dashboard/interior background mapped to local `hero-interior.jpg`.
- Yellow vehicle service slot: source yellow crossover PNG mapped to local `yellow-car.jpg`.
- Process quote image: source yellow headlight/grille photo mapped to local `headlight.jpg`.
- Reviews: source six-person testimonial grid adapted to three customer cards with local Unsplash portraits.
- Pricing: source Basic/Premium/Ultimate card structure preserved.
- FAQ: source category tabs adapted into accessible FAQ panels while preserving question coverage.

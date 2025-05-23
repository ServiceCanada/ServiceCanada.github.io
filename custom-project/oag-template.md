---
title:
  en: OAG template
  fr: Gabarit BVG
description: Integration 
  
modified: 2025-04-11
lastReviewAbout: Initial implementation of the custom template
componentName: oag-template
sponsor: OAG onboarding team

statusUpdate: 2025-04-11 - Intial creation of this documents

pages:
  examples:
    - title: Home page
      language: en
      path: https://servicecanada.github.io/oag-template/examples/home.html
    - title: Content page
      language: en
      path: https://servicecanada.github.io/oag-template/examples/content.html
    - title: Stacked heading
      language: fr
      path: https://servicecanada.github.io/oag-template/examples/stacked-heading.html

maintenancePlan:
  - due: Next release (for v1.1 or v1.0.1)
    what: Reduce number of includes necessary by adapting GCWeb's own includes
    rational: Having many include overrides could increase the technical debt of this project. By adapting GCWeb Jekyll to leverage different parameters, we'll be able to minimize the need for include overrides.
  - due: Next release (for v1.1 or v1.0.1)
    what: "Add <title> and <xml> elements in SVG markup (ref: https://github.com/wet-boew/GCWeb/blob/master/sites/assets/sig-blk-en.svg?short_path=5922cb9)"
    rational: SVG's should be of high quality

observationNotes:
  - about: Main menu
    observation: Some main menu items do not have sub-menu items, which is not standard for the main menu.

todos:
  - Implement dynamic approach for home page tiles.

output: false
---

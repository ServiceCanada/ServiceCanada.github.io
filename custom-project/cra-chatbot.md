---
title:
  en: CRA chatbot
  fr: Robot de clavardage de l'ARC
description: Integration 
  
modified: 2024-01-15
lastReviewAbout: When moving code from freestyle to github repository
componentName: cra-chatbot
sponsor: Mathieu Bergeron, CRA 

pages:
  examples:
    - title: Chat with Charlie chatbot
      language: en
      path: https://servicecanada.github.io/cra-chatbot/demos/index.html
    - title: Clavardez avec Charlie
      language: fr
      path: https://servicecanada.github.io/cra-chatbot/demos/index-fr.html

maintenancePlan:
  - due: First release (for v1.0)
    what: Apply SRI to the webchat javascript
    rational: Considering this is an external, non-gc CDN, we need to ensure the integrity of those files
  - due: Next release (v1.1 or v1.0.1)
    what: Update to latest webchat v4.13.0 (released on 2021-04-05)
    rational: According to change log, there is a lot of accessibility fixes since the version 4.9.1.
  - due: Next release or two (v1.1 +)
    what: Investigate and report for the replacement option for webchat.
    rational: The webchat has not been updated since 2021 and the Github repository seems to be stale.
  - due: Next release or two (v1.1 +)
    what: Map the domain name "asuzewebsite" into a valid Canada.ca subdomain.
    rational: Improve the trust and clearly identify that is content under our control
  - due: To be determined
    what: Code optimization
    rational: See informal todos

observationNotes:
  - about: CRA chatbot token
    observation: Return a JSON file containing what its look like to be a JWT and a JWS

todos:
  - Minimizing the need of adding custom HTML code in every individual page using the chat bot. Suggestoin: Manage that HTML pattern centrally in teh JS or via an HTML assets. Ref.
  - Optimizing

output: false
---

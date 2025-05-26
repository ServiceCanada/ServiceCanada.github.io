---
title:
  en: Search UI
  fr: Interface de recherche
description: Provide MWS pages with the proper JS and CSS assets to achieve a working search page with the vendor's (Coveo) technology called Headless.
  
modified: 2025-05-22
lastReviewAbout: Prior to release v1.6.0
componentName: search-ui
sponsor: Francis Gorman, Principal Publisher, ESDC 

statusUpdate: 2025-05-22 - Working on release v1.6.0, which doesn't include 1 item from the maintenance plan (postponed to next release)

pages:
  examples:
    - title: List of all search page examples
      language: en
      path: https://servicecanada.github.io/search-ui/index.html
    - title: Sample basic search page
      language: en
      path: https://servicecanada.github.io/search-ui/test/srb-en.html
    - title: Sample advanced search page
      language: en
      path: https://servicecanada.github.io/search-ui/test/sra-en.html
    - title: Sample contextual search page
      language: en
      path: https://servicecanada.github.io/search-ui/test/src-en.html
    - title: Exemple de page de résultats de la recherche (base)
      language: fr
      path: https://servicecanada.github.io/search-ui/test/srb-fr.html
    - title: Exemple de page de résultats de la recherche (avancée)
      language: fr
      path: https://servicecanada.github.io/search-ui/test/sra-fr.html
    - title: Exemple de page de résultats de la recherche (contextuelle)
      language: fr
      path: https://servicecanada.github.io/search-ui/test/src-fr.html

maintenancePlan:
  - due: "Next release (was for: v1.6.0, but postponed to 1.6.1 or 1.7.0)"
    what:
      - "Must: Clean outdated search query from the local storage variable `__coveo.analytics.history`. At minimum an expiry date/time constraint must be applied."
    rational: "Postponing to next release MAX, since the search vendor is still working on a viable solution which requires management approval on our side (through: https://jtickets.atlassian.net/browse/SR-543)"
  - due: Next release or two (v1.6 +)
    what: Start to add automated testing for the search-ui code functional aspect. This could be unit testing or functiona testing with pupetteer.
    rational: There is no functional testing, only a code linter and basic syntax checker.
  - due: Release v1.6.0 - COMPLETED
    what:
      - "Create demos/test that are illustrating all functionality. Like a demos that show all the possible configurable option."
      - "Manage API key over a session storage where it allow the tester to enter that key manually in a separate page"
    rational: During the review of v1.4, we found that change/addition was made to un-demoed feature.
  - due: Release v1.5.0 or v1.4.1 - COMPLETED
    what: Enforce the line ending for CSS build to be linux line ending, especially when generating the distribution files
    rational: Ensure that the windows build, linux build or mac build do produce the same binary file.

todos:
  - Refactor the code to make it easier to understand it functional aspect
  - Manage template centrally in a way that is applying change are intituitive and easierand make if easier to configure/update
  - Remove the need for having a CSS file to be handled by GCWeb instead!
  - Add missing pieces such as "error message", "no result" and "did you mean" into our reference implementation as an example
  - Add Expected output on test pages (HTML) and use Jekyll highlights
  - "**to validate, reported as completed** Add includes of JS (src) files in a baked in Jekyll variables instead of hardcoded"
  - Align search pages with new GCWeb template and/or define new GCWeb templates
  - Ensure no section or heading or any element with semantic is added alone/empty on the page 
  - Create search template specific styles (.page-type-search), to get rid of overusage of .h3 class for example
  - "Leverage wb core features instead of reinving the wheel, such as for language of page and dates. For dates, native JS functions could be leveraged such as: toLocaleDateString"
  - "Improve caching of variable that are used multiple times in the script, such as: window.location, then window.location.pathname"
  - Revisit how dates are handled for output formats (need an array of months?)
  - Make IDs configurable for "suggestion", "result-list", "result-link", "query-summary", "pager"
  - Revisit customEvent to potentially be scoped to the search-ui element instead of document
  - Document customEvent with further details
  - Improve warning message when Headless doesn't load
  - "`numberOfPages: 9` and `automaticallyCorrectQuery: false` should be configurable through parameters"
  - "**to validate, reported as completed** Investigate Pagination styles when testing from GitHub"
  - "**to validate, reported as completed** Investigate #wb-land focus on Advanced search"
  - "COMPLETED: Potentially come up with an easier way to test locally"
  - "COMPLETED: Finish proper development of Suggestion box (type-ahead)"
  - "COMPLETED: Improve the form code to not rely on an action that points to an anchor for a dynamically added element, which doesn't exist on the page prior to JS"
  - "COMPLETED: Revisit the need to search for postscript and rich text documents (ps and rtf. Are they needed? What's the usecase?"
  - "COMPLETED: Revisit the window.location.origin.startsWith( 'file://' ) condition"

output: false
---

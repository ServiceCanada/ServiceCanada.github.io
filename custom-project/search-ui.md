---
title:
  en: Search UI
  fr: Interface de recherche
description: Provide MWS pages with the proper JS and CSS assets to achieve a working search page with the vendor's (Coveo) technology called Headless.
  
modified: 2024-01-15
lastReviewAbout: Prior the release of v1.4.0
componentName: search-ui
sponsor: Francis Gorman, Principal Publisher, ESDC 

pages:
  examples:
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
  - due: Next release (for v1.5)
    what: Create demos/test that are illustrating all functionality. Like a demos that show all the possible configurable option.
    rational: During the review of v1.4, we found that change/addition was made to un-demoed feature.
  - due: Next release (for v1.5.0 or v1.4.1)
    what: Enforce the line ending to be linux line ending, especially when generating the distribution files
    rational: Ensure that the windows build, linux build or mac build do produce the same binary file.
  - due: Next release or two (v1.5 +)
    what: Start to add automated testing for the search-ui code functional aspect. This could be unit testing or functiona testing with pupetteer.
    rational: There is no functional testing, only a code linter.

todos:
  - Refactor the code to make it easier to understand it functional aspect
  - Manage template centrally in a way that is applying change are intituitive and easierand make if easier to configure/update
  - Remove the need for having a CSS file to be handled by GCWeb instead!
  - Add missing pieces such as "error message", "no result" and "did you mean" into our reference implementation as an example
  - Potentially come up with an easier way to test locally
  - Add Expected output on test pages (HTML) and use Jekyll highlights
  - Finish proper development of Suggestion box (type-ahead)
  - "**to validate, reported as completed** Add includes of JS (src) files in a baked in Jekyll variables instead of hardcoded"
  - Align search pages with new GCWeb template and/or define new GCWeb templates
  - Ensure no section or heading or any element with semantic is added alone/empty on the page 
  - Improve the form code to not rely on an action that points to an anchor for a dynamically added element, which doesn't exist on the page prior to JS
  - Create search template specific styles (.page-type-search), to get rid of overusage of .h3 class for example
  - Leverage wb core features instead of reinving the wheel, such as for language of page and dates. For dates, native JS functions could be leveraged such as: toLocaleDateString
  - Improve caching of variable that are used multiple times in the script, such as: window.location, then window.location.pathname
  - Revisit how dates are handled for output formats (need an array of months?)
  - Make IDs configurable for "suggestion", "result-list", "result-link", "query-summary", "pager"
  - Revisit customEvent to potentially be scoped to the search-ui element instead of document
  - Document customEvent
  - Improve warning message when Headless doesn't load
  - "`numberOfPages: 9` and `automaticallyCorrectQuery: false` should be configurable through parameters"
  - Revisit the need to search for postscript and rich text documents (ps and rtf. Are they needed? What's the usecase?
  - Revisit the "window.location.origin.startsWith( 'file://' )" condition
  - "**to validate, reported as completed** Investigate Pagination styles when testing from GitHub"
  - "**to validate, reported as completed** Investigate #wb-land focus on Advanced search"

output: false
---

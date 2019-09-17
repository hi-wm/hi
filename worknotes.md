---
title: Daily Worknotes
---

The purpose of this document is to keep a running record of my daily activities at [Horizontal Integration](http://horizontalintegration.com)  
This is mostly notes related to ongoing projects

> 9/17/19

* cw 6472 Chapter Component - add spacing to match spec `margin-bottom: 4rem;`
* cw 6462 Update search field to match specs - set max-width according to spec
* cw 6172 Update image specs for download asset component - generated new set of images and updated component markup

> 9/16/19

* cw 8239 Lazy loading - updated waypoint offset from 66% to 80%, elements above the fold should appear more readily
* cw 8266 Add button to Insights page render

> 9/13/19

* cw 8046 Header Utility Menu Display Issue - had to define width for .header-utilityNav item; was breaking to a new line
* cw 6058 Subscribe CTA - broken ::before && ::after - had to define pseudo element translateX positioning for devices below XS breakpoint
* cw 6462 Hero Search Input Size - updated width of search field, had initially placed the fix in the wrong file... specificity broke the 'fix', now it is fixed
* cw 7186 Multimedia Search Results Page - fix from yesterday has been pushed to QA, but the modal open mask covers the entire page now. CoveoSearchInterface put a z-index on the wrapper which overrode the modal z-index.

> 9/12/19

* cw 7813 Hero Page Title Card - Fixed min-height for event of no button (an optional element)
* cw 7186 Multimedia Search Results Page - Continues playing on modal close fix;

```podcasts were broken because BED did not use the unique classnames set for the two different podcast sources
videos were broken because Coveo loads after the video modal JS is init, added: if (window.YT) { $(window).trigger('youTubePlayerApiReady'); }; && if (window.VidyardV4) { $(window).trigger('vidyardPlayerApiReady'); }; <-- triggers if element is found```

> 9/11/19

> Target class of '.coveo-query-summary-cancel-last' and change text to 'Try a different search term'

```$('.coveo-query-summary-cancel-last').text('Try a different search term');```

* cw 8047 Design and Implement CoveoQuerySummary CSS
* cw 8068 Hero Image & Video Cards SM / XS breakpoint fix
* cw 7813 Hero Page Title Card Image Size(s) fix

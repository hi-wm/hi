---
title: William Harrison - Front End Developer at Horizontal Integration
---

The purpose of this document is to keep a running record of my daily activities at [Horizontal Integration](http://horizontalintegration.com)  
You will find some notes related to ongoing projects as well as Frontend Development resources that have proven useful 

> 9/17

`<!-- Resources -->`

## Sitecore Experience Accelerator

[Custom Component Build - Part 1 - Introduction](https://www.nishtechinc.com/en/Blog/2018/November/Nuptial-Experiment-Introduction)

[Custom Component Build - Part 2 - Milestone 1](https://www.nishtechinc.com/en/Blog/2018/November/Nuptial-Experiment-Part-2)

[Custom Component Build - Part 3 - Milestones 2 & 3](https://www.nishtechinc.com/en/Blog/2018/November/Nuptial-Experiment-Part-3)

[Custom Component Build - Part 4 - Final Thoughts](https://www.nishtechinc.com/en/Blog/2018/November/Nuptial-Experiment-Final-Thoughts)

`<!-- Work Items -->`

* cw 6172 Update image specs for download asset component - generated new set of images and updated component markup
* cw 6462 Update search field to match specs - set max-width according to spec

> 9/16

`<!-- Resources -->`

## Sitecore Experience Accelerator

[Overview Part 1](https://www.velir.com/blog/2017/10/16/tour-sitecore-experience-accelerator-sxa-part-1)

[Overview Part 2](https://www.velir.com/blog/2017/10/16/tour-sitecore-experience-accelerator-sxa-part-2)

[Some Tips & Tricks](https://www.sidewalk.be/articles/the-sitecore-sxa-journey-discover-tips-and-tricks-when-implementing-an-sxa-website)

[Video Tutorial Walkthrough](https://www.reddit.com/r/sitecore/comments/bdihvd/sitecore_sxa_tutorials_sxa_1_8_full_site_step_by/)

[Add data attributes to renderings](http://blog.martinmiles.net/post/how-to-add-id-and-data-attributes-to-a-rendering-variant-in-sxa)

`<!-- Work Items -->`

* cw 8239 Lazy loading - updated waypoint offset from 66% to 80%, elements above the fold should appear more readily
* cw 8266 Add button to Insights page render

> 9/13

`<!-- Work Items -->`

* cw 8046 Header Utility Menu Display Issue - had to define width for .header-utilityNav item; was breaking to a new line
* cw 6058 Subscribe CTA - broken ::before && ::after - had to define pseudo element translateX positioning for devices below XS breakpoint
* cw 6462 Hero Search Input Size - updated width of search field, had initially placed the fix in the wrong file... specificity broke the 'fix', now it is fixed
* cw 7186 Multimedia Search Results Page - fix from yesterday has been pushed to QA, but the modal open mask covers the entire page now. CoveoSearchInterface put a z-index on the wrapper which overrode the modal z-index.

> 9/12

`<!-- Work Items -->`

* cw 7813 Hero Page Title Card - Fixed min-height for event of no button (an optional element)
* cw 7186 Multimedia Search Results Page - Continues playing on modal close fix;

```podcasts were broken because BED did not use the unique classnames set for the two different podcast sources
videos were broken because Coveo loads after the video modal JS is init, added: if (window.YT) { $(window).trigger('youTubePlayerApiReady'); }; && if (window.VidyardV4) { $(window).trigger('vidyardPlayerApiReady'); }; <-- triggers if element is found```

> 9/11

Target class of '.coveo-query-summary-cancel-last' and change text to 'Try a different search term'

$('.coveo-query-summary-cancel-last').text('Try a different search term');

`<!-- Work Items -->`

* cw 8047 Design and Implement CoveoQuerySummary CSS
* cw 8068 Hero Image & Video Cards SM / XS breakpoint fix
* cw 7813 Hero Page Title Card Image Size(s) fix

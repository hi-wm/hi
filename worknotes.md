---
title: Daily Worknotes
---

The purpose of this document is to keep a running record of my daily activities at [Horizontal Integration](http://horizontalintegration.com)  
This is mostly notes related to ongoing projects

<details>
<summary>2019</summary>
<details>
<summary>September</summary>
<br>

> 9/19

*Closed out remaining cw tickets.*
*Working on mwt full time now.*

* mwt 185 - RTE Text Formatting - BED refused a classname from our markup which broke body copy styling. Additionally, styling was needed for `<strong>` text. I did that. Like this:

```scss
p {
    margin-top: 11px;
    strong {
        font-family: Helvetica Neue LT W01_83 Hv Ex,Helvetica Neue,Helvetica,Arial,sans-serif;
        text-transform: uppercase;
    }
}
```

* mwt 182 / 184 - Extra Whitespace - BED had reused a classname on an element which resulted in strange behavior. I added a new classname and relevant styling, but once implemented by BED, Sitecore adds spaces in a `<div>` with no content and the `:empty` pseudo-selector was unable to work. Thankfully, BED *was* able to write some logic that will conditionally render the `<div>` if there is content for it. Also had update the name of a file, because some FED had not done that causing the test page to be broken.

```scss
.flex-content-feature-accordion {
        display: flex;
        width: 100%;
        order: 3;
        &:empty {
            display: none;
        }
    }
```

* mwt 35 Tabbed Carousel - pushed yesterdays changes to dev

> 9/18

* mwt 35 Tabbed Carousel - this component (based off of [slick slider](https://kenwheeler.github.io/slick/)) was intended to be used stand-alone, but of course QA found a reason to use it twice on a page (maybe there is a genuine use case for this?). Needless to say, how the component was initally set up was targeting a class instead of a unique ID. Adding a data-target was able to solve the problem. The changes made are as follows:

*these were the changes made to the JavaScript*

```javascript
...
var $this = $(this); // this line already existed
var target = $this.data('target');

// inside of the slick slider settings

asNavFor: '#' + target,

// targets the unique id

...$('#' + target).slick...
```

*and these were the changes made to the HTML files*

```html
<div class="innovations-tabbed-view__items" id="1"> <!-- added the id -->
```

```html
<section class="innovations-tabbed-view" data-target="1"> <!-- added the data-target -->
```

> 9/17

* cw 6472 Chapter Component - add spacing to match spec `margin-bottom: 4rem;`
* cw 6462 Update search field to match specs - set `max-width` according to spec
* cw 6172 Update image specs for download asset component - generated new set of images and updated component markup

> 9/16

* cw 8239 Lazy loading - updated waypoint offset from 66% to 80%, elements above the fold should appear more readily
* cw 8266 Add button to Insights page render

> 9/13

* cw 8046 Header Utility Menu Display Issue - had to define width for .header-utilityNav item; was breaking to a new line
* cw 6058 Subscribe CTA - broken `::before` && `::after` - had to define pseudo element translateX positioning for devices below XS breakpoint
* cw 6462 Hero Search Input Size - updated width of search field, had initially placed the fix in the wrong file... specificity broke the 'fix', now it is fixed
* cw 7186 Multimedia Search Results Page - fix from yesterday has been pushed to QA, but the modal open mask covers the entire page now. CoveoSearchInterface put a `z-index` on the wrapper which overrode the modal `z-index`.

> 9/12

* cw 7813 Hero Page Title Card - Fixed min-height for event of no button (an optional element)
* cw 7186 Multimedia Search Results Page - Continues playing on modal close fix;

*podcasts were broken because BED did not use the unique classnames set for the two different podcast sources
videos were broken because Coveo loads after the video modal JS is init, added:*

```javascript
if (window.YT) { $(window).trigger('youTubePlayerApiReady'); }; &&
if (window.VidyardV4) { $(window).trigger('vidyardPlayerApiReady'); };
```

*triggers if element is found*

> 9/11

*Target class of '.coveo-query-summary-cancel-last' and change text to 'Try a different search term'*

```javascript
$('.coveo-query-summary-cancel-last').text('Try a different search term');
```

* cw 8047 Design and Implement CoveoQuerySummary CSS
* cw 8068 Hero Image & Video Cards SM / XS breakpoint fix
* cw 7813 Hero Page Title Card Image Size(s) fix

</details>
</details>
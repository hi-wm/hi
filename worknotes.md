---
title: Daily Worknotes
---

The purpose of this document is to keep a running record of my daily activities at [Horizontal](http://horizontalintegration.com)  
This is mostly notes related to ongoing projects

<details>
<summary>2019</summary>
<details>
<summary>September</summary>
<br>

9/24

*mwt merged repos, built and deployed the project in its current state. Lots of bugs knocked out, focus shifted to PIP (Product Information Page) Component production*

* mwt 99 - pip gallery component - Another new component build based off of the Sketch file provided by UX. Having become more familiar with the project structure, this was an easier build, but there were some interesting trip ups provided by flexbox. The major hiccups were uneven columns, an image that spanned 2 columns and rows, and gradient overlays. The following ```HTML``` and ```SCSS``` is how that was handled. Built for mobile first, the ```SCSS``` is what really drives the magic here. I hope the clients dev team doesn't mind my ```@mixin``` here because it helped to make the code more DRY.

```scss
@import ''; // link removed to preserve client anonymity
@mixin overlay-base {
    content: '';
    position: absolute;
    width: 100vw;
    background: -moz-linear-gradient(top, rgba(0,0,0,0) 80%, rgba(0,0,0,0.95) 100%); /* FF3.6+ */
    background: -webkit-gradient(linear, left top, left bottom, color-stop(0%,rgba(0,0,0,0.95)), color-stop(100%,rgba(0,0,0,0))); /* Chrome,Safari4+ */
    background: -webkit-linear-gradient(top, rgba(0,0,0,0) 80%,rgba(0,0,0,0.95) 100%); /* Chrome10+,Safari5.1+ */
    background: -o-linear-gradient(top, rgba(0,0,0,0) 80%,rgba(0,0,0,0.95) 100%); /* Opera 11.10+ */
    background: -ms-linear-gradient(top, rgba(0,0,0,0) 80%,rgba(0,0,0,0.95) 100%); /* IE10+ */
    background: linear-gradient(to bottom, rgba(0,0,0,0) 80%,rgba(0,0,0,0.95) 100%); /* W3C */
}
.pip-gallery {
    width: 100vw;
    display: flex;
    position: relative;
    flex-wrap: wrap;
    @media screen and (min-width: $tablet-min) {
        flex-wrap: nowrap;
    }
    
    &__large-image {
        flex: 0 0 100vw;
        order: 1;
        @media screen and (min-width: $tablet-min) {
            flex: 0 0 66.66vw;
        }
        
        & img {
            width: 100%;
            z-index: -1;
        }
        
        &__overlay::after {
            @include overlay-base;
            left: 0;
            top: 0;
            height: 33.33%;
            @media screen and (min-width: $tablet-min) {
                height: 100%;
                width: 66.66vw;
            }
        }
    }
    
    &__small-image {
        flex: 0 0 100vw;
        flex-direction: unset;
        order: 2;
        @media screen and (min-width: $tablet-min) {
            flex: 0 0 33.33vw;
        }
        
        &__overlay-top::after {
            @include overlay-base;
            right: 0;
            top: 0;
            height: 67%;
            @media screen and (min-width: $tablet-min) {
                height: 50%;
                width: 33.33vw;
            }
        }
        &__overlay-bottom::after {
            @include overlay-base;
            right: 0;
            bottom: 0;
            height: 100%;
            @media screen and (min-width: $tablet-min) {
                height: 50%;
                width: 33.33vw;
            }
        }
        
        & img {
            width: 100%;
            z-index: -1;
        }
    }
}
```

```html
<section class="pip-gallery">
    <div class="pip-gallery__large-image">
        <div class="pip-gallery__large-image__overlay">
            <img src="/pip-gallery-1.png">
        </div>
    </div>
    <div class="pip-gallery__small-image">
        <div class="pip-gallery__small-image__overlay-top">
            <img src="/pip-gallery-2.png">
        </div>
        <div class="pip-gallery__small-image__overlay-bottom">
            <img src="/pip-gallery-3.png">
        </div>
    </div>
</section>
```

---

9/23

* mwt 91 - hero header component - UPDATE - I had this reviewed internally before passing it on. I neglected that this was a new component that needed to be fleshed out by BED before a PR was submitted, so my PR got abandoned ¯\_(ツ)_/¯ Not a big deal, more a matter of me learning the workflow a bit. BED got this knocked out and all looks good.

---

9/20

*mwt internal team having trouble with build and deployment*

* mwt 91 - hero header component - This is a new component build based off of a Sketch file provided by UX. I have had some trouble with the overall structure of the project, would probably have been useful to spend some time speaking with a dev who has worked on the project before just diving in. Exported and cleaned up an ```SVG```, built out ```HTML``` and ```SCSS``` for the component. Would like someone to review before I submit a PR. Can hopefully get that this Monday.

---

9/19

*Closed out remaining cw tickets.*  
*Working on mwt full time now.*

* mwt 185 - RTE Text Formatting - BED refused a classname from our markup which broke body copy styling. Additionally, styling was needed for `<strong>` text. I did that. Like this:

```scss
p {
    margin-top: 11px;
    strong {
        font-family: Helvetica Neue LT W01_83 Hv Ex,Helvetica Neue,Helvetica,Arial,sans-serif;
        // had to change the above to a variable *$helvetica83* that had been declared in a separate file
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

---

9/18

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

---

9/17

* cw 6472 Chapter Component - add spacing to match spec `margin-bottom: 4rem;`
* cw 6462 Update search field to match specs - set `max-width` according to spec
* cw 6172 Update image specs for download asset component - generated new set of images and updated component markup

---

9/16

* cw 8239 Lazy loading - updated waypoint offset from 66% to 80%, elements above the fold should appear more readily
* cw 8266 Add button to Insights page render

---

9/13

* cw 8046 Header Utility Menu Display Issue - had to define width for .header-utilityNav item; was breaking to a new line
* cw 6058 Subscribe CTA - broken `::before` && `::after` - had to define pseudo element translateX positioning for devices below XS breakpoint
* cw 6462 Hero Search Input Size - updated width of search field, had initially placed the fix in the wrong file... specificity broke the 'fix', now it is fixed
* cw 7186 Multimedia Search Results Page - fix from yesterday has been pushed to QA, but the modal open mask covers the entire page now. CoveoSearchInterface put a `z-index` on the wrapper which overrode the modal `z-index`.

---

9/12

* cw 7813 Hero Page Title Card - Fixed min-height for event of no button (an optional element)
* cw 7186 Multimedia Search Results Page - Continues playing on modal close fix;

*podcasts were broken because BED did not use the unique classnames set for the two different podcast sources
videos were broken because Coveo loads after the video modal JS is init, added:*

```javascript
if (window.YT) { $(window).trigger('youTubePlayerApiReady'); }; &&
if (window.VidyardV4) { $(window).trigger('vidyardPlayerApiReady'); };
```

*triggers if element is found*

---

9/11

*Target class of '.coveo-query-summary-cancel-last' and change text to 'Try a different search term'*

```javascript
$('.coveo-query-summary-cancel-last').text('Try a different search term');
```

* cw 8047 Design and Implement CoveoQuerySummary CSS
* cw 8068 Hero Image & Video Cards SM / XS breakpoint fix
* cw 7813 Hero Page Title Card Image Size(s) fix

</details>
</details>
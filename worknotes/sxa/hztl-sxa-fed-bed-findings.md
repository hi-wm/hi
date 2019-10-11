<br />  

[Lixil-Related FED Findings](https://horizontal.atlassian.net/wiki/spaces/LWTA/pages/800718849/Lixil+-+Bootstrap+SXA+Learnings+and+Findings)
 
[Lixil-Related BED Findings](https://horizontal.atlassian.net/wiki/spaces/LWTA/pages/802652352/SXA+POC+Findings)
 
[Even more Lixil-Related SXA Notes](https://horizontal.atlassian.net/wiki/spaces/LWTA/pages/814514694/SXA)
 
# Some other notes for UX/Content teams:
 
## What is SXA?
SXA (Sitecore Experience Accelerator) is a module developed by Sitecore and comes with Sitecore 9.0 and up.
[Features](https://doc.sitecore.com/users/sxa/17/sitecore-experience-accelerator/en/introducing-sitecore-experience-accelerator.html)
Tenants and sites (Set up tenants, multisites, security roles)
Toolbox (reusable renderings you can drag and drop)
Grid and column layout (ability to configure rows and columns)
Pluggable themes (enable available themes or use your own custom brand themes)
Page designs and partial designs (define presentation for pages and partials)
Creative Exchange (ability to sync themes and content back to Sitecore environment)
Share content and presentation (allows you to control content from one central location and shared across sites)
Asset Optimizer (enable optimization on assets such as CSS/JS for improved site performance)
Data modeling (ability to model and access data via JSON API)
 
## Why should we use it?
SXA helps separate structure from design so designers, developers, and content authors can work in parallel to build, deploy, and maintain sites.
i.e. 
BED configures data and templates while
FED works on theming
Content author can enter content during this time and/or
UXD could assemble wireframes for initial layout and components
 
## How have we used it on Lixil?
We’ve spun up a base site with a base theme that is rolled out to all brand themes. Each brand theme then has its own custom brand CSS, which also inherits from the base theme. All components are also available across sites. Lixil is multisite and will be comprised of 4-5 brand sites down the road.
 
## What challenges has it solved for us?
Faster delivery - Using OOTB components reduces time of development.
Reusability - Has sped up production via reuse of components, layouts and templates. 
Commerce - Using SXA Commerce Storefront theme which speeds up development as well.
 
## What challenges do we still face from a FED perspective?
OOTB components don’t always come with all the features we need, so we have create and rely on variants to extend the rendering. This requires some extra dev (BED config & export, FED UI work).
Requires a lot of collaboration and communication between all teams to make decisions, implement, and validate.
Things that are not available:
Variant creation for carousel, accordion, 
Full card anchors (we’re just javascript to make it so)
OOTB SXA video component can’t be played in a popup
OOTB SXA navigation is restrictive so header/footer is custom
Still on Bootstrap 3.3.4 because Commerce Storefront does not support Bootstrap 4.
Encountered a lot of presentation/layout issues due to OOTB SXA component structure
OOTB code structure does not fully conform to Bootstrap grid in places.
Generating double .rows, too many chained classes, etc.
Issues with row splitters and column splitters getting too nested.
Must be really careful during component construction to not deeply nest items or,
Carefully tweak CSS to account for code structure that cannot be modified
Best Practices:
Start with a bare bones theme.
Avoid using row splitters and column splitters. Add components directly to a placeholder.
Use containers if more than one components needs to be added for a section like multiple/repeating promo cards.
For items inside .container > .row, make sure they include the bootstrap grid classes where necessary i.e. col-xs-12 col-md-6 col-lg-3
Make sure the component structure follows Bootstrap grid structure. i.e. 
```html
<div class=“container”><div class=“row”><div class=“col-xs-12”>…</div></div></div>
```
Add css class names to variants so FED can use this css to style them. Follow component naming convention as defined in functional requirements for consistency.
 
## What does UX need to know to get started?
Kathryn Deming and Lisa Albinson from the Minneapolis UXD team are great resources.
Get familiar with [OOTB components/rendering variants](https://doc.sitecore.com/users/sxa/17/sitecore-experience-accelerator/en/the-sxa-renderings-and-rendering-variants.html).
Check out the Lixil component requirements. Many are based on OOTB components which we’ve created variants for.  [Check it out](https://horizontal.atlassian.net/wiki/spaces/LWTA/pages/811599681/Components+Overview)!
 
## Resources
[Official Sitecore SXA Documentation](https://doc.sitecore.com/developers/sxa/17/sitecore-experience-accelerator/en/index-en.html)
[Lixil Content Guides](https://horizontal.atlassian.net/wiki/spaces/LWTA/pages/814711176/Release+Notes+Content+Guides )

```Note: Use the links in the left hand nav (instead of body conten on this page) to see individual content guides per component```
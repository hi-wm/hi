<summary>Part 4 - Placeholders and Placeholder Restrictions</summary>
<br />  

Link to YouTube video for this section [SXA Rendering Variants Part 4 - Placeholders and Placeholder Restrictions](https://youtu.be/deeYre6u9_E)

*Let's talk about placeholders*

Speaking of *Rendering Variants*, here's some information about how to add a *Placeholder* for your content authors. Find one of your *Rendering Variants* and ```Insert > Placeholder```. This will insert a *Placeholder* into your rendering variant. Now your rendering variant will have a placeholder in it. Once in the *Experience Editor*, the *Placeholder* will allow you to drop additional components into your rendering variant.

Continuing on, we are presented with the idea of a blog and the presenter would like to add any tags associated with each post to appear under the title of the post and have it render in a list. Adding a *Placeholder* to the rendering variant allows you to drop in a taxonomy component that will render the tags, but the default way sitecore treats this placeholder will cause the tags to be rendered from the first list item then applied to all of the other posts in the render. To get the unique tags for each of the different posts, the *Placeholder* needs to have an additional setting applied, *Switch component context to currently rendered item*.

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Placeholders-Component-Context.png "SXA Rendering Variants Placeholders and Restrictions, get unique elements rendered in your placeholders by checking this box")
*SXA Rendering Variants Placeholders and Restrictions, get unique elements rendered in your placeholders by checking this box*

Above the checkbox you will notice a *Placeholder Key*. It is important to define a name for this key so that it can be targeted when defining a placeholder restriction. Give the *Placeholder Key* a name.   *Placeholder Settings* ```sitecore > *tenant_name* > *site_name* > Presentation > Placeholder Settings``` is home to the placeholder settings. To define a placeholder restriction, right-click *Placeholder Settings* then ```Insert > Placeholder```. Give your new placeholder a name (you may need to give it a name with a wildcard * to capture all instances of the placeholder you are targeting i.e. blog*). In the content window of the new placeholder, under *Allowed Controls* you can set what components are allowed for the placeholder. After defining what components are allowed for the placeholder, check in the *Experience Editor* and you will find components that are not allowed are unable to be placed within the placeholder.

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Placeholders-Restricted-Components.png "SXA Rendering Variants Placeholders and Restrictions, good luck getting a restricted component into that placeholder")
*SXA Rendering Variants Placeholders and Restrictions, good luck getting a restricted component into that placeholder*

That's great, but let's define some more restrictions. Within the Blog Posts Tag Placeholder definition, we should add a *Rules* to only render the related tags for posts with tags.

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Placeholders-Rule-Definition.png "SXA Rendering Variants Placeholders and Restrictions, to conditionally render something, add a rule")
*SXA Rendering Variants Placeholders and Restrictions, to conditionally render something, add a rule*

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Placeholders-Rule-Definition-Wizard.png "SXA Rendering Variants Placeholders and Restrictions, here is the rule definition wizard")
*SXA Rendering Variants Placeholders and Restrictions, here is the rule definition wizard*

Here is a link to the sitecore documentation about how to [Set Placeholder Restrictions](https://doc.sitecore.com/developers/sxa/17/sitecore-experience-accelerator/en/set-placeholder-restrictions.html)  

And here is another link from a sitecore MVP about the [multiple ways of using SXA placeholder settings](https://www.linkedin.com/pulse/sitecore-tip-22-multiple-ways-using-sxa-placeholder-emmerzaal/)
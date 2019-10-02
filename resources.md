---
title: Frontend Development Resources
---

Here are some Frontend Development resources that have proven useful

## Sitecore Experience Accelerator

<details>
<summary>Tenant and Site Creation</summary>

Right-click on ```Content``` node and a dropdown menu will appear. From here, follow ```Insert > Tenant```. If your site will have numerous sub-sites, you can either create a ```Tenant Folder``` which can house multiple ```Tenants```, or you can create a ```Tenant``` which can also house multiple ```Tenants```. Each Tenant has a set of Data Templates, which are stored in the Templates section which you can share within a Tenant. You can also share Rendering Variants, Themes, and Media. Think first about how your organizational structure should be reflected, then click the button to make the thing.

When you right click on ```Content``` then select ```Insert > Tenant``` a Tenant creation wizard will appear. It's magical. It is a single-step wizard, so it's not really that magical. But you should give your Tenant a name according to the naming conventions you have agreed upon with your client and or team, and additionally, you can select which of the Modules you may need for your Tenant.

Once you have created your Tenant, it will appear along the following path; ```sitecore > Content > *new_tenant_you_created*```. If you select your tenant, you will be able to explore all of the relevant paths for your tenant, available modules, shared site information. Once you have created this tenant, you will notice that in some places along your sitecore folder tree, that some new folders have been created. i.e. ```sitecore > Templates *new_tenant_you_created*```. In that folder there will be a bunch of Data Templates. Same for the Media Library, ```sitecore > Media Library > Project > *new_tenant_you_created*```.

Next, right-click on the ```*new_tenant_you_created*```, and you will see a menu similar to when you right-click on the ```Content``` in your folder tree. Under ```Insert``` there are options to create a Site, Site Folder, or Insert From Template. Click ```Insert > Site``` and the Site wizard will load. This wizard is more complex than the first one we met, this is a 4-tabbed wizard. He will ask you about General, Modules, Theme, and Grid. Be ready.

Under General > Site name, tell the 4-tabbed wizard the name of your site. You will do this by clicking into the Site name field, then using the keyboard to type the name of your site. i.e. My Super Awesome Sitecore SXA Website. In the Host name field, you will have to tell the 4-tabbed wizard the URL for your website, but it will also need to be bound and that's a thing that BED people do, so as the presenter does, just skip that $***. In the Virtual folder field, the 4-tabbed wizard is curious if you would like to store your files anywhere other than the site root. Just leave it alone. Same with the Language dropdown; if you want anything other than English, select that, otherwise, leave it alone.

Moving on to the second tab in our 4-tabbed wizard, Modules, here you can select the modules that you may want preconfigured for your site. This time, think about what Modules you actually want, because sitecore will make all of them if you want, but that's a lot of time and data which you may not need to waste or use. If you happen to make an improper selection or miss a Module, you can fix that later on.

Welcome to the third tab in our 4-tabbed wizard, Theme. You can create a new theme by clicking the checkbox labeled *Create a new theme*. There also exists a default theme called *Wireframe*. Check the *Create a new theme* checkbox and in the *New theme name* input field, tell the 4-tabbed wizard the name of your new theme.

And... we've made it to the fourth and final tab in our 4-tabbed wizard, Grid. By default, there are THREE grid options; Bootstrap, Foundation, and Grid 960. Just go with Bootstrap and click that little blue Ok button in the bottom-right corner of the 4-tabbed wizard and the new *My Super Awesome Sitecore SXA Website* site will generate. It may take a while, go get a La Croíx or take a nap. Do NOT do anything else or the 4-tabbed wizard will destroy your computer and most of the internet.

Phew, you dodged a something by following directions well. Click the little blue Close button and now you will see your *My Super Awesome Sitecore SXA Website* site underneath your previously created Tenant, i.e. ```sitecore > Content > *new_tenant_you_created* > My Super Awesome Sitecore SXA Website```. Inside of your My Super Awesome Sitecore SXA Website in the folder tree, you can see a whole bunch of folders that have been made by the 4-tabbed wizard for you! He made; Home, Media, Data, Presentation, and Settings folders! Home stores all of your webpages, Media stores media, Data stores all of the different Modules you selected earlier (these will act as a datasource for your website), Presentation stores the different files that control how your website looks and behaves, and finally Settings allows you to change a bunch of settings for your site (404 page, 500 server error page control lives here). Under ```sitecore > Content > *new_tenant_you_created* > My Super Awesome Sitecore SXA Website > Settings > Site Grouping > My Super Awesome Sitecore SXA Website```, you can find the settings that you defined with the 4-tabbed wizard *General* tab.

A Site will share datasources with its tenant, but you will have control over theme and a virtual folder for the site will exist independent of the tenant. If you should ever need to delete your site, you can rihght-click on the site name in the folder tree and under *Scripts*, click the *Remove site* option. This will run a script that removes all of the folders which are specific to the site which you would like to remove. The *Are you sure you want to delete My Super Awesome Sitecore SXA Website?* wizard will launch to confirm your decision. If you are certain, you may click the blue *OK* button, if you would like to thank this wizard for saving you from making an egregious error, click the grey *Cancel* button, and the wizards disappearance will serve as acknowledgement of both your thanks and your error. There is a similar option available for Tenants that you wish to remove from your sitecore instance. Follow the above steps and meet the wizard.

If you had deselected a module when running though any of the wizards you have met before *(either the tenant one-step wizard, or the site 4-tabbed wizard)* and would like to add a module to them, right-click on the name of the site or tenant and under the *Scripts* menu, there is a script called *Add Site module*. Click that. The Add site module wizard will appear to help you in your search to add modules. If you have made any custom modules for sitecore and placed them in your sitecore instance, they would be available in the add module wizard if you had not selected them when making a tenant or site.

</details>

<details>
<summary>SXA Partial and Page Design Basics</summary>



</details>

[Custom Component Build - Part 1 - Introduction](https://www.nishtechinc.com/en/Blog/2018/November/Nuptial-Experiment-Introduction)

[Custom Component Build - Part 2 - Milestone 1](https://www.nishtechinc.com/en/Blog/2018/November/Nuptial-Experiment-Part-2)

[Custom Component Build - Part 3 - Milestones 2 & 3](https://www.nishtechinc.com/en/Blog/2018/November/Nuptial-Experiment-Part-3)

[Custom Component Build - Part 4 - Final Thoughts](https://www.nishtechinc.com/en/Blog/2018/November/Nuptial-Experiment-Final-Thoughts)

[SXA Overview Part 1](https://www.velir.com/blog/2017/10/16/tour-sitecore-experience-accelerator-sxa-part-1)

[SXA Overview Part 2](https://www.velir.com/blog/2017/10/16/tour-sitecore-experience-accelerator-sxa-part-2)

[SXA Implementation - Some Tips & Tricks](https://www.sidewalk.be/articles/the-sitecore-sxa-journey-discover-tips-and-tricks-when-implementing-an-sxa-website)

[Video Tutorial Walkthrough](https://www.reddit.com/r/sitecore/comments/bdihvd/sitecore_sxa_tutorials_sxa_1_8_full_site_step_by/)

[Add data attributes to renderings](http://blog.martinmiles.net/post/how-to-add-id-and-data-attributes-to-a-rendering-variant-in-sxa)

## Random Junk & Garbage

[ES6 In Depth - Brought to you by Mozilla](https://hacks.mozilla.org/category/es6-in-depth/)

[Add or Remove classes on things w/ Jquery?](http://jsfiddle.net/ak9Lnrjj/10/)  
*could be a fix for slick carousel variable height slides. add a class that makes all the other slides have```css display: none;```* 

[Charles - Web Debugging Proxy Application](https://www.charlesproxy.com)

## Ewwww SVG

*read in order*

[A Primer to Frontend SVG Hacking :D](https://dbushell.com/2013/02/04/a-primer-to-front-end-svg-hacking/)

[Optimizing SVGs in Data URIs](https://codepen.io/tigt/post/optimizing-svgs-in-data-uris)

[Data URI Generator](https://dopiaza.org/tools/datauri/index.php)

[URL Encoder](https://www.urlencoder.org/)

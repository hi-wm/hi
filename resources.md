---
title: Frontend Development Resources
---

Here are some Frontend Development resources that have proven useful

## Sitecore Experience Accelerator

<details>
<summary>SXA Basics</summary>
<details>
<summary>Tenant and Site Creation</summary>
<br />  

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
<br />  

*Within SXA, you can use partial and page designs to create your UX layout.*

After datasource architecture, partial and page designs is a likely first step. Follow this path ```sitecore > Content > *my_tenant_name* > *my_site_name* > Presentation > Page || Partial Designs```. Partial Designs, i.e. a Header or Footer, are combined to create a Page Design. Right-click on ```Partial Designs``` then find ```Insert > Partial Design```. In the partial design wizard, give your partial design a name, i.e. Header, then click ok. Your new partial design will appear in the folder tree, right-click on that then click ```Experience Editor```, this will open the *Experience Editor*.

Within the *Experience Editor* you can drag and drop components into your partial design. In the *Experience Editor*, you will see (in the main part of the screen) a field that looks like a canvas (grey and white checkboard patterned), this is where the components for your partial design will go. There is a *header*, a *main*, and a *footer* for each partial design and when the page is rendered, these sections will be rendered in that order. For example, if you are making a Header component, but place the components for the partial design in a section that is not the header, then your Header Partial Design will not render in the header of your page.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Canvas.png "SXA Experience Editor Canvas")
*SXA Experience Editor Canvas. The alternating white and blue squares are highlighting the *main* section of the partial design canvas area*

To add a component to the Header, drag the *Navigation* component from the right-hand side of the *Experience Editor* to the header section of the canvas. The *Navigation* component is nested under the *NAVIGATION* category of available components. Once the *Navigation* component is in the header section of the canvas, a toolbar for that component will appear (as seen below).

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Navigation-Component.png "SXA Experience Editor Navigation Component placed in header of Design Partial, toolbar active")
*SXA Experience Editor Navigation Component placed in header of Design Partial, toolbar active*

On the right-side of the toolbar for your placed component, there is a dropdown menu, labeled *More*, underneath which are additional options for your component. Click *More*, then click *Edit component properties* to open the *Control Properties* wizard. When the wizard opens, scroll to the bottom *Styling* section. Here you can change the style of your component. Under *Navigation*, click the *Big/Fat Navigation*, then scroll further to the *Navigation Settings* section of the wizard. In the *Navigation Settings* section of the *Control Properties* wizard you can adjust the levels of navigation. In the demo, the presenter changes the *Bottom Navigation Level* from the default of 2, to 1. Click the little blue *OK* button to save the changes to your component. You should now see a horizontal navigation. Click save.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Component-Control-Properties-Wizard.png "SXA Experience Editor Component Control Properties Wizard")
*SXA Experience Editor Component Control Properties Wizard showing the Navigation Settings settings*

Back in the main folder tree of your project, right-click on ```Partial Designs``` then find ```Insert > Partial Design```. In the partial design wizard, give your partial design a name, i.e. Footer, then click ok. Your new partial design will appear in the folder tree, right-click on that then click ```Experience Editor```, this will open the *Experience Editor*.

Try inserting a *Rich Text* component into the footer section of your footer partial design. The *Rich Text* component is in the *PAGE CONTENT* section on the right-hand side of the partial design experience editor. Add some basic text, i.e. © 2019, then click the save icon in the top-left corner of the *Experience Editor*.

Back in the main folder tree again, in the *Partial Designs* folder of your site you should have a *Footer* and a *Header*. These can now be combined in a *Page Design*. Without a page design, there will be no way to render a page and page designs are dependent on partial designs. So far, the design partials that have been created are only within the header and footer sections of the page, applying those to a page design would still leave the *main* section of a page empty. If you are working on a specific page design layout that requires content to be in the *main* section of a page (show me a page that only has a header and a footer...), then you will need to build some partial designs that have components in the *main* section of them.

In the folder tree, right-click on *Page Designs* and ```Insert > Page Design```. In the *new page design* wizard, enter a name for the new item (the new page design).

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Page-Design-Insert.png "SXA Experience Editor Page Design Insert")
*SXA Experience Editor Page Design Insert menu*

Once you have named your new page, you will be presented with options for your new page. Under the *Designing* section, ALL shared *Partial Designs* are available to be selected for the page design. Clicking the name will move them over to the Selected area.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Page-Design-Window.png "SXA Experience Editor Page Design Window")
*SXA Experience Editor Page Design Window*

Add your *Header*, *Footer*, and *Metadata* *Partial Designs*, then click the save icon in the upper right-hand corner of the screen. Now, if you follow your website folder tree to; ```Tenant > *site_name* > Home > Page_#``` then right-click and select *Experience Editor*, you will be taken to the Experience Editor for that page.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Page-Design-Setup.png "SXA Experience Editor Page Design Setup")
*SXA Experience Editor Page Design Setup. You can select a page design here*

Leave the *Home* Page alone, but set the *Page* design type to the *Page Design* you have previously created. Save the setting (upper right-hand corner), you should then see the header and footer automatically assigned to your page.
</details>
<details>
<summary>Rendering Variants - Part 1 - The Basics</summary>
<br />  

*What are Rendering Variants and when should you use them?*

In Sitecore, most of the pages that display content can be rendered using *Rendering Variants*. In your project folder tree, look at ```sitecore > Templates > Project > Tenant > Blog Post```. Here you can *Build* a template that can be used to structure your blog posts.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Blog-Post-Template.png "SXA Experience Editor Rendering Variants Blog Post Template")
*SXA Experience Editor Rendering Variants Blog Post Template. Set up the fields needed for blog posts*

If you open a Blog Post in the sitecore *Experience Editor*, you can drop a *Page Content* component into the main section of the blog post (find this component in the *PAGE CONTENT* section of available components on the right-hand side of the *Experience Editor*). By default, the *Page Content* component will use the first found rendering variant. To make a new *Rendering Variant* definition, check the screenshot below.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Page-Content-Variant.png "SXA Experience Editor Rendering Variants Page Content Variant")
*SXA Experience Editor Rendering Variants Page Content Variant*

The *Variant Definition* wizard will launch and you can enter a new name for your variant definition. After you have named your rendering variant definition, it will appear under ```Page Content > *new_rendering_variant*```. You can now insert a variety of rendering variant renderers that will be available for your *new_rendering_variant*. Add a new *Field* and name it "Title" then set the *Tag* to h1. Make sure you click the *Save* button in the upper right-hand corner of the screen.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Page-Content-Variant-Add-Field.png "SXA Experience Editor Rendering Variants Page Content Variant Add Field")
*SXA Experience Editor Rendering Variants Page Content Variant Add Field*

Now that you've added a field to your rendering variant, add another! This time add a field and name it *Author*. In the *Variant Details* section, set the *Tag* to a ```<span>```. In the *Data attributes* section of your new field, you can specify inline style attributes, but don't.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Page-Content-Variant-Add-Field-Data-Attributes.png "SXA Experience Editor Rendering Variants Page Content Variant Add Field Data Attributes")
*SXA Experience Editor Rendering Variants Page Content Variant Add Field Data Attributes Inline Styling… Please DON'T*

Now, if you click the *Save* button (you should hopefully know where it is by now, but if not... it is in the upper right-hand corner), you can load up your *Blog Post* page and see that you now have an author field in your render variant. As you add additional content to your rendering variant, you can simply reorder the items by dragging and dropping them within the folder tree, otherwise, sitecore will order them in the order they were created.

Add a *Date* field to your rendering variant, name it however you like, play with the settings, i.e. format of date (hint: there is a dropdown within the *Date* rendering variant component settings), save it, reorder it from within your folder tree, then check the result on your *Blog Post* page. Try adding an ```<hr>``` by using the *HTML Tag* element type.

When exposing content that has been defined in a page type, make sure to set up fields in your rendering variant that match the different fields in your page. i.e. if you have an image and it is called *MyImage* make sure that the *Field Name* matches.

In order to provide some additional structure to all of these items that you are generating to build a rendering variant, adding *Section* elements to your rendering variant can help keep things organized. Just as you've added a *Field* or an *HTML Tag*, right-click on the rendering variant name and ```Insert > Section```. Name your sections semantically, i.e. *Header*, *Main*, *Footer*. Then, you can drag and drop your different elements into your sections. *Sections* can also be styled via *Data attributes*, but DON'T

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Page-Content-Variant-Add-Section.png "SXA Experience Editor Rendering Variants Page Content Variant Add Sections")
*SXA Experience Editor Rendering Variants Page Content Variant Add Sections. You can organize your render variant with sections*

Great, now you've manually built a rendering variant and applied it to a *Blog Post*, but you are missing the automation that sitecore and SXA brings. Let's make a *Partial Design* from all of this work.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Page-Content-Variant-Insert-Partial-Design.png "SXA Experience Editor Rendering Variants Page Content Variant Insert Partial Design")
*SXA Experience Editor Rendering Variants Page Content Variant Insert Partial Design. Let's make a partial design out of our rendering variant*

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Page-Content-Variant-Insert-Partial-Design-Wizard.png "SXA Experience Editor Rendering Variants Page Content Variant Insert Partial Design Wizard")
*SXA Experience Editor Rendering Variants Page Content Variant Insert Partial Design Wizard. Let's make a partial design out of our rendering variant*

Once you have created the partial design, drop the *Page Content* component into the *main* section of the page, then set the *Variant* to the variant you have previously been working with in this chapter. Save your thing. Then create a *Page Design* so that you can assign the just created *Partial Design* to the *Page Design*.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Page-Content-Variant-Insert-Page-Design.png "SXA Experience Editor Rendering Variants Page Content Variant Insert Page Design")
*SXA Experience Editor Rendering Variants Page Content Variant Insert Page Design.*

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Page-Content-Variant-Insert-Page-Design-Wizard.png "SXA Experience Editor Rendering Variants Page Content Variant Insert Page Design Wizard")
*SXA Experience Editor Rendering Variants Page Content Variant Insert Page Design Wizard*

After giving your *Page Design* a name, in the next dialogue wizard that appears, you will have to assign the *Partial Designs* to your *Page Design*. Save that, then you will be able to associate your new *Page Design* with whatever type page needed, in this case *Blog Post*. Do that in the *Site Page Designs* menu at the top-center of the screen.
</details>
<details>
<summary>Create Fixed Layouts with the Page Content Component</summary>
<br />  

*With the Page Content Component, you can speed up development by creating Fixed Layouts*

The recommended approach to using SXA is to give content authors freedom for Landing Pages, allow them to arrange components how they like. But for the more detailed pages, for example a blog page or a news article, it's better to create fixed layouts so that your visitors are not disoriented navigating through your site. This is where the *Page Content Component* comes in handy. It can read all of the different fields and values of your different pages and display them in a certain layout. Navigate to ```Templates > Project > *your_tenant* > Custom templates```. If you do not have the *Custom templates* folder, create one, otherwise, right-click on the *Custom templates* folder and ```Insert > New Template```, this will launch the *New Template* wizard. The *New Template* wizard will guide you through the *New Template* creation process. Give your new template a name.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Create-Fixed-Layout-Custom-Template.png "SXA Experience Editor Create Fixed Layout Custom Template")
*SXA Experience Editor Create Fixed Layout Custom Template*

In the *New Template* wizard, after you have given it a name, select the *Base template*. The video example provides the following path ```Templates > Project > *new_tenant* > Page```. After you have selected the *Base template*, click *Next* to save your *New Template*. Locate your new template in your project folder tree, then select it by clicking on its name. On the right-hand side of the project folder tree, options related to your new template will open up.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Create-Fixed-Layout-Custom-Template-Options.png "SXA Experience Editor Create Fixed Layout Custom Template Options")
*SXA Experience Editor Create Fixed Layout Custom Template Options*

In the *Builder* tab for the new template, add a section named *Content* then define 2 additional fields below the new section name:

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Summary</td>
      <td>Multi-Line Text</td>
    </tr>
    <tr>
      <td>Publishdate</td>
      <td>Date</td>
    </tr>
  </tbody>
</table>

Now that you have your new fixed layout, go to ```sitecore > Content > *tenant_name* > *site_name* > Home``` and right-click on *Home*. You should be able to click *Insert* and see your new fixed layout that was just created as an option when creating a new page for your site. Select the new fixed layout type and give your page a name. If everything has been correctly set up, you should now see your new page with the fields that were established above.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Create-Fixed-Layout-Custom-Template-Applied.png "SXA Experience Editor Create Fixed Layout Custom Template Applied")
*SXA Experience Editor Create Fixed Layout Custom Template Applied*

Using your new template, you can create new pages that have the type of your template and each page will be generated according to how you defined the template. Finally a shoutout to FED, it is said that with the basic structure of our pages defined, we are free to style the page the way we need. Yay SXA ?!
</details>
<details>
<summary>Creating and Working with Styles</summary>
<br />  

<!-- *What are Rendering Variants and when should you use them?*

In Sitecore, most of the pages that display content can be rendered using *Rendering Variants*. In your project folder tree, look at ```sitecore > Templates > Project > Tenant > Blog Post```. Here you can *Build* a template that can be used to structure your blog posts.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Blog-Post-Template.png "SXA Experience Editor Rendering Variants Blog Post Template")
*SXA Experience Editor Rendering Variants Blog Post Template. Set up the fields needed for blog posts*

If you open a Blog Post in the sitecore *Experience Editor*, you can drop a *Page Content* component into the main section of the blog post (find this component in the *PAGE CONTENT* section of available components on the right-hand side of the *Experience Editor*). By default, the *Page Content* component will use the first found rendering variant. To make a new *Rendering Variant* definition, check the screenshot below.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Page-Content-Variant.png "SXA Experience Editor Rendering Variants Page Content Variant")
*SXA Experience Editor Rendering Variants Page Content Variant* -->
</details>
<details>
<summary>The SXA Themes - Structure and Inheritence</summary>
<br />  

<!-- *What are Rendering Variants and when should you use them?*

In Sitecore, most of the pages that display content can be rendered using *Rendering Variants*. In your project folder tree, look at ```sitecore > Templates > Project > Tenant > Blog Post```. Here you can *Build* a template that can be used to structure your blog posts.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Blog-Post-Template.png "SXA Experience Editor Rendering Variants Blog Post Template")
*SXA Experience Editor Rendering Variants Blog Post Template. Set up the fields needed for blog posts*

If you open a Blog Post in the sitecore *Experience Editor*, you can drop a *Page Content* component into the main section of the blog post (find this component in the *PAGE CONTENT* section of available components on the right-hand side of the *Experience Editor*). By default, the *Page Content* component will use the first found rendering variant. To make a new *Rendering Variant* definition, check the screenshot below.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Page-Content-Variant.png "SXA Experience Editor Rendering Variants Page Content Variant")
*SXA Experience Editor Rendering Variants Page Content Variant* -->
</details>
<details>
<summary>Introduction to Responsive Grid Settings for Components</summary>
<br />  

<!-- *What are Rendering Variants and when should you use them?*

In Sitecore, most of the pages that display content can be rendered using *Rendering Variants*. In your project folder tree, look at ```sitecore > Templates > Project > Tenant > Blog Post```. Here you can *Build* a template that can be used to structure your blog posts.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Blog-Post-Template.png "SXA Experience Editor Rendering Variants Blog Post Template")
*SXA Experience Editor Rendering Variants Blog Post Template. Set up the fields needed for blog posts*

If you open a Blog Post in the sitecore *Experience Editor*, you can drop a *Page Content* component into the main section of the blog post (find this component in the *PAGE CONTENT* section of available components on the right-hand side of the *Experience Editor*). By default, the *Page Content* component will use the first found rendering variant. To make a new *Rendering Variant* definition, check the screenshot below.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Page-Content-Variant.png "SXA Experience Editor Rendering Variants Page Content Variant")
*SXA Experience Editor Rendering Variants Page Content Variant* -->
</details>
<details>
<summary>Configuring and Working with Shared Sites</summary>
<br />  

<!-- *What are Rendering Variants and when should you use them?*

In Sitecore, most of the pages that display content can be rendered using *Rendering Variants*. In your project folder tree, look at ```sitecore > Templates > Project > Tenant > Blog Post```. Here you can *Build* a template that can be used to structure your blog posts.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Blog-Post-Template.png "SXA Experience Editor Rendering Variants Blog Post Template")
*SXA Experience Editor Rendering Variants Blog Post Template. Set up the fields needed for blog posts*

If you open a Blog Post in the sitecore *Experience Editor*, you can drop a *Page Content* component into the main section of the blog post (find this component in the *PAGE CONTENT* section of available components on the right-hand side of the *Experience Editor*). By default, the *Page Content* component will use the first found rendering variant. To make a new *Rendering Variant* definition, check the screenshot below.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Page-Content-Variant.png "SXA Experience Editor Rendering Variants Page Content Variant")
*SXA Experience Editor Rendering Variants Page Content Variant* -->
</details>
</details>
<br />

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

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
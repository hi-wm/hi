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

The *Variant Definition* wizard will launch and you can enter a new name for your variant definition. After you have named your rendering variant definition, it will appear under ```Page Content > *new_rendering_variant*```. You can now insert a variety of rendering variant renderers that will be available for your *new_rendering_variant*. Add a new *Field* and name it "Title" then set the *Tag* to h1.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Rendering-Variants-Page-Content-Variant-Add-Field.png "SXA Experience Editor Rendering Variants Page Content Variant Add Field")
*SXA Experience Editor Rendering Variants Page Content Variant Add Field*

</details>
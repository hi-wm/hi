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

| Name | Type |
| :--- | ---: |
| Summary | Multi-Line Text |
| Publishdate | Date |
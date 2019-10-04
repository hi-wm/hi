<summary>Part 2 - Working with References and Links</summary>
<br />  

Following up on the previous *Rendering Variants* *Blog Post* has been extended. The Author / Single-Line Text has been subbed for Authors / Multiroot Treelist with a dynamic source.

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Working-References-Links-Dynamic-Source.png "SXA Rendering Variants Working with References and Links Dynamic Source Example ")
*SXA Rendering Variants Working with References and Links Dynamic Source Example*

To set up the dynamic source for the *Blog Post*, a new folder has been added ```sitecore > Content > *tenant_name* > *site_name* > Data > *new_folder_name*```, in this case the new folder is called *Authors* and a bunch of authors have been added. A new rendering variant is required for this new set of *Data*. To create a new *Rendering Variant* follow this path ```sitecore > Content > *tenant_name* > *site_name* > Presentation > Rendering Variants > Page Content```, right-click on *Page Content* then ```Insert > Variant Definition```. Give your new *Variant Definition* a name.

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Working-References-Page-Content-Definition.png "SXA Rendering Variants Working with References and Links, creating a new variant definition for Page Content component")
*SXA Rendering Variants Working with References and Links, creating a new variant definition for Page Content component*

If you click on your new variant definition, the *Content* window to the right of the folder tree will become active for the new variant definition. Scrolling down the *Content* window, there is a field to add CSS classes to the variant definition, add any classes as needed, separated by a space. 

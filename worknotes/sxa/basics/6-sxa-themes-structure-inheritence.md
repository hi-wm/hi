<summary>The SXA Themes - Structure and Inheritence</summary>
<br />  

*The overall look and feel of a website is because of a theme.*

sitecore / SXA comes with a two base themes; Wireframes & Wireframes (deprecated). There is also a set of *Base Themes* that style components. When you create a Tenant and then a site, you will also get a corresponding Tenant / site set of folders in the *Themes* folder. This is where you place your site theme. Back up the folder tree, in ```sitecore > Content > *tenant_name* > *site_name*```, if you click on the site_name, you can export the site to hand off to a FED team to implement the styling. Check the screenshots below.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Theming-Export-Site-Theme.png "SXA Experience Editor Theming, Export Site Theme")
*SXA Experience Editor Theming, Export Site Theme*

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Theming-Export-Site-Theme-Wizard.png "SXA Experience Editor Theming, Export Site Theme Wizard")
*SXA Experience Editor Theming, Export Site Theme Wizard. Here you can select different options for exporting your site theme*

In the export site theme wizard shown above, there are a variety of settings that you may need to change when exporting your site theme.

* Device - If there is more than one device-based theme available for your site, more options would appear
* Language - If there are additional languages activated for your site instance, more options would appear
* Pages in buckets - Not very clear what this does, but you can select Ignore, Include, or One of template
* Export to - .zip file or server location? Should be pretty self explanatory
* Exported content - entire Site? a Branch? or a Single page? Your needs should dictate the choice you make here
* Mode - Either you can re-import the site later on by making it importable, or not...

Once you have made the difficult choices with the export site theme wizard, click the button labeled *Next*. Your site will export, there is even a delightful animation to keep you distracted while the wizard works his magic.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Theming-Export-Site-Theme-Exporting.gif "SXA Experience Editor Theming, Export Site Theme Exporting Animation")
*SXA Experience Editor Theming, Export Site Theme Exporting Animation for your enjoyment*
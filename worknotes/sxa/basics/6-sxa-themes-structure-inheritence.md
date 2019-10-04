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

After the wizard is done, you can download your .zip file. *If you chose that option in the intial setup* Abruptly moving on, let's talk about *gulp* files. The *gulp* is a task runner. Read more about [*gulp*](https://gulpjs.com/). In sitecore, and any project that uses *gulp*, once configured, there are various tasks that do things.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Theming-Export-Site-Theme-Gulp.png "SXA Experience Editor Theming, Export Site Theme Gulp task list")
*SXA Experience Editor Theming, Export Site Theme Gulp task list*

In the *sass* folder, there are *sass* files. In passing, we know that the *sass* will be handled by the *gulp*. In the *fonts* folder, there are fonts. In the *images* folder, there are images. And in the *styles* folder, there are styles.

Imagine for a moment that your client would like a theme just for Christmas. Don't overwrite your style files! Make a new site theme! Right-click on your site name in the folder tree, then follow ```Scripts > New Site Theme```. The *New Site Theme* script will run and eventually open the *Create a new SXA site theme.* wizard. Tell the wizard all of the things.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Theming-New-Site-Theme.png "SXA Experience Editor Theming, New Site Theme")
*SXA Experience Editor Theming, New Site Theme*

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Theming-New-Site-Theme-Script-Running.png "SXA Experience Editor Theming, New Site Theme Script Running")
*SXA Experience Editor Theming, New Site Theme Script Running*

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Theming-New-Site-Theme-Wizard.png "SXA Experience Editor Theming, New Site Theme Wizard")
*SXA Experience Editor Theming, New Site Theme Wizard*

After naming your new theme, you can just click next. The *New Site Theme* script will then finish up. The amount of time that the *New Site Theme* script takes to run is directly correlated to the processing power of your computer. Once hell has frozen over, your new theme will be somewhere... maybe ```... > Themes > *tenant_name* > *site_name*```. Now that you have your new theme, you can make all the required changes and the changes will only affect that theme! And 3 minutes of clicking around later... You can make all the required changes and the changes will only affect that theme! Seriously, there was nothing useful stated at the end of the video.
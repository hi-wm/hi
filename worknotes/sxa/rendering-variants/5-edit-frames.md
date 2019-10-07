<summary>Part 5 - Edit Frames</summary>
<br />  

Link to YouTube video for this section [SXA Rendering Variants Part 5 - Edit Frames](https://youtu.be/x1YREa4KG3Y)

*Using Edit Frames to solve some problems with Rendering Variants*

In a rendering variant, when a reference is established, the variant will iterate through available items in a data source and render them according to the definition. This is normal, but if a content author would like to edit these items in any way, additional measures must be taken to set up this functionality. This can be done by wrapping references in an *Edit Frame*. Right-click on the top-level of the variant and ```Insert > Edit Frame```. You will need to move all of the rendering elements into the *Edit Frame* to make them editable.

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Edit-Frames-Add.png "SXA Rendering Variants Edit Frames, add an Edit Frame to a rendering variant")
*SXA Rendering Variants Edit Frames, add an Edit Frame to a rendering variant*

The *Edit Frame* needs buttons to be selected. But the needed buttons are not available in the dropdown of available elements, but they do exist in the core database of sitecore ```/sitecore/content/Applications/WebEdit/Edit Frame Buttons```. Find the location of the buttons that you would like to use and, as you should have been doing in many other occasions, make a copy of the buttons, title them according to the element that they will belong to, and update the settings of the button; Header, Icon, Fields

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Edit-Frames-Button-Setup.png "SXA Rendering Variants Edit Frames, set up the buttons for your Edit Frame")
*SXA Rendering Variants Edit Frames, set up the buttons for your Edit Frame*

Back in the rendering variant, the buttons that were just defined are now available from the buttons dropdown for the *Edit Frame*. Click *Save* and return to the *Experience Editor* to see the *Edit Frame* just defined is now active and able to be used. *Edit Frames* can do more than buttons, but that is outside the scope of this video.

Further details about *Edit Frames* can be found in sitecores [Create a Rendering Variant](https://doc.sitecore.com/developers/sxa/18/sitecore-experience-accelerator/en/create-a-rendering-variant.html) documentation.
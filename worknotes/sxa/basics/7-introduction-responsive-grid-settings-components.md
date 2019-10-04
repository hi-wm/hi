<summary>Introduction to Responsive Grid Settings for Components</summary>
<br />  

Jumping right in... in the *Experience Editor* turn on the *Grid*, it is under the *VIEW* tab at the top of the *Experience Editor*. Then, back in the canvas section of the *Experience Editor*, you will see the grid when you click on a section of the page i.e. header, main, footer.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Responsive-Grid-Turn-On.png "SXA Experience Editor Responsive Grid, turn it on")
*SXA Experience Editor Responsive Grid, turn it on*

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Responsive-Grid-Show.png "SXA Experience Editor Responsive Grid, this is how it looks")
*SXA Experience Editor Responsive Grid, this is how it looks when you are working on the component canvas with the grid turned on*

The columns shown above are the grid. There are likely to always be 12 columns. These columns are used to lay out components and content. You will need to tell the components how much space they are allowed to take, i.e. how many columns wide they can be. Add a *Rich Text* component to the main area of your canvas. Add some lorem ipsum placeholder text to your *Rich Text* component. Hit save in the upper right-hand corner of the *Experience Editor*. If you do not hit save and start making adjustments to the grid settings for your component, it is possible that your changes will be lost and no one wants that, except for the *Experience Editor*... Anyway, it is always good practice to save. With your component selected, click *More* on the component editor panel, then *Edit component properties* to bring up the component properties dialogue window.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Responsive-Grid-Edit-Component.png "SXA Experience Editor Responsive Grid, edit the component")
*SXA Experience Editor Responsive Grid, edit the component*

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Responsive-Grid-Edit-Component-Dialogue.png "SXA Experience Editor Responsive Grid, edit the component with this dialogue window")
*SXA Experience Editor Responsive Grid, edit the component with this dialogue window. See the grid settings?*

The component grid settings are organized by a mobile first approach, from smallest device type to largest. In the above screenshot, *Compact Phones* is set to 12, which means that this component will take up all of the available column space and since no other devices types have settings applies, they will inherit from the *Compact Phones* setting. If you would like to modify the components column settings for other device types, simply click on the dropdown menu next to the device name and set the number of columns you would like the component to use accordingly. If you skip a device type, the setting from a higher level device type will be inherited until the next definition is reached. i.e. if the *Compact Phones* and *Tablets* have settings, but no other devices are set, then *Phones* will inherit its settings from *Compact Phones* and *Laptops* & *Desktops* will inherit their settings from *Tablets*. yay. Set the *Tablets* column settings to 6. Save.

Add another *Rich Text* component as above and repeat the steps to make it take up 6 columns. Now you should have something that looks like this:

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Responsive-Grid-6-Col-Components.png "SXA Experience Editor Responsive Grid, these two Rich Text components have their columns set to 6 for devices Tablets and up")
*SXA Experience Editor Responsive Grid, these two Rich Text components have their columns set to 6 for devices Tablets and up*

If you would like to confirm that the column settings you have made are in fact working, open up the Chrome inspector and toggle the responsive view mode or resize your browser window and watch the magic unfold.

The most important thing is to remember that you have 12 columns to work with.
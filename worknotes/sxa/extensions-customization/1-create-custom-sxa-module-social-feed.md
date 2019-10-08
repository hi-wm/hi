<summary>Create Custom SXA Module - Social Feed</summary>
<br />  

Link to YouTube video for this section [Create Custom SXA Module - Social Feed](https://youtu.be/avuVlJ34BwU)

*It's always better to clone an existing component rather than using the existing component*

It is recommended to clone an existing component because there is a folder structure to a component and it is easier to modify a clone than to make all of the required folders and files from scratch. The component to copy for this tutorial is the *Promo* component. Find the *Promo* component in sitecores folder tree, right-click the name, then ```Scripts > Clone Rendering```.

![alt text](assets/images/sxa-extensions-customization/SXA-Extensions-Customization-Custom-Module-Clone-Existing.gif "SXA Extensions and Customization, clone an existing component and use the wizard to configure the component clone")
*SXA Extensions and Customization, clone an existing component and use the wizard to configure the component clone*

The cloning process will create a full blown component, which may need to be cleaned up after it has been cloned. For example, if you look at the component itself, in this case the *Promo* clone, you will find that there are a lot of settings related to the original *Promo* that you would like to change.

For additional documentation, please refer to the sitecore docs on how to [create a new SXA module](https://doc.sitecore.com/developers/sxa/17/sitecore-experience-accelerator/en/create-a-new-sxa-module.html)

And here's a nice article following the flow of [creating a custom SXA component](http://blog.martinmiles.net/post/creating-custom-sxa-components-with-rendering-variants-and-almost-no-codebehind-on-an-example-of-social-share-buttons)
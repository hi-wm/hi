<summary>Create Custom SXA Module - Social Feed</summary>
<br />  

Link to YouTube video for this section [Create Custom SXA Module - Social Feed](https://youtu.be/avuVlJ34BwU)

*It's always better to clone an existing component rather than using the existing component*

It is recommended to clone an existing component because there is a folder structure to a component and it is easier to modify a clone than to make all of the required folders and files from scratch. The component to copy for this tutorial is the *Promo* component. Find the *Promo* component in sitecores folder tree, right-click the name, then ```Scripts > Clone Rendering```.

![alt text](assets/images/sxa-extensions-customization/SXA-Extensions-Customization-Custom-Module-Clone-Existing.gif "SXA Extensions and Customization, clone an existing component and use the wizard to configure the component clone")
*SXA Extensions and Customization, clone an existing component and use the wizard to configure the component clone*

The cloning process will create a full blown component, which may need to be cleaned up after it has been cloned. For example, if you look at the component itself, in this case the *Promo* clone, you will find that there are a lot of settings related to the original *Promo* that you would like to change. For the social media component configuration, there is the configuration of the component itself, and the configuration of the rendering as seen in the screenshots below.

![alt text](assets/images/sxa-extensions-customization/SXA-Extensions-Customization-Custom-Module-Configuration.png "SXA Extensions and Customization, custom module configuration. The field settings are specific to the Social Feed component that is being created")
*SXA Extensions and Customization, custom module configuration. The field settings are specific to the Social Feed component that is being created*

![alt text](assets/images/sxa-extensions-customization/SXA-Extensions-Customization-Custom-Module-Render-Configuration.png "SXA Extensions and Customization, custom module render configuration. The field settings are specific to the Social Feed component that is being created")
*SXA Extensions and Customization, custom module render configuration. The field settings are specific to the Social Feed component that is being created*

Now that the component and it's base render settings have been configured, the layout rendering should be configured as well. ``` sitecore > layout > Renderings > Feature > *custom_component*``` The presenter launches VSCode and has a completed component ready to go. What would appear to be the BED work for a custom component is presented. There are a lot of methods and constructors called, the section from [8:29 - 16:34](https://youtu.be/avuVlJ34BwU?t=509)(link starts at 8:29 mark) covers the implementation in VSCode. The component implementation is brief yet comprehensive. Additional learning would be useful for this one. At the very end of the video, the presenter states, "most of the work is done in the backend to create the controller".

For additional documentation, please refer to the sitecore docs on how to [create a new SXA module](https://doc.sitecore.com/developers/sxa/17/sitecore-experience-accelerator/en/create-a-new-sxa-module.html)

And here's a nice article following the flow of [creating a custom SXA component](http://blog.martinmiles.net/post/creating-custom-sxa-components-with-rendering-variants-and-almost-no-codebehind-on-an-example-of-social-share-buttons)
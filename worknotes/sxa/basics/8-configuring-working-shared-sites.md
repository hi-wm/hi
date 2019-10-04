<summary>Configuring and Working with Shared Sites</summary>
<br />  

*Working with shared sites, how to configure them, and what you can do with them*

Imagine a real-life company (this is what a *tenant* is in sitecore) with multiple brand sites (these would be the sites that live under the company *tenant*) that have some shared content (about us, contact, something else?), wouldn't it be nice to be able to manage this shared content in a central place and not have duplicate content? The suggested approach here would be to literally create a site instance that serves as a central repository, then in however many site instances you have to create, you can use the central repository assets, components, etc for your other sites. If you click on your tenant folder, the right-hand side of your screen will show the *Content* viewer for your tenant. If you scroll down the *Content* view, you will hit a *Sharing* section where you can configure sites that are Shared or not. In the following screenshot, *Central Repository* has been added to the *Shared sites*. Other sites will now be able to use content that exists on the *Central Repository*.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Shared-Sites-Setup.png "SXA Experience Editor Shared Sites, see the Central Repository added to the shared sites")
*SXA Experience Editor Shared Sites, see the Central Repository added to the shared sites*

Now that a shared site has been set for the tenant, when adding components in the *Experience Editor*, you will be able to *Select the Associated Content* and will see the shared site that wasjust set up as an option for the associated content.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Shared-Sites-Associated-Content.png "SXA Experience Editor Shared Sites, set up the associated content for the component")
*SXA Experience Editor Shared Sites, set up the associated content for the component*

Another thing you can do with shared sites is work with rendering variants. In the following screenshot, you can see that the *Contact* component in the *Experience Editor* has 2 available variants which come from the central repository that was established earlier.

![alt text](assets/images/sxa-basics/SXA-Experience-Editor-Shared-Sites-Rendering-Variants.png "SXA Experience Editor Shared Sites, this component has 2 rendering variants available from the central repository")
*SXA Experience Editor Shared Sites, this component has 2 rendering variants available from the central repository*

Another aspect of shared sites is that their *Page Designs* and *Partial Designs* are available to be used by other sites. Styles are also available from shared sites. As seen previously, when a component is selected in the *Experience Editor*, click on *More*, then *Edit component properties*. In here you can add classes that come from the central repository.
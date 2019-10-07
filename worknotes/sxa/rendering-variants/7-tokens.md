<summary>Part 7 - Tokens</summary>
<br />  

Link to YouTube video for this section [SXA Rendering Variants Part 7 - Tokens](https://youtu.be/0ziwN_F4Uww)

*Let's talk about rendering variant tokens*

*Tokens* are one of the options you will see when you try to insert a *Rendering Variant*. Tokens are useful for both editors and developers. There are situations where you don't want to render just a field, but you need to do some transformation on the values that are available in the sitecore items. *Tokens* allow you to developers to provide you with this transformation. The developers should provide a list of the available tokens. Tokens that are already in sitecore by default are; $Size, $FileTypeIcon, $id, $name

* $Size - Renders the size of a media item
* $FileTypeIcon - Renders a file type icon
* $id - Renders the id of an item
* $name - Renders the name of an item

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Tokens-Insert.png "SXA Rendering Variants Tokens, insert a token to a rendering variant")
*SXA Rendering Variants Tokens, insert a token to a rendering variant*

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Tokens-Example.png "SXA Rendering Variants Tokens, here is an example of a rendering variant set up with tokens")
*SXA Rendering Variants Tokens, here is an example of a rendering variant set up with tokens*

Here is sitecores documentation about how to [Create a Custom Token for a Rendering Variant](https://doc.sitecore.com/developers/sxa/18/sitecore-experience-accelerator/en/create-a-custom-token-for-a-rendering-variant.html)
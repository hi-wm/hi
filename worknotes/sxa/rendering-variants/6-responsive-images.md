<summary>Part 6 - Responsive Images</summary>
<br />  

Link to YouTube video for this section [SXA Rendering Variants Part 6 - Responsive Images](https://youtu.be/22IXpZtG1u8)

*SXA can render through a simnple image rendering field by providing the field of type that is image*

Out of the box, the image rendering in sitecore does not provide responsive image field rendering, but it can be set up! Within rendering variants, there is an *Image* type. If you right-click on *Image*, you can set up a *Responsive Image* rendering variant!

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Responsive-Images-Setup.png "SXA Rendering Variants Responsive Images, this is what it looks like to set up a responsive image rendering variant in sitecore")
*SXA Rendering Variants Responsive Images, this is what it looks like to set up a responsive image rendering variant in sitecore*

The settings in *Sizes* will be determined by UX / FED. Under the hood, sitecore is generating the correct syntax to markup the page to render images responsively. [Check out this link for more information about responsive images](https://alistapart.com/article/using-responsive-images-now). Sitecore will only download the image according to the breakpoint as defined by the source set of images.

Here is sitecores documentation about how to [Render Image Fields Using the Responsive Image Variant](https://doc.sitecore.com/developers/sxa/17/sitecore-experience-accelerator/en/render-image-fields-using-the-responsive-image-variant.html)
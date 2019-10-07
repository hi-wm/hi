<summary>Part 8 - Basics Revisited</summary>
<br />  

Link to YouTube video for this section [SXA Rendering Variants Part 8 - Basics Revisited](https://youtu.be/VwfcV6JLW1w)

*Let's revisit some basics of rendering variants*

In the first *Rendering Variants - Basics* video, the rendering variant types were not covered well, so let's do that now.

* Section - A wrapper that allows you to put additional elements inside of them. It will wrap any elements in a tag that you get to specify, it can have styles applied to it, and additional attributes.
* Field - The field will render your content according to the type itself i.e. an image field will render an image, rich-text will allow you to edit content, a title will render text
* Text - Variant text is for specifying text constants, i.e. *Author*
* Date - Will render the date and there are many date formats available
* HTML Tag - A set of self-closing HTML tags that cannot contain any other tags within it

Most of the rendering variant types have the ability to add *Data attributes* which will be added (inline) to the HTML Tag that is specified for the rendering variant. Some rendering variant types also have fields for Prefix or Suffix content which allows additional content to be defined before or after the element.

[Here is the complete list of Rendering Variants and what they do and are used for](https://doc.sitecore.com/developers/sxa/17/sitecore-experience-accelerator/en/create-a-rendering-variant.html)
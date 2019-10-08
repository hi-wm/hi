<summary>Customize the XA RTE Profile</summary>
<br />  

Link to YouTube video for this section [Customize the XA RTE Profile](https://youtu.be/SZvIOXjOn8A)

*How to add different classes to our text directly from the RTE editor*

This is 🔥, just follow this path in your folder tree ```... Settings > Html Editor Profiles > Right Text XA > Paragraphs``` and add a new type, name it whatever is appropriate. In the *Content* section of the screen for the new RTE style, in the *Data* section, define the *Header* and *Value* fields. *Header* is the name of the style, *Value* is the HTML wrapper including any classes you would like to apply.

Another way to add styles to the RTE is to add values to the dropdown list for the RTE in the backend, then add the CSS to the default.css file associated with the RTE.

I'm not convinced that either way... well maybe the first approach seems more reasonable / future proof, but here is an additional reading:

Approach #2, touching core files... [Adding Custom CSS Class to Sitecore RTE](https://therelentlessfrontend.com/2018/03/15/adding-custom-css-class-to-sitecore-rich-text-editor/)
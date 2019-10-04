<summary>Part 3 - Querying Content</summary>
<br />  

*Querying Content in Rendering Variants*

We've covered passing through links to get content from content items that are linked to the items that are being rendered. But not all links are rendered this way. Sometimes there needs to be field comparison to get some related content to the render. That is what we will be learning here. To build this out, there has been an additional field added to *Page* ```... > Templates > Project > Tenant > Page```. The field is named *RelatedProducts* of type *Treelist* with a dynamic source, in this case *query:$home/Products*.

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Querying-Content-Dynamic-Query-Field.png "SXA Rendering Variants Querying Content, dynamic query field with name, type, and source highlighted")
*SXA Rendering Variants Querying Content, dynamic query field with name, type, and source highlighted*


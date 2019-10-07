<summary>Part 3 - Querying Content</summary>
<br />  

Link to YouTube video for this section [SXA Rendering Variants Part 3 - Querying Content](https://youtu.be/BsamkDxp_dI)

*Querying Content in Rendering Variants*

We've covered passing through links to get content from content items that are linked to the items that are being rendered. But not all links are rendered this way. Sometimes there needs to be field comparison to get some related content to the render. That is what we will be learning here. To build this out, there has been an additional field added to *Page* ```... > Templates > Project > Tenant > Page```. The field is named *RelatedProducts* of type *Treelist* with a dynamic source, in this case *query:$home/Products*.

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Querying-Content-Dynamic-Query-Field.png "SXA Rendering Variants Querying Content, dynamic query field with name, type, and source highlighted")
*SXA Rendering Variants Querying Content, dynamic query field with name, type, and source highlighted*

The next step is to create a rendering variant, again using the *Page Content* component. Finally, the presenter admits that you should not continue adding items under this component type, but that you should in fact clone it to use for your rendering variant needs. But of course that's not what we are gonna do in this video! Simply ```Insert > Variant Definition```, name the thing (in this case *Related Products*), then in the *Related Products* variant definition, right-click on its name then ```Insert > Text``` and name it *Title*. Change the *Tag* to an ```h3``` and add some *Text* (Related Products?).

The variant definition is able to render out and iterate through content that has been defined within pages and posts. In the *Related Products* rendering variant, right-click then ```Insert > Reference``` and name it the same as the field that you would like to target i.e. *RelatedProducts* (this is the field that has been defined in the video). The presenter is always shuffling around the sub-components as they are added, is this presentation related, or is there another purpose?

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Querying-Content-Sorting-Sub-Components.png "SXA Rendering Variants Querying Content, sort your sub-components, because the presenter did!")
*SXA Rendering Variants Querying Content, sort your sub-components, because the presenter did!*

Of course, don't forget to add inline styling to your rendering variants, becuase that's what you should do. Now that you have thte variant definition set up, you can add additional fields (according to those that exist in the definition that you are referencing), i.e. render a field and reference it's name to target it. In the *Variant Details* section of your new field, set a *Tag* type if needed (the *Tag* refers to HTML i.e. h4). You can also ```Insert > HTML Tag``` if you need, for example, a horizontal rule.

Now comes the fun part, and the purpose of this chapter on rendering variants, adding a query. Right-click on the reference within the *Rendering Variant* and ```Insert > Query```. In the *Variant Details* section of ttthe *Query*, build your query ```query:./*``` < selects immediate children, then right-click on the new *Query* and ```Insert > Field``` and name it according to a field that exists in the item you are referencing, in this case, *Title*. What we have looks like the following:

![alt text](assets/images/sxa-rendering-variants/SXA-Rendering-Variants-Querying-Content-Query-Structure.png "SXA Rendering Variants Querying Content, this how the rendering variant for a query is structured in the project folder tree")
*SXA Rendering Variants Querying Content, this how the rendering variant for a query is structured in the project folder tree*

If you do the query right, you will get the right results. And... the above query does not get the intended results. It grabs all children when it should be more discriminate. Let's update that query to ```query:./*[@@templatename!='Page Data']```. That query can be found within sitecore, so if you don't remember the syntax or the precise query, simply searching for children at the top of the folder tree will reveal all items that refer to children and in those results you can find at least one item that has the aforementioned query already built. If you need more complex queries, you are SOL. But that query will get the children and leave out the *Page Data*, which is something that you may not need.

The remaining half of the video (from ~13:00) repeats the above steps, but builds another query based on *Taggable* content using a *token*. The entirety of this process is outlined in the link below.

Here is a link to the sitecore documentation about [Using a Query to Render Items](https://doc.sitecore.com/developers/sxa/18/sitecore-experience-accelerator/en/walkthrough--using-a-query-to-render-items.html)
<summary>Search Non Page Items in SXA</summary>
<br />  

Link to YouTube video for this section [Search Non Page Items in SXA](https://youtu.be/sonYfC9I8eU)

*The problem with SXA solo search is that it only searches content that's coming from pages or media types*

The example scenario is a few PDF items that aren't able to be included in search results. The proposed solution is as follows:

* Create a new search aggregator ```TAMM.XA.Foundation.Search```

* Update the sxacontent computed field in ```App_Config/Include/Z.Foundation.Overrides/Sitecore.XA.Foundation.Search.Solr.config``` to use this aggregator ```TAMM.XA.Foundation.Search``` instead of the default

* ```<field fieldName="sxacontent" returnType="textCollection" type="TAMM.XA.Foundation.Search.AggregatedContent, TAMM.XA.Foundation.Search"> <mediaIndexing ref="contentSearch/indexConfigurations/defaultSolrIndexConfiguration/mediaIndexing"/></field>```

This is another backend heavy section. Watch the video
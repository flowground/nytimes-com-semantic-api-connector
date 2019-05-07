# ![LOGO](logo.png) Semantic **flow**ground Connector

## Description

A generated **flow**ground connector for the Semantic API (version 2.0.0).

Generated from: https://api.apis.guru/v2/specs/nytimes.com/semantic_api/2.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:43:21+03:00

## API Description

The Semantic API complements the Articles API. With the Semantic API, you get access to the long list of people, places, organizations and other locations, entities and descriptors that make up the controlled vocabulary used as metadata by The New York Times (sometimes referred to as Times Tags and used for Times Topics pages).

The Semantic API uses concepts which are, by definition, terms in The New York Times controlled vocabulary. Like the way facets are used in the Articles API, concepts are a good way to uncover articles of interest in The New York Times archive, and at the same time, limit the scope and number of those articles. The Semantic API maps to external semantic data resources, in a fashion consistent with the idea of linked data. The Semantic API also provides combination and relationship information to other, similar concepts in The New York Times controlled vocabulary.


## Authorization

Supported authorization schemes:
- API Key
## Actions

### get_name__concept_type___specific_concept__json

#### Input Parameters
* `concept-type` - _required_ - The type of the concept, used for Constructing a Semantic API Request by Concept Type and Specific Concept Name. The parameter is defined as a name-value pair, as in "concept_type=[nytd_geo|nytd_per|nytd_org|nytd_des]".

    Possible values: nytd_geo, nytd_per, nytd_org, nytd_des.
* `specific-concept` - _required_ - The name of the concept, used for Constructing a Semantic API Request by Concept Type and Specific Concept Name. The parameter is defined in the URI path, as the element immediately preceding ".json" like with "Baseball.json".

* `fields` - _optional_ - "all" or comma-separated list of specific optional fields: pages, ticker_symbol, links, taxonomy, combinations, geocodes, article_list, scope_notes, search_api_query

Optional fields are returned in result_set. They are briefly explained here:

pages: A list of topic pages associated with a specific concept.
ticker_symbol: If this concept is a publicly traded company, this field contains the ticker symbol.
links: A list of links from this concept to external data resources.
taxonomy: For descriptor concepts, this field returns a list of taxonomic relations to other concepts.
combinations: For descriptor concepts, this field returns a list of the specific meanings tis concept takes on when combined with other concepts.
geocodes: For geographic concepts, the full GIS record from geonames.
article_list: A list of up to 10 articles associated with this concept.
scope_notes: Scope notes contains clarifications and meaning definitions that explicate the relationship between the concept and an article.
search_api_query: Returns the request one would need to submit to the Article Search API to obtain a list of articles annotated with this concept.

    Possible values: all, pages, ticker_symbol, links, taxonomy, combinations, geocodes, article_list, scope_notes, search_api_query.
* `query` - _required_ - Precedes the search term string. Used in a Search Query. Except for &lt;specific_concept_name&gt;, Search Query will take the required parameters listed above (&lt;concept_type&gt;, &lt;concept_uri&gt;, &lt;article_uri&gt;) as an optional_parameter in addition to the query=&lt;query_term&gt;.

### get_search_json

#### Input Parameters
* `query` - _required_ - Precedes the search term string. Used in a Search Query. Except for &lt;specific_concept_name&gt;, Search Query will take the required parameters listed above (&lt;concept_type&gt;, &lt;concept_uri&gt;, &lt;article_uri&gt;) as an optional_parameter in addition to the query=&lt;query_term&gt;.
* `offset` - _optional_ - Integer value for the index count from the first concept to the last concept, sorted alphabetically. Used in a Search Query. A Search Query will return up to 10 concepts in its results.
* `fields` - _optional_ - "all" or comma-separated list of specific optional fields: pages, ticker_symbol, links, taxonomy, combinations, geocodes, article_list, scope_notes, search_api_query

Optional fields are returned in result_set. They are briefly explained here:

pages: A list of topic pages associated with a specific concept.
ticker_symbol: If this concept is a publicly traded company, this field contains the ticker symbol.
links: A list of links from this concept to external data resources.
taxonomy: For descriptor concepts, this field returns a list of taxonomic relations to other concepts.
combinations: For descriptor concepts, this field returns a list of the specific meanings tis concept takes on when combined with other concepts.
geocodes: For geographic concepts, the full GIS record from geonames.
article_list: A list of up to 10 articles associated with this concept.
scope_notes: Scope notes contains clarifications and meaning definitions that explicate the relationship between the concept and an article.
search_api_query: Returns the request one would need to submit to the Article Search API to obtain a list of articles annotated with this concept.

    Possible values: all, pages, ticker_symbol, links, taxonomy, combinations, geocodes, article_list, scope_notes, search_api_query.

## License

**flow**ground :- Telekom iPaaS / nytimes-com-semantic-api-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.

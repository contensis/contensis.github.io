# Overview

A Query tree structure, along with order and paging specifiers, allows a search to be performed against indexed documents held in ElasticSearch. The query API allows any required sub-query structure to be defined and a comprehensive selection of Operators enable individual field level evaluation.

The C# example below demonstrates a search with an order-by clause and paging options:

{% method -%}
##### Example

This example demonstrates a search with an order-by clause and paging options:

{% sample lang="cs" -%}
```cs
var query = new Query(
    Op.Contains("title", "Batman"),
    Op.GreaterThan("lengthRunTime", 200)
);
 
query.OrderBy.Add("-yearOfRelease")
query.PageIndex = 1;
query.PageSize = 50;
 
var results = client.Entries.Search(query);
```

{% sample lang="js" -%}
```js
// TODO

```

{% sample lang="http" -%}
```http
POST: /api/search

{
    "pageIndex": 1,
    "pageSize": 50,
    "orderBy": [{
        "desc": "yearOfRelease"
    }],
    "where": [{
        "field": "title",
        "contains": "Batman"
    }, {
        "field": "lengthRunTime",
        "greaterThan": 200
    }]
}
```

{% endmethod %}


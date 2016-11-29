# Search

A Query tree structure, along with order and paging specifiers, allows a search to be performed against indexed documents held in ElasticSearch. The query API allows any required sub-query structure to be defined and a comprehensive selection of Operators enable individual field level evaluation.

## Queries

{% method -%}

This example demonstrates a simple search with default ordering and paging options:

{% sample lang="cs" -%}
Synchronous
```cs
var query = new Query(
    Op.Contains("title", "Batman"),
    Op.GreaterThan("lengthRunTime", 200)
);

// Execute the search
var results = client.Entries.Search(query);
```

Asynchronous

```cs
// Execute the search asynchronously
var results = await client.Entries.SearchAsync(query);
```

{% sample lang="js" -%}
```js
// TODO

```

{% sample lang="http" -%}
```http
POST: /api/search

{
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

## Sub-queries

A sub-query is a query within another query that is used as a condition to further restrict the results. Effectively they are defined by an explicit nesting of [logical operators](/common/query-api/query-operators.md#logical-operators).

{% method -%}

This example demonstrates a simple search with a sub-query:

{% sample lang="cs" -%}
Synchronous
```cs
var query = new Query(
    Op.Contains("title", "Batman"),
    Op.Or(
        Op.GreaterThan("yearOfRelease", 1960),
        Op.Contains("synopsis", "gotham")
    )
);
```

{% sample lang="js" -%}
```js
// TODO

```

{% sample lang="http" -%}
```json
{
    "where": [
        {
            "field": "title",
            "contains": "Batman"
        },
        {
            "or": [
                {
                    "field": "yearOfRelease",
                    "greaterThan": 1960
                },
                {
                    "field": "synopsis",
                    "contains": "gotham"
                }
            ]
        }
    ]
}
```

{% endmethod %}

## Ordering

Results can be ordered by one or more fields in an ascending or descending direction. Order clauses are prioritised in the order that they are added. By default, if no order clauses are specified then the entry results are ordered by the TitleField [^1] in an ascending direction.

{% method -%}

{% sample lang="cs" -%}
Order by 'yearOfRelease'.

```cs
query.OrderBy.Add("yearOfRelease")
```

Order by 'yearOfRelease' in a descending direction using the '-' token.

```cs
query.OrderBy.Add("-yearOfRelease")
```

Multiple order clauses.

```cs
query.OrderBy.Add("title", "-yearOfRelease")
```

{% sample lang="js" -%}
```js
// TODO

```

{% sample lang="http" -%}
Order by 'yearOfRelease'.

```json
{
    "orderBy": [{
        "asc": "yearOfRelease"
    }],
}
```

Order by 'yearOfRelease' in a descending direction using the '-' token.

```json
{
    "orderBy": [{
        "desc": "yearOfRelease"
    },],
}
```

Order by 'yearOfRelease' in a descending direction using the '-' token.

```json
{
    "orderBy": [{
        "desc": "yearOfRelease"
    },],
}
```

{% endmethod %}

## Paging

Paging allows the number of results to be restricted to a defined count so that the results are easier to handle and ensures a response is returned quickly. The page number can also be specified to allow which set of results is to be returned.

{% method -%}

{% sample lang="cs" -%}

```cs
{
    // Create a query
    var query = new Query(
        Op.EqualTo("contentTypeId", "film"));
    
    // Set the paging options
    query.PageSize = 50; 

    // Get the 2nd result set
    query.PageIndex = 1; 
}
```

{% sample lang="http" -%}

```json
{
    "pageSize": 50,
    "pageIndex": 1
}
```

{% endmethod %}


## Specifying fields

### System fields

The fields for search generally match the names defined in the entry structure, for example 'id', 'contentTypeId', 'projectId', etc. Field data not held at the root of the entry, such as the version information are accessed using a dot notation, i.e. 'version.versionNo', 'version.published', etc.

The 'titleField' field is a dynamic value, determined by the 'Title Field' value in the Content Type.

### Data fields

Fields defined in the Content Type for the entry can be accessed by their API id.

## Full example

The example below combines the ordering and paging concepts:

{% method -%}

{% sample lang="cs" -%}
```cs
var query = new Query(
    Op.Contains("title", "Batman"),
    Op.GreaterThan("lengthRunTime", 200)
);
 
query.OrderBy.Add("-yearOfRelease")
query.PageIndex = 1;
query.PageSize = 50;
 
// Execute the search
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

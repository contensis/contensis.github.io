# List Entries by Content Types


- List(string contentTypeId, string languageCode, PageOptions pageOptions = null, SortFields sortFields = null, int entryLinkDepth = 0)

- ListAsync(string contentTypeId, string languageCode, PageOptions pageOptions = null, SortFields sortFields = null, int entryLinkDepth = 0); 

- List(string contentTypeId, string languageCode, PageOptions pageOptions, SortFields sortFields, string[] fields, int entryLinkDepth = 0)

- ListAsync(string contentTypeId, string languageCode, PageOptions pageOptions, SortFields sortFields, string[] fields, int entryLinkDepth = 0)

- List(string contentTypeId, string languageCode, PageOptions pageOptions, string[] fields, int entryLinkDepth = 0)

- ListAsync(string contentTypeId, string languageCode, PageOptions pageOptions, string[] fields, int entryLinkDepth = 0)

- List(string contentTypeId, string languageCode, string[] fields, int entryLinkDepth = 0)

- ListAsync(string contentTypeId, string languageCode, string[] fields, int entryLinkDepth = 0)

- List(string contentTypeId, PageOptions pageOptions = null, SortFields sortFields = null, int entryLinkDepth = 0)

- ListAsync(string contentTypeId, PageOptions pageOptions = null, SortFields sortFields = null, int entryLinkDepth = 0)

- List(string contentTypeId, string[] fields, int entryLinkDepth = 0)

- ListAsync(string contentTypeId, string[] fields, int entryLinkDepth = 0)

- List(string contentTypeId, PageOptions pageOptions, string[] fields, int entryLinkDepth = 0)

- ListAsync(string contentTypeId, PageOptions pageOptions, string[] fields, int entryLinkDepth = 0)

- List(string contentTypeId, PageOptions pageOptions, SortFields sortFields, string[] fields, int entryLinkDepth = 0)

- ListAsync(string contentTypeId, PageOptions pageOptions, SortFields sortFields, string[] fields, int entryLinkDepth = 0)


## Suggested Change

{% method -%}
{% sample lang="cs" -%}

```cs
public PagedList<Entry> List(string contentTypeId)
{
}

public PagedList<Entry> List(EntryListOptions options)
{
}

var options = new EntryListOptions
{
    PageOptions = new PageOptions(0, 50),
    Fields = new [] { "field1", "field2", "field2" },
    Order = new Order(),
    DeliveryContext = DeliveryContext.Live
    ...
}
```
{% endmethod %}

## REST

**List**  
{projectId}/contenttypes/{contentTypeId}/entries

> string contentTypeId,  
> int pageIndex = 0,  
> int pageSize = 20,  
> string sort = "",  
> string fields = "",  
> int entryLinkDepth = 0,  
> bool resolveLinks=true

**List**  
{projectId}/contenttypes/{contentTypeId}/entries/{version?}

> string contentTypeId,  
> string version = null,  
> string lang = null,  
> int pageIndex = 0,  
> int pageSize = 20,  
> string sort = "",  
> string fields = "",  
> int entryLinkDepth = 0,  
> bool resolveLinks=true  

**List**  
{projectId}/entries

> int pageIndex = 0,  
> int pageSize = 20,  
> string sort = "",  
> string fields = "",   
> string dataFormat = "",   
> int entryLinkDepth = 0,  
> bool resolveLinks = true  

**ListLatest**  
{projectId}/entries/latest

> int pageIndex = 0,  
> int pageSize = 20,  
> string sort = "",  
> string fields = "",  
> string dataFormat = "",  
> int entryLinkDepth = 0,  
> bool resolveLinks = true  

**ListPublished**  
{projectId}/entries/published

> int pageIndex = 0,  
> int pageSize = 20,  
> string sort = "",  
> string fields = "",  
> string dataFormat = "",  
> int entryLinkDepth = 0,  
> bool resolveLinks = true  

## Changes

- Change 'sort' to order - to put it inline
- Move 'dataFormat' to the management API
- Move 'resolveLinks' to the management API
- Move 'resolveLinks' to the management API
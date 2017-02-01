# List entries

Requesting a list of entries can be achieved by using one of the `List` method overloads.

- [List(PageOptions pageOptions)](#list)
- [ListAsync(PageOption pageOptions)](#list-async)
- [List(string contentTypeId, PageOptions pageOptions)](#list-by-content-type)
- [ListAsync(string contentTypeId, PageOptions pageOptions)](#list-by-content-type-async)
- [List(string contentTypeId, PageOptions pageOptions, IList<string> order)](#list-by-content-type-with-paging-and-ordering)
- [ListAsync(string contentTypeId, PageOptions pageOptions, IList<string> order)](#list-by-content-type-with-paging-and-ordering-asynchronously)
- [List(EntryListOptions listOptions)](#list-with-options-object)
- [ListAsync(EntryListOptionslistOptions)](#list-with-options-object-asynchronously)

## List

Lists entries for all content types, with paging.

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public PagedList<Entry> List(PageOptions pageOptions = null)
{
}
```
{% endmethod %}

### Parameters

*pageOptions*
> Type: [PageOptions](/delivery-api/model/dotnet/pageoptions-dotnet.md)   
> Paging options for specify the page index and size.

### Remarks

The default for the pageOptions is PageSize: 20, PageIndex: 0.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Create a client
var client = ContensisClient.Create();

// Get all entries with the default paging options
var entries = client.Entries.List();

// Get all entries with specified paging options
var entries = client.Entries.List(new PageOptions(3, 10));
```
{% endmethod %}

---



## List async

Lists entries for all content types asynchronously, with paging.

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public Task<PagedList<Entry>> List(PageOptions pageOptions = null)
{
}
```
{% endmethod %}

### Parameters

*pageOptions*
> Type: [PageOptions](/delivery-api/model/dotnet/pageoptions-dotnet.md)   
> Paging options for specifying the page index and size.

### Remarks

The default for the PageOptions is PageSize: 20, PageIndex: 0.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Create a client
var client = ContensisClient.Create();

// Get all entries with the default paging options
var entries = await client.Entries.ListAsync();

// Get all entries with specified paging options
var entries = await client.Entries.ListAsync(new PageOptions(3, 10));
```
{% endmethod %}

---





## List by content type

Lists entries for a specific content type.

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public PagedList<Entry> List(string contentTypeId, PageOptions pageOptions = null)
{
}
```
{% endmethod %}

### Parameters

*contentTypeId*
> Type: `string`  
> The id of the content type to restrict the entries by.

*pageOptions*
> Type: [PageOptions](/delivery-api/model/dotnet/pageoptions-dotnet.md) 
> Paging options for specifying the page index and size.

### Remarks

The default for the PageOptions is PageSize: 20, PageIndex: 0.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Create a client
var client = ContensisClient.Create();

// Get entries with the default paging options
var entries = client.Entries.List("movie");

// Get all entries with specified paging options
var entries = client.Entries.List("movie", new PageOptions(3, 10));
```
{% endmethod %}

---





## List by content type async

Lists entries for a specific content type.

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public Task<PagedList<Entry>> ListAsync(string contentTypeId, PageOptions pageOptions = null)
{
}
```
{% endmethod %}

### Parameters

*contentTypeId*
> Type: `string`  
> The id of the content type to restrict the entries by.

*pageOptions*
> Type: [PageOptions](/delivery-api/model/dotnet/pageoptions-dotnet.md)  
> Paging options for specifying the page index and size.

### Remarks

The default for the PageOptions is PageSize: 20, PageIndex: 0.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Create a client
var client = ContensisClient.Create();

// Get entries with the default paging options
var entries = await client.Entries.ListAsync("movie");

// Get all entries with specified paging options
var entries = await client.Entries.ListAsync("movie", new PageOptions(3, 10));
```
{% endmethod %}

---



## List by content type with paging and rdering

Lists entries for a specific content type, with paging and field order configuration.

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public PagedList<Entry> List(string contentTypeId, PageOptions pageOptions, IList<string> order)
{
}
```
{% endmethod %}

### Parameters

*contentTypeId*
> Type: `string`  
> The id of the content type to restrict the entries by.

*pageOptions*
> Type: PageOptions  
> Paging options for specifying the page index and size.

*order*
> Type: `IList<string>`  
> Options for specifying the result ordering.

### Remarks

The default for the PageOptions is PageSize: 20, PageIndex: 0.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Create a client
var client = ContensisClient.Create();

// Get all entries with the default paging options
var entries = client.Entries.List("film", new PageOptions(3, 10), 
    new [] {  } );
```
{% endmethod %}

---



## List by content type with paging and sorting asynchronously

Lists entries for a specific content type, with paging and field sort configuration.

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public Task<PagedList<Entry>> ListAsync(string contentTypeId, PageOptions pageOptions, SortFields sortFields)
{
}
```
{% endmethod %}

### Parameters

*contentTypeId*
> Type: `string`  
> The id of the content type to restrict the entries by.

*pageOptions*
> Type: PageOptions  
> Paging options for specifying the page index and size.

*sortFields*
> Type: SortFields  
> Options for specifying the result ordering.

### Remarks

The default for the PageOptions is PageSize: 20, PageIndex: 0.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Create a client
var client = ContensisClient.Create();

// Get all entries with the default paging options
var entries = await client.Entries.ListAsync("film", new PageOptions(3, 10), 
    new SortFields { new SortField("title", SortField.FieldSortDirection.Descending) });
```
{% endmethod %}

---



## List with options object

Lists entries using an EntryListOptions object to allow more granular control of entries being returned.

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public PagedList<Entry> List(EntryListOptions listOptions)
{
}
```
{% endmethod %}

### Parameters

*listOptions*
> Type: `EntryListOptions`
> Allows all parameters to be optional set and exposes less commonly used parameters.

### Remarks

The default for the PageOptions is PageSize: 20, PageIndex: 0.

The default for the VersionStatus parameter is `VersionStatus.Published`.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Create a client
var client = ContensisClient.Create();

// Use the list options to filter the entry listing
var entries = client.Entries.List(new EntryListOptions{
    ContentTypeId = "film",
    PageOptions = new PageOptions(3, 10),
    Order = new[] { "title", "-sys.version.created" },
    Language = "fr-fr",
    EntryLinkDepth = 5,
    Fields = new[] { "title", "description", "releaseDate", "coverImage" }
});
```
{% endmethod %}

---


## List with options object asynchronously

Lists entries using an EntryListOptions object to allow more granular control of entries being returned.

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public Task<PagedList<Entry>> ListAsync(EntryListOptions listOptions)
{
}
```
{% endmethod %}

### Parameters

*listOptions*
> Type: `EntryListOptions`  
> Allows all parameters to be optional set and exposes less commonly used parameters.

### Remarks

The default for the PageOptions is PageSize: 20, PageIndex: 0.

The default for the VersionStatus parameter is `VersionStatus.Published`.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Create a client
var client = ContensisClient.Create();

// Use the list options to filter the entry data
var entries = await client.Entries.ListAsync(new EntryListOptions{
    ContentTypeId = "film",
    PageOptions = new PageOptions(3, 10),
    Order = new[] { "title", "-sys.version.created" },
    VersionStatus = VersionStatus.Latest,
    Language = "fr-fr",
    EntryLinkDepth = 5,
    Fields = new { "title", "description", "releaseDate", "coverImage" }
});
```
{% endmethod %}

---
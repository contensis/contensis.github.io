# Getting an entry

Requesting an individual entry can be achieved by using one of the `Get` method overloads. Additionally 

- [Get(Guid, String, Integer))](#get-by-guid-id)
- [Get(String, String, Integer)](#get-by-string-id)
- [GetAsync(Guid, String, Integer)](#get-by-guid-id-async)  
- [GetAsync(String, String, Integer)](#get-by-string-id-async)


## Get by guid id

Gets an entry by its Guid identifier

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public Entry Get(Guid id, string languageCode = null, entryLinkDepth = 0)
{
}
```
{% endmethod %}

### Parameters

*id*
> Type: `Guid`  
> The id of the Entry.

*languageCode*
> Type: `string`  
> The specified language variation for the entry. If no value is provided then the project default language is used.

*entryLinkDepth*
> Type: `integer`  
> The depth at which to resolve the full entry data for a linked entry. The max depth that can be specified is 10 - larger values will be handled as being 10. By default no entry data is resolved.

### Remarks

Returns *null* if an entry with an id matching the specified id does not exist.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Create a client
var client = ContensisClient.Create();

// Get the french variation of the film entry and resolve links to a depth of 3
Entry film = client.Entries.Get(filmGuid, "fr-fr", 3);
```
{% endmethod %}

---

## Get by string id

Gets an entry by its identifier

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public Entry Get(string id, string languageCode = null, entryLinkDepth = 0)
{
}
```
{% endmethod %}

### Parameters

*id*
> Type: `string`  
> The id of the Entry.

*languageCode*
> Type: `string`  
> The specified language variation for the entry. If no value is provided then the project default language is used.

*entryLinkDepth*
> Type: `integer`  
> The depth at which to resolve the full entry data for a linked entry. The max depth that can be specified is 10 - larger values will be handled as being 10. By default no entry data is resolved.

### Remarks

Returns *null* if an entry with an id matching the specified id does not exist. If the id string is not a valid `Guid` format then an exception will be thrown.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Create a client
var client = ContensisClient.Create();

// Get the french variation of the film entry and resolve links to a depth of 3
Entry film = client.Entries.Get("456e5f2a-a1cf-4520-a46c-e5f22ed299e8", "fr-fr", 3);
```
{% endmethod %}

---

## Get by guid id async

Gets an entry by its Guid identifier asynchronously

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public async Task<Entry> GetAsync(Guid id, string languageCode = null, entryLinkDepth = 0)
{
}
```
{% endmethod %}

### Parameters

*id*
> Type: `Guid`  
> The id of the Entry.

*languageCode*
> Type: `string`  
> The specified language variation for the entry. If no value is provided then the project default language is used.

*entryLinkDepth*
> Type: `integer`  
> The depth at which to resolve the full entry data for a linked entry. The max depth that can be specified is 10 - larger values will be handled as being 10. By default no entry data is resolved.

### Remarks

Returns *null* if an entry with an id matching the specified id does not exist.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Create a client
var client = ContensisClient.Create();

// Get the french variation of the film entry and resolve links to a depth of 3
Entry film = await client.Entries.GetAsync(filmGuid, "fr-fr", 3);
```
{% endmethod %}

---

## Get by string id async

Gets an entry by its String identifier asynchronously

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public async Task<Entry> GetAsync(string id, string languageCode = null, entryLinkDepth = 0)
{
}
```
{% endmethod %}

### Parameters

*id*
> Type: `string`  
> The id of the Entry.

*languageCode*
> Type: `string`  
> The specified language variation for the entry. If no value is provided then the project default language is used.

*entryLinkDepth*
> Type: `integer`  
> The depth at which to resolve the full entry data for a linked entry. The max depth that can be specified is 10 - larger values will be handled as being 10. By default no entry data is resolved.

### Remarks

Returns *null* if an entry with an id matching the specified id does not exist. If the id string is not a valid `Guid` format then an exception will be thrown.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Create a client
var client = ContensisClient.Create();

// Get the french variation of the film entry and resolve links to a depth of 3
Entry film = await client.Entries.GetAsync("456e5f2a-a1cf-4520-a46c-e5f22ed299e8", "fr-fr", 3);
```
{% endmethod %}

---
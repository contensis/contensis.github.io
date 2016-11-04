# Entry Methods

## Get

Gets a field from an entry by *fieldName* and returns a dynamic object instance. 

### Syntax

{% method -%}
{% sample lang="cs" -%}
```cs
public dynamic Get(string fieldName)
{
}
```
{% endmethod %}

### Parameters

*fieldName*
> Type: string  
> The name of the requested field

### Remarks

Returns *null* if the field is not found or if the field value is null.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Get the title field as dynamic
dynamic title = entry.Get("title")
```
{% endmethod %}

---

## Get`<T>`

Gets a field from an entry by *fieldName* and returns a typed object instance.

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public T Get<T>(string fieldName)
{
}
```
{% endmethod %}

### Parameters

*T*
> The type to attempt to cast the field data to

*fieldName*
> Type: string  
> The name of the requested field

### Remarks

If the API cannot successfully cast or convert the field value then it will return the default for the specified type. Requesting field values by the wrong type will __not__ result in exceptions being thrown.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
// Get the title field as defined type
string title = entry.Get<string>("title")
```
{% endmethod %}

---

## HasValue

Determines whether the field exists and the value is not null.

### Syntax

{% method -%}
{% sample lang="cs" -%}

```cs
public bool HasValue(string fieldName)
{
}
```
{% endmethod %}

### Parameters

*fieldName*
> Type: string  
> The name of the field to check

### Return Value
> Type: boolean  
> __true__ if the field exists and is not null, otherwise __false__


### Remarks

If the *fieldName* is not defined in the content type that the entry is based on then it will return null.

### Examples

{% method -%}
{% sample lang="cs" -%}
```cs
if (entry.HasValue("title"))
{
    // Get the location field as type
    Location title = entry.Get<Location>("filmingLocation")
}
```
{% endmethod %}
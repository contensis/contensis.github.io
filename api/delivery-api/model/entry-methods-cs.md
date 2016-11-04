# Entry Methods

## Get

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

{% method -%}
{% sample lang="cs" -%}

### Syntax

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

{% method -%}
{% sample lang="cs" -%}

### Syntax

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
# Composed fields

The `ComposedField` type contains the data that the [Composer editor](https://contensis.github.io/docs/content-types/field-editors/editor-composer.html) defines. It is a read-only list of `ComposedFieldItem` instances, which expose a *Type* property and *Value* methods. The *Value* methods return the data for the field. The *Type* property is a name given to an *allowed field type validation* defined in the content type that the entry is based on.

An *allowed field type* is essentially any standard field (such as Image, Heading, Location, etc.) that restricts what types of field can be added to a `ComposedField`.

For example, an *allowed field* could be defined with a type of *Heading* and given a type name of "mainHeading" or with a type of *Image* and given a type name of "bannerImage". There can be multiple *allowed fields* based on the same type, but a `ComposedField` cannot contain other `ComposedField` fields.

# ComposedFieldItem methods

The methods on the `ComposedFieldItem` enable the value of the field to be retrieved.

{% method -%}

## Value()

Returns the field item value as a `dynamic` object.

{% sample lang="cs" -%}

```cs
public dynamic Value()
{
}
```

{% endmethod %}

### Remarks

Complex objects will be returned as dynamic [ExpandoObject](https://msdn.microsoft.com/en-us/library/system.dynamic.expandoobject(v=vs.110).aspx instances.

{% method -%}

### Example

{% sample lang="cs" -%}

```cs
// Get the ComposedField instance
var composed = film.Get<ComposedField>("synopsis");

// Get the first item value
dynamic quote = composed[0].Value();
```

{% endmethod %}

---

{% method -%}

## Value`<T>`()

Returns the field item value as `T`.

{% sample lang="cs" -%}

```cs
public T Value<T>()
{
}
```

{% endmethod %}

### Parameters

*T*
> The type to attempt to cast the field data to.

### Remarks

For complex objects, if the type of T does not match the value type, then either a null value will be returned or an object of type T is returned with no property values.

{% method -%}

### Example

{% sample lang="cs" -%}

```cs
// Get the ComposedField instance
var composed = film.Get<ComposedField>("synopsis");

// Get the first item value as a Quote object
var quote = composed[0].Value<Quote>();
```

{% endmethod %}

---

## Example

The example below shows how a composed field with different field types can be rendered.

{% method -%}
{% sample lang="cs" -%}

```cs
@using Zengenti.Contensis.Delivery

@{
    // Create an api client
    var client = ContensisClient.Create();

    // Get an entry
    var filmEntry = client.Entries.Get("1fdbdac6-a8fe-4a86-9c1a-42238fcb47f1");

    // Get the synopsis field as a ComposedField type
    var synopsis = filmEntry.Get<ComposedField>("synopsis");
}

<div>

@foreach(ComposedFieldItem item in synopsis)
{
    // Loop through the ComposedFieldItems in the ComposedField and render the items
    //

    if (item.Type == "mainHeading")
    {
        <h1>@item.Value()</h1>
    }

    if (item.Type == "subHeading")
    {
        <h2>@item.Value()</h2>
    }

    if (item.Type == "markup")
    {
        <div>@Html.Raw(@item.Value<string>())</div>
    }

    if (item.Type == "quote")
    {
        var filmQuote = item.Value<Quote>();

        <blockquote cite="@filmQuote.Source">
            @filmQuote.Text
        </blockquote>
    }
}

</div>

```
{% endmethod %}

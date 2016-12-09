# Quote

The Quote type represents a section of referenced text from an external source.

## Properties

| Property | Type | Description |
| :------- | :--- | :---------- |
| Text | `string` | The quote text |
| Source | `string` | The source of the quote |

## Validation

TODO: Confirm if a Validation should exist

## Examples

{% method -%}

##### Get a Source field object

{% sample lang="cs" -%}

```cs
@{
    // Retrieve a film by it's ID.
    var film = client.Get("3bb72e32-1fc7-4289-bf65-60a5b8ce1f78");

    // Get the field value as a DateRange instance.
    var filmQuote = film.Get<Quote>("memorableQuote");
}

<blockquote cite="@filmQuote.Source">
    @filmQuote.Text
</blockquote>
```
{% endmethod %}
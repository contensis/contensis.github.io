# DateRange

## Overview

The Quote type represents a section of referenced text from an external source.

## Properties

| Property | Type | Description |
| :------- | :--- | :---------- |
| Text | `string` | The quote text |
| Source | `string` | The source of the quote |

## Validation

## Examples

{% method -%}

##### Get a Source field object

{% sample lang="cs" -%}

```cs
@{
    // Retrieve a film by it's ID.
    var film = client.Get("");

    // Get the field value as a DateRange instance.
    var filmingPeriod = film.Get<DateRange>("filmingPeriod");
}

<div class="start">@filmingPeriod.From</div>

<div class="end">@filmingPeriod.To</div>
```
{% endmethod %}
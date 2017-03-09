# DateRange

The DateRange type represents a start and end point in time.

## Properties

| Property | Type | Description |
| :------- | :--- | :---------- |
| From | DateTime? | The datetime the range starts |
| To | DateTime? | The datetime the range ends |

## Remarks

The *From* and *To* properties are of type nullable DateTime and can be partly set.

## Validation

The *From* value cannot be a later date than the *To* value.

## Example

{% method -%}

### Get a DateRange field object

{% sample lang="cs" -%}

```cs
@{
    // Retrieve a film by it's ID.
    var film = client.Get("0aabad4e-a083-4a88-bd75-b2674e2f8298");

    // Get the field value as a DateRange instance.
    var filmingPeriod = film.Get<DateRange>("filmingPeriod");
}

<div class="start">@filmingPeriod.From</div>

<div class="end">@filmingPeriod.To</div>
```
{% endmethod %}

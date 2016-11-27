# DateRange

## Overview

The DateRange object represents a start and end point in time.

## Properties

| Property | Type | Description |
| :------- | :--- | :---------- |
| from | string | The datetime the range starts |
| to | string | The datetime the range ends |

## Validation

The *from* value cannot be a later date than the *to* value.

## Example

{% method -%}

{% sample lang="json" -%}

```json
{
    "from": "2006-12-06T09:00:00",
    "lng": "2009-09-10T09:00:00"
}
```
{% endmethod %}
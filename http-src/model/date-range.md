# DateRange

## Overview

The DateRange object represents a start and end point in time.

## Properties

| Property | Type | Description |
| :------- | :--- | :---------- |
| from | datetime | The datetime the range starts |
| to | datetime | The datetime the range ends |

## Validation

The *from* value cannot be a later datetime than the *to* value.

## Example

```json
{
    "from": "2006-12-06T09:00:00",
    "to": "2009-09-10T09:00:00"
}
```
# Get project by id

Returns a project resource by it's API id.

**GET:** /api/delivery/**{projectId}**

## Example

```http
GET: /api/delivery/projects/movieDb
```

## Response Messages

|HTTP Status Code|Reason|Response Model|
|-|-|-|
|200|Success|[Project](/model/entry.md)|
|404|Project not found|[Error](../model/errors.md)|
|500|Internal Server Error|[Error](../model/errors.md)|

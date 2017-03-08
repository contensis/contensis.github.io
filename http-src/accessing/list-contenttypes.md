# Get content types for a project

Returns an array of content type resources for a project.

**GET:** /api/delivery/**{projectId}**/contenttypes/

## Parameters

|Name|Parameter Type|Type|Format|Description|
|:-|:-|:-|:-|:-|
|projectId|path|string||The project identifier|

## Example

```http
GET: /api/projects/movieDb/contenttypes
```

## Response Messages

|HTTP Status Code|Reason|Response Model|
|:-|:-|:-|
|200|Success|[ContentType [...]](/model/content-type.md)|
|404|Project not found|[Error](../model/errors.md)|
|500|Internal Server Error|[Error](../model/errors.md)|

# Get content type by id

Returns a content type resource by it's API id.

**GET:** /api/delivery/**{projectId}**/contenttypes/**{contentTypeId}**

## Parameters

|Name|Parameter Type|Type|Format|Description|
|:-|:-|:-|:-|:-|
|projectId|path|string||The project identifier|
|contentTypeId|path|string||The content type identifier|

## Example

```http
GET: /api/delivery/projects/movieDb/contenttypes/movie
```

## Response Messages

|HTTP Status Code|Reason|Response Model|
|:-|:-|:-|
|200|Success|[Content type](/model/content-type.md)|
|404|Project not found|[Error](/model/errors.md)|
|500|Internal Server Error|[Error](/model/errors.md)|

# Get an Entry by id

**GET:** /api/delivery/**{projectId}**/entries/**{entryId}**

## Parameters

|Name|Parameter Type|Type|Format|Description|
|:-|:-|:-|:-|:-|
|projectId|path|string||The project identifier|
|entryId|path|string|GUID|The entry identifier as a 128 bit GUID|
|lang|query|string||The specified language variation for the entry. If no value is provided then the project default language is used|
|linkDepth|query|number|int|The depth at which to resolve the full entry data for a linked entry or asset, with a maximum depth value of 10|

## Example

```http
GET: /api/delivery/projects/movieDb/entries/99aae243-ad6e-401b-89f9-90a51def6a18/?lang=de-DE&linkDepth=1
```

## Response Messages

|HTTP Status Code|Reason|Response Model|
|:-|:-|:-|
|200|Success|[Entry](/model/entry.md)|
|404|Entry not found|[Error](/model/errors.md)|
|500|Internal Server Error|[Error](/model/errors.md)|
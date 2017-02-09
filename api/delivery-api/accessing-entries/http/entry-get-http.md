# Getting an entry

## Get an Entry by id

**GET** /api/**{projectId}**/entries/**{entryId}**

### Parameters

|Name|Parameter Type|Data Type|Description|
|-|-|-|-|-|
|projectId|path|Guid|The project identifier|
|entryId|path|Guid|The entry identifier|
|lang|query|string|The specified language variation for the entry. If no value is provided then the project default language is used|
|entryLinkDepth|query|int|The depth at which to resolve the full entry data for a linked entry, with a maximum depth value of 10|

### Example

{% method -%}

{% sample lang="http" -%}
```http
GET: /api/projects/movieDb/entries/99aae243-ad6e-401b-89f9-90a51def6a18/?lang=de-DE&entryLinkDepth=1
```
{% endmethod %}

### Response Messages

|HTTP Status Code|Reason|Response Model|
|-|-|-|
|200|Success|[Entry]()|
|404|Entry not found|
|500|Internal Server Error|

---



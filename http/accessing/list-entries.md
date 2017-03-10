# List entries

## List all

**GET:** /api/delivery/**{projectId}**/entries

## Parameters

|Name|Parameter Type|Type|Format|Description|
|:-|:-|:-|:-|:-|
|projectId|path|string|| The project identifier |
|versionStatus|query|string||The status of the entry, either *"published"* or *"latest"*. The default is *"published"* |
|linkDepth|query|number|int|The depth at which to resolve the full entry data for a linked entry or asset, with a maximum depth value of 10|
|pageIndex|query|number|int| The index of the result set to return |
|pageSize|query|number|int| The number of items to return in the result set  |
|order|query|string|  | A comma-separated list of [field](/model/content-type.md#field) ids to order the results by. Descending order is specified using a prefixed '-' |
|fields|query|string|  | A comma-separated list of [field](/model/content-type.md#field) ids to restrict the fields returned for an entry |
|lang|query|string|[LanguageCode](/localization.md)| The language variation to return for each entry |


## Response Messages

|HTTP Status Code|Reason|Response Model|
|:-|:-|:-|
|200|Success|[PagedList](/model/paged-list.md) of [Entry](/model/entry.md) items|
|500|Internal Server Error|[Error](/model/errors.md)|


## Examples

**List of all entries - actors, movies, directors, etc.**
```http
GET: /api/delivery/projects/movieDb/entries/
```

**List of all entries translated to German**
```http
GET: /api/delivery/projects/movieDb/entries/?lang=de
```

**List of all entries translated to German and ordered by published date descending**
```http
GET: /api/delivery/projects/movieDb/entries/?lang=de&order=-sys.published
```

**List of all entries with their direct child entries, assets and images resolved**
```http
GET: /api/delivery/projects/movieDb/entries/?linkDepth=1
```

---

## List by content type

**GET:** /api/delivery/**{projectId}**/contenttype/**{contentTypeId}**/entries

|Name|Parameter Type|Type|Format|Description|
|:-|:-|:-|:-|:-|
|projectId|path|string|| The project identifier |
|contentTypeId|path|string|  | The content type identifier |
|versionStatus|query|string||The status of the entry, either *"published"* or *"latest"*. The default is *"published"* |
|linkDepth|query|number|int|The depth at which to resolve the full entry data for a linked entry or asset, with a maximum depth value of 10|
|pageIndex|query|number|int| The index of the result set to return |
|pageSize|query|number|int| The number of items to return in the result set  |
|order|query|string|  | A comma-separated list of [field](/model/content-type.md#field) ids to order the results by. Descending order is specified using a prefixed '-' |
|fields|query|string|  | A comma-separated list of [field](/model/content-type.md#field) ids to restrict the fields returned for an entry |
|lang|query|string|[LanguageCode](/localization.md)| The language variation to return for each entry |

## Response Messages

|HTTP Status Code|Reason|Response Model|
|:-|:-|:-|
|200|Success|[PagedList](/model/paged-list.md) of [Entry](/model/entry.md) items|
|500|Internal Server Error|[Error](/model/errors.md)|

## Examples

**List of all movies**
```http
GET: /api/delivery/projects/movieDb/contentTypes/movies/entries/
```

**List of all movies translated to German**
```http
GET: /api/delivery/projects/movieDb/contentTypes/movies/entries?lang=de
```

**List of all movies translated to German and ordered by release date descending**
```http
GET: /api/delivery/projects/movieDb/contentTypes/movies/entries?lang=de&order=-releaseDate
```

**List of all movies with their direct child entries, assets and images resolved**
```http
GET: /api/delivery/projects/movieDb/contentTypes/movies/entries?linkDepth=1
```
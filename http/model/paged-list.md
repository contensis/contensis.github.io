# PagedList

A paged list is a structure that is used to describe paging details for listing and search results.

| Property | Type | Format | Description |
| :------- | :--- | :----- | :---------- |
| pageIndex | number | int | The index of the result set to return |
| pageSize | number | int | The size of the result set to return |
| totalCount | number | int | The total number of results available |
| items | object [...] |  | A container for the items being returned |

## Remarks

The paged list properties provide the information required to implement an accurate paging control with settable page sizes.

## Example

```json
{
  "pageIndex": 0,
  "pageSize": 20,
  "totalCount": 342,
  "items": [
    {
      "title": "The Terminator",
      "tagline": "The thing that won't die, in the nightmare that won't end.",
      "overview": "<p>In the post-apocalyptic future, reigning tyrannical supercomputers teleport a cyborg assassin known as the \"Terminator\" back to 1984 to kill Sarah Connor, whose unborn son is destined to lead insurgents against 21st century mechanical hegemony. Meanwhile, the human-resistance movement dispatches a lone warrior to safeguard Sarah. Can he stop the virtually indestructible killing machine?</p>",
      "releaseDate": "1985-01-11T00:00:00",
      "actors": [],
      "entryTitle": "The Terminator",
      "sys": {
        "id": "b678c784-0bb0-46ff-8837-9e0e79b8ba21",
        "uri": "/api/delivery/projects/website/entries/b678c784-0bb0-46ff-8837-9e0e79b8ba21",
        "projectId": "website",
        "contentTypeId": "movie",
        "dataFormat": "entry",
        "language": "en-GB",
        "metadata": {},
        "properties": {},
        "version": {
          "createdBy": "topdog",
          "created": "2017-03-07T16:10:41.8894598+00:00",
          "modifiedBy": "topdog",
          "modified": "2017-03-07T16:10:43.5147206+00:00",
          "publishedBy": "ServicesUser",
          "published": "2017-03-07T16:10:43.9989079+00:00",
          "versionNo": "1.0"
        },
        "owner": "topdog"
      }
    },
    ...
  ]
}
```
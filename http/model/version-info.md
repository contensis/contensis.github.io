# VersionInfo

The VersionInfo object contains the version status information for the current version of the resource.

| Property | Type | Format | Description |
| :------- | :--- | :----- | :---------- |
| created | string | date-time | The date and time the resource was created |
| createdBy | string | | The user id of who created the resource |
| modified | string | date-time | The date and time the resource version was last modified |
| modifiedBy | string | | The user id of who last modified the resource |
| published | string | date-time | The date and time the resource version was last published |
| publishedBy | string | | The user id of who last published the resource |
| versionNo | string | {Major}.{Minor} | The version number of the resource | 


## Example

```json
{
    "version": {
        "createdBy": "s.derrickson",
        "created": "2016-10-12T09:29:18.5144641+01:00",
        "modifiedBy": "b.cumberbatch",
        "modified": "2016-10-13T10:15:12.1973648+01:00",
        "publishedBy": "b.cumberbatch",
        "published": "2016-10-13T10:15:12.1973648+01:00",
        "versionNo": "2.0"
    }
}
```
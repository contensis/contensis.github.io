# Assets

Assets are effectively an extension of entries, with additional properties containing details about the file they represent. An asset is an entry with a dataFormat value equal to 'asset', which allows them to be identified and queried independently to entries.

## Standard fields

All assets have the following standard entry fields:

| Name | Description |
| ---- | ----------- |
| title | The title of the asset |
| description | The description for the asset |
| properties | A readonly collection of asset specific fields |

## Image fields

In addition to the standard entry fields, image content types have the following:

| Name | Description |
| ---- | ----------- |
| altText | The default alt text defined for the image resource |

## Default properties

All assets have the following default readonly properties:

| Name | Description |
| -------- | ----------- |
| filename | The name of the actual file, with extension included |
| fileSize | The file size in bytes |
| uri | The URI path to the file, excluding the domain |

## Extended properties

Extended properties are specific to a content type:

### Images

| Name | Description |
| -------- | ----------- |
| width | The width of the image |
| height | The height of the image |
| caption | The default caption defined for the image resource |

## Example JSON

{% method -%}
{% sample lang="json" -%}

```json
{
    "id": "71f73a9b-2a13-4d63-bcc1-e8ee5047b01c",
    "contentTypeId": "Image",
    "projectId": "movieDb",
    "dataFormat": "asset",
    "en-GB": {
        "title": "Deadpool cover",
        "description": "Cover art for the Deadpool film",
        "altText": "Deadpool jumping over a car, shooting numerous men",
        "metadata": {
            "originalId": 12345
        },
        "properties": {
            "filename": "deadpool.jpg",
            "fileSize": 34323,
            "width": 800,
            "width": 1200
        },
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
}
```
{% endmethod %}
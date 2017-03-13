# Assets

Assets are an extension of entries, with additional properties containing details about the file they represent. An asset is an entry with a dataFormat value equal to *asset*, which allows them to be identified and queried independently to entries.

## Fields
### Standard

All assets have the following standard data fields.

| Name | Description |
| ---- | ----------- |
| title | The title of the asset |
| description | The description for the asset |
| sys.properties | A readonly collection of asset specific properties |

### Image
In addition to the standard data fields, images have the following.

| Name | Description |
| ---- | ----------- |
| altText | The default alt text defined for the image resource |

## Properties
### Default
All assets have the following default readonly properties.

| Name | Description |
| -------- | ----------- |
| filename | The name of the actual file, with extension included |
| fileSize | The file size in bytes |

### Extended
Extended properties are specific to a content type.

#### Images

| Name | Description |
| -------- | ----------- |
| width | The width of the image |
| height | The height of the image |

## Example

@TODO: Example to be based on dotnet example

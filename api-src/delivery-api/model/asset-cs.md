# Assets

Assets are effectively an extension of entries, with additional properties containing details about the file they represent. An asset is an entry with a dataFormat value equal to 'asset', which allows them to be identified and queried independently to entries.

## Standard Fields

All assets have the following standard entry fields

| Name | Type | Description |
| ---- | ---- | ----------- |
| Title | The title of the asset |
| description | The description for the asset |
| properties | A readonly collection of asset specific fields |


## Default Properties

All assets have the following default readonly properties

| Name | Description |
| ---- | ----------- |
| filename | The name of the actual file, with extension included |
| fileSize | The file size in bytes |
| extension | The file extension |
| fieldId | The GUID identifier of the file resource |
| uri | The URI path to the file, excluding the domain |

## Extended Properties

### Images

| Name | Description |
| ---- | ----------- |
| width | The name of the actual file, with extension included |
| height | The height of the image |
| altText | The default alt text defined for the image resource |
| caption | The default caption defined for the image resource |
# Assets

Assets are effectively an extension of entries, with additional properties containing details about the file they represent. An asset is an entry with a dataFormat value equal to 'asset', which allows them to be identified and queried independently to entries.

## Standard Fields

All assets have the following standard entry fields

| Name | Type | Description |
| ---- | ---- | ----------- |
| Title | string | The title of the asset |
| Description | string | The description for the asset |
| properties | PropertiesDictionary | A readonly collection of asset specific fields |

## PropertiesDictionary

| Name | Type | Description |
| ---- | ---- | ----------- |
| Filename | The name of the actual file, with extension included |
| FileSize | The file size in bytes |
| Extension | The file extension |
| FieldId | The GUID identifier of the file resource |
| Uri | The URI path to the file, excluding the domain |
| [fieldName] | string | TODO |

## Extended Properties

### Images

| Name | Description |
| ---- | ----------- |
| width | The name of the actual file, with extension included |
| height | The height of the image |
| altText | The default alt text defined for the image resource |
| caption | The default caption defined for the image resource |
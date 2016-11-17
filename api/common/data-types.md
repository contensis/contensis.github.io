# Field Types

## Data Types

The Data Type is the storage type for a field. TODO: Add more here

| Type | Description |
| ---- | ----------- |
| string | Used for text entries such as titles, content or markup |
| integer | A whole number |
| decimal | A number with a fractional part |
| boolean | A value of `true` or `false` |
| datetime | A point in time |
| object | Any arbitary structure as JSON or a string |
| stringArray | An array of strings |
| integerArray | An array of integers |
| decimalArray | An array of decimals |
| booleanArray | An array of booleans |
| datetimeArray | An array of datetimes |
| objectArray | An array of objects |

## Data Format

The Data Format property is used as an extension of a DataType to describe or identify the structure and intent of the data. For example, a Location has a DataType of *object*, and a DataFormat of *location*. 

The DataFormat is designed to allow custom types to be added. The value is a simple string

### Supported Data Formats

| Format | Data Type | Description |
| ------ | --------- | ----------- |
| entry | object | An entry format for storing content |
| asset | object | An asset format that represents a file resource |
| location | object | Represents a point on the surface of Earth |
| quote | object | A quote with text and a source |
| field | objectArray |Represents a composed field type, usually defined as an ObjectArray Data Type |
| image | object | Wraps an Asset with an additional Caption property |

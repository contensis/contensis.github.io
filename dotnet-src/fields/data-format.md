# Data format

The Data Format property is used as an extension of a [DataType](/fields/data-types) to describe or identify the structure and intent of the data. For example, a [Location](/model/location.md) has a DataType of *object*, and a DataFormat of *location*. Another example is a HTML block, which has a DataType of *string* and a DataFormat of *html*.  

The DataFormat is a string value and is designed to allow custom types to be added.

## Supported data formats

The following list contains the data formats that are understood by Contensis:

| Format | Data Type | Description |
| ------ | --------- | ----------- |
| entry | Object | An entry format for storing content |
| asset | Object | An asset format that represents a file resource |
| location | Object | Represents a point on the surface of the Earth |
| quote | Object | A quote with text and a source |
| field | ObjectArray |Represents a composed field type, defined as an ObjectArray Data Type |
| image | Object | Wraps an Asset with an additional Caption property |
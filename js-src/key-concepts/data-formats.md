@TODO: Copy from http when signed off

# Data formats

The dataFormat property is used as an extension of a [dataType](/key-concepts/data-types.md) to describe the structure and intent of the data. For example, a *location* has a dataType of *object*, and a dataFormat of *location*. Another example is a HTML block, which has a dataType of *string* and a dataFormat of *html*.  

The dataFormat is a string value and is designed to allow custom types to be added.

## Supported data formats

The following list contains the data formats that are currently understood by Contensis:

| Data format | Data type | Description |
| :---------- | :-------- | :---------- |
| [entry](/model/entry.md) | object | An entry format for storing content |
| [asset](/model/asset.md) | object | An asset format that represents a file resource |
| [location](/model/location.md) | object | Represents a point on the surface of the Earth |
| [quote](/model/quote.md) | object | A quote with text and a source |
| [dateRange](/model/date-range.md) | object | Represents a document heading |
| [image](/model/image.md) | object | Wraps an Asset with an additional Caption property |
| field | objectArray | Represents a [composed](/model/composed.md) type, defined as an `objectArray` Data Type |
| heading | string | Represents a document heading |
| html | string | A string of HTML markup |
| markdown | string | A string of Markdown markup |

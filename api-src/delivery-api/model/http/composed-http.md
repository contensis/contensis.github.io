# Composed fields

The composed field type contains the data that the [Composer editor](https://contensis.github.io/docs/content-types/field-editors/editor-composer.html) defines. It is a array of objects which expose *type* and *value* properties.  The *type* property is a name given to an *allowed field type validation* defined in the content type that the entry is based on. The *value* contains the data for the field.

An *allowed field type* is essentially any standard field (such as Image, Heading, Location, etc.) that restricts what types of field can be added to a composed field.

For example, an *allowed field* could be defined with a type of *Heading* and named "mainHeading" or with a type of *Image* and named "bannerImage". There can be multiple *allowed fields* based on the same type, but a composed field cannot contain other composer fields. 

## Properties

| Name | Description |
| ---- | ----------- |
| type | The name given to a field type defined in the content type |
| value | The value of the field, which can be of any type |

## Example

The JSON below shows an example composed field:

{% method -%}

{% sample lang="json" -%}

```json
{
    "synopsis": [
        {
            "type": "mainHeading",
            "value": "Plot details"
        },
        {
            "type": "markup",
            "value": "Nearly 10 years have passed since Sarah Connor was targeted for termination by a cyborg from the future. Now her son, John, the future leader of the resistance, is the target for a newer, more deadly terminator. Once again, the resistance has managed to send a protector back to attempt to save John and his mother Sarah."
        },
        {
            "type": "memorableQuote",
            "value": {
                "text": "I'll be back!",
                "source": "Terminator T-800"
            }
        }
    ]
}
```

{% endmethod %}

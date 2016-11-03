# Date/time field editors
The date / time field editors have four distinct flavours, providing the flexibility to capture the data you require.

| Type | Summary|
| ---| --- |
| Date | A single date picker |
| Date and time | A date and time picker |
| Date range | Two date pickers to provide a range |
| Date and time range | Two date and time pickers to provide a range |

The date range editors become available when the format of a Date / Time field are set to range.

> **Note:** we do not support time without a date as we store date and times as UTC. While there may be some use cases for time on its own we recommend you use a text field with a regular expression for validation.

## Settings
| Setting name | Summary|
| ---| --- |
| [Name](/content-types/field-editors/field-settings.md#name) | A text label to identify the field in an entry.|
| [Field ID](/content-types/field-editors/field-settings.md#field-id) | A sanitised name to be used by the API. |
| [Default value](/content-types/field-editors/field-settings.md#default-value) | The default value property sets the default content for a field when an entry is created. |


## Supported validation
This field editor supported the following validation methods.

- [Required field](/content-types/validation/required-validation.md)

## Properties

### Common properties
| Property name | Summary|
| ---| --- |
| [Placeholder text](/content-types/field-editors/field-properties.md#placeholder-text) | The placeholder property specifies a short hint that describes the expected value of a field. [^1]|
| [Help instructions](/content-types/field-editors/field-properties.md#help-instructions) |  Provides guidance to an author of the expected content that the field should contain. |

### Future dates
This property sets if you want an author to be able to select a date in the future *e.g.* a date greater than today. This is enabled by default.

### Past dates
This property sets if you want an author to be able to select a dates in the past *e.g.* a date less than today. This is enabled by default.


#### Footnotes

---

[^1]: Should we provide placeholder text / labelling for date ranges
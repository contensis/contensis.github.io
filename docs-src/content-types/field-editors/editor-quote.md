# Quote field editor
The quote field editor is an editor that allows you to record quotes and a source citation within an entry. Its handy when you want to include a quote from a customer in a case study or a famous quote in a blog post. The source citation is optional. 

## Settings
| Setting name | Summary|
| ---| --- |
| [Name](/content-types/field-editors/field-settings.md#name) | A text label to identify the field in an entry.|
| [Field ID](/content-types/field-editors/field-settings.md#field-id) | A sanitised name to be used by the API. |

## Supported validation
This field editor supported the following validation methods.

- [Required Field](/content-types/validation/required-validation.md)

## Properties

### Common properties
| Property name | Summary|
| ---| --- |
| [Placeholder text](/content-types/field-editors/field-properties.md#placeholder-text) | The placeholder text for the quote |
| [Help Instructions](/content-types/field-editors/field-properties.md#help-instructions) | A sanitised name to be used by the API. |

### Source placeholder text
The [placeholder](/content-types/field-editors/field-properties.md#placeholder-text) text for the source citation.

### Require source?
If you want to enforce a source to be included then set this toggle to yes. Its default value is set to *No.[^1]

### Custom error message
Provide a custom validation message when the source citation is not included by populating the textbox.[^2]

#### Footnotes

---
[^1]: Should we provide a toggle option to enable source. this would allow us to group all source properties.
[^2]: The text label of the message should be consistent with all other validation messages.
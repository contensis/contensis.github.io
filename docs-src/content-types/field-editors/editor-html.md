# HTML field editor
The HTML Editor provides the user the ability to create blocks of rich text including Headings, Lists, Bold, Italic as well as links.

The editor is powered by the Redactor editor. We automatically strip out any invalid HTML, including removing all `<span>` tags, empty tags, and style attributes.

## Settings
| Setting name | Summary|
| ---| --- |
| [Name](/content-types/field-editors/field-settings.md#name) | A text label to identify the field in an entry.|
| [Field ID](/content-types/field-editors/field-settings.md#field-id) | A sanitised name to be used by the API. |

## Supported validation
This field editor supports the following validation methods.

- [Required field](/content-types/validation/required-validation.md)


## Properties

### Common properties
| Property name | Summary|
| ---| --- |
| [Content guidelines](/content-types/field-editors/field-properties.md#content-guidelines) |  Provides guidance to an author of the expected content that the field should contain. |
| [Size](/content-types/field-editors/field-properties.md#editor-size) | Determines the size of the rendered editor in the entry editor. Its default value is set to Medium. |

### Show toolbar
The setting enables you to disable the editor toolbar and instead use an inline editing toolbar. Its default value is set to *Yes*.

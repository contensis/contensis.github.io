# HTML field editor
The HTML Editor allows you to create blocks of rich text including headings, lists, bold, italic and hyperlinks.

The editor is powered by the TinyMCE editor. Contensis automatically strips out any invalid HTML, including `<span>` tags, empty tags, and style attributes.

## Appearance
![HTML Field Editor](/images/field-editor-html.png)

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
| [Placeholder text](/content-types/field-editors/field-properties.md#placeholder-text) | The placeholder property provides a short hint describing the expected value of a field. |
| [Content guidelines](/content-types/field-editors/field-properties.md#content-guidelines) | Provides guidance to an author for the expected content the field should contain. |
| [Size](/content-types/field-editors/field-properties.md#editor-size) | Determines the size of the rendered editor in the entry editor. The default value is set to *Medium*. |

# Asset field editor
This field editor allows an author to make single or multiple selections of file assets that have been uploaded to Contensis.

Selection is made in an asset gallery. Single or multiple selection of assets is determined by the allow multiple field setting.

### Settings
| Setting name | Summary|
| ---| --- |
| [Name](/content-types/field-editors/field-settings.md#name) | A text label to identify the field in an entry.|
| [Field ID](/content-types/field-editors/field-settings.md#field-id) | A sanitised name to be used by the API. |
| [Multiple selection](/content-types/field-editors/field-settings.md#allow-multiple) |  Allows multiple selection within a field. |

## Supported validation
This field editor supports the following validation methods.

- [Required field](/content-types/validation/required-validation.md)

## Properties

### Common properties
| Property name | Summary|
| ---| --- |
| [Content guidelines](/content-types/field-editors/field-properties.md#content-guidelines) |  Provides guidance to an author of the expected content that the field should contain. |

### Type
The display of available assets in the gallery will be restricted to show only those types selected in the Type dropdown.

The dropdown list is populated with asset types supported by the current project. Some system reserved asset types are not displayed in this list such as forms, templates, polls and databases.

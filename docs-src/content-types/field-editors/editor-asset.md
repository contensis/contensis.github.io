# Asset field editor
This field editor allows an author to make single or multiple selections of file assets that have been uploaded to Contensis.

Selection is made in an asset gallery. Single or multiple selection of assets is determined by the allow multiple field setting.

## Settings
| Setting name | Summary|
| ---| --- |
| [Name](/content-types/field-editors/field-settings.md#name) | A text label to identify the field in an entry.|
| [Field ID](/content-types/field-editors/field-settings.md#field-id) | A sanitised name to be used by the API. |
| [Allow multiple](/content-types/field-editors/field-settings.md#allow-multiple) |  Allows multiple selection within a field. |

## Supported validation
This field editor supports the following validation methods.

- [Required field](/content-types/validation/required-validation.md)

## Properties

### Common properties
| Property name | Summary|
| ---| --- |
| [Placeholder text [^1]](/content-types/field-editors/field-properties.md#placeholder-text) | The placeholder property specifies a short hint that describes the expected value of a field. |
| [Help instructions](/content-types/field-editors/field-properties.md#help-instructions) |  Provides guidance to an author of the expected content that the field should contain. |

### Type
Types of asset can be restricted in the gallery to a single asset type by selecting the type from the property dropdown.

The dropdown list is populated with assets types supported by the current project. Some system reserved asset types are not displayed in this list such as forms, templates, polls and databases. [^2]

#### Footnotes:

---

[^1]: Is the placeholder text used in the asset editor?
[^2]: Should we allow the restriction to be made to more than a single type?

# Image field editor
This field editor allows an author to make single or multiple selections of images that have been uploaded to Contensis.

Selection is made in an image gallery. Single or multiple selection of images is determined by the allow multiple field setting.

## Appearance
**Single**
![Single Image Editor](/images/field-editor-single-image.png)
**Medium**
![Multiple Image Editor](/images/field-editor-multiple-image.png)


## Settings
| Setting name | Summary|
| ---| --- |
| [Name](/content-types/field-editors/field-settings.md#name) | A text label to identify the field in an entry.|
| [Field ID](/content-types/field-editors/field-settings.md#field-id) | A sanitised name to be used by the API. |
| [Multiple selection](/content-types/field-editors/field-settings.md#allow-multiple) |  Allows multiple selection within a field. |

## Supported validation
This field editor supports the following validation methods:

- [Required field](/content-types/validation/required-validation.md)

## Properties

### Common properties
| Property name | Summary|
| ---| --- |
| [Content guidelines](/content-types/field-editors/field-properties.md#content-guidelines) |  Provides guidance to an author of the expected content that the field should contain. |
| [Placeholder text](/content-types/field-editors/field-properties.md#placeholder-text) | The placeholder property specifies a short hint that describes the expected value of a field. |

### Requires caption
The caption requirement forces an author to include a caption for each image they have selected in the field editor.

### Requires caption error message
An optional validation message can be entered to remind an author that a caption is required.

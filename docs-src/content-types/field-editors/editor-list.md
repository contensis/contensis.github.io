# List field editor
The list field editor will display a list of items for an author to select from that are set in the list values properties text box.

The type of list displayed will depend on if multiple selection is allowed. Single selection lists are shown as a radio button list, checkbox lists are used when multiple selection is set.

## Appearance
![List Field Editor](/images/field-editor-list.png)

## Settings
| Setting name | Summary|
| ---| --- |
| [Name](/content-types/field-editors/field-settings.md#name) | A text label to identify the field in an entry.|
| [Field ID](/content-types/field-editors/field-settings.md#field-id) | A sanitised name to be used by the API. |
| [Default value](/content-types/field-editors/field-settings.md#default-value) | The default value property sets the default content for a field when an entry is created. |
| [Multiple selection](/content-types/field-editors/field-settings.md#allow-multiple) |  Allows multiple selection within a field. |

## Supported validation
This field editor supports the following validation methods.

- [Required field](/content-types/validation/required-validation.md)

## Properties
### Common properties
| Property name | Summary|
| ---| --- |
| [Content guidelines](/content-types/field-editors/field-properties.md#content-guidelines) |  Provides guidance to an author for the expected content that the field should contain. |

### List values
This property expects a comma separated list of values that are to be displayed in the list.

> *e.g.* Red, Blue, Green, Orange, Purple

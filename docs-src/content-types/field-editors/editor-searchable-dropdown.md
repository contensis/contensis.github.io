# Searchable dropdown field editor
The searchable dropdown field editor provides a way to use keyword searches to filter down a large list of values that are set in the list values properties text box.

The type of dropdown displayed will depend on whether multiple selection is allowed. Single selections allow a single value to be searched for and set, very similar to a standard dropdown menu with the additional support for search.

When multiple selection is set each value selected is added as box with a cross which allows items to be removed from the list.

## Appearance
![Searchable Dropdown Field Editor](/images/field-editor-searchabledropdown.png)

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
| [Placeholder text](/content-types/field-editors/field-properties.md#placeholder-text) | The placeholder property specifies a short hint that describes the expected value of a field, in the case of the searchable dropdown this value will set the default text. [^1] |
| [Content guidelines](/content-types/field-editors/field-properties.md#content-guidelines) |  Provides guidance to an author of the expected content that the field should contain. |

### List values
This property expects a comma separated list of values that are to be displayed in the dropdown.

> *e.g.* Red, Blue, Green, Orange, Purple

### Validation message
Why is this even here? [^2]

#### Footnotes:

---

[^1]: Should the placeholder text be removed, and instead the default value be set to Please select?
[^2]: This needs to be removed.

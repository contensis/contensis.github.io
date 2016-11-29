# Taxonomy field editor
This editor allows you to bind a list of existing taxonomy nodes from the taxonomy manager into a selection that can be made by an author.

This is an ideal field editor for centrally managing static values, examples being categorisations, language or country lists that may be used elsewhere in your project.

The taxonomy editor supports single and multiple selection, and allows you to specify a root taxonomy node from where values can be selected from.

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
| [Content guidelines](/content-types/field-editors/field-properties.md#content-guidelines) |  Provides guidance to an author of the expected content that the field should contain. |

### Root node
The root node property allows you to select a node that values can be selected from. If no node is selected the whole of your taxonomy will be visible in the editor.

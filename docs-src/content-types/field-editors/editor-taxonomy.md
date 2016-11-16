# Taxonomy field editor
This editor allows you to bind a list of pre existing taxonomy nodes from the taxonomy manager into a selection that can be made by an author.

This is an ideal field editor for static values you want to manage centrally such as categorisations, language or country lists that you might use elsewhere in your project.

The taxonomy editor supports single and multiple selection, whilst allowing to specify a root taxonomy node where child values should stem from.

## Settings
| Setting name | Summary|
| ---| --- |
| [Name](/content-types/field-editors/field-settings.md#name) | A text label to identify the field in an entry.|
| [Field ID](/content-types/field-editors/field-settings.md#field-id) | A sanitised name to be used by the API. |
| [Allow multiple](/content-types/field-editors/field-settings.md#allow-multiple) |  Allows multiple selection within a field. |

## Supported validation
This field editor supported the following validation methods.

- [Required field](/content-types/validation/required-validation.md)

## Properties

### Common properties
| Property name | Summary|
| ---| --- |
| [Help instructions](/content-types/field-editors/field-properties.md#help-instructions) |  Provides guidance to an author of the expected content that the field should contain. |

### Root node
The root node property allows you to select a node that child values should stem from. If no node is selected the whole of your taxonomy will be visible in the editor.

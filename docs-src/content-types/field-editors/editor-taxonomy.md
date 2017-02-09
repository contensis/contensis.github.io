# Taxonomy field editor
This editor allows you to bind a list of existing taxonomy nodes from the *Taxonomy Manager* to a field where one or more items are available for selection by an author.

This is an ideal field editor for centrally managing static values, such as categories, languages, or country lists that may be used elsewhere in your project.

The taxonomy editor supports single and multiple selections, and allows you to specify a root taxonomy node from which values can be selected.

## Appearance
![Taxonomy Field Editor](/images/field-editor-taxonomy.png)

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
| [Content guidelines](/content-types/field-editors/field-properties.md#content-guidelines) |  Provides guidance to an author for the expected content that the field should contain. |

### Root node
The root node property allows you to select a node to determine what values can be selected by an author. If no node selection is made, then all taxonomy values will be visible in the editor.

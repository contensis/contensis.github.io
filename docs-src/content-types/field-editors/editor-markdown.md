# Markdown field editor
The markdown editor provides the user the ability to write blocks of content using the markdown syntax.

We use the SimpleMDE markdown editor as it provides a rich toolset including fullscreen mode.

## Limitations
The content entered into the markdown editor is stored and  returned through the Delivery API as pure markdown. Any links or images referenced in the markdown editor have to be external as we do not parse the markdown content.

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
| [Size](/content-types/field-editors/field-properties.md#editor-size) | Determines the size of the rendered editor in the entry editor. Its default value is set to *Medium*. |


### Show toolbar
The setting enables you to disable the editor toolbar from being displayed. This would require an author to understand how to write in the markdown syntax.

Its default is set to *No*.

### Show status
This setting changes the visibility of the character and word count below the markdown editor.

Its default is set to *No*.

### Allow fullscreen
Its possible to edit markdown in a fullscreen window within Contensis to provide a distraction free writing experience. This setting determines if authors should be allowed to enter full screen.

Its default is set to *No*.


[^1]: Has duplicate panel title of Markdown

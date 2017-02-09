# Markdown field editor
The Markdown editor allows you to write blocks of content using the Markdown syntax. Contensis uses the SimpleMDE Markdown editor as it provides a rich toolset including fullscreen mode.

## Limitations
The content entered into the Markdown editor is stored and returned through the Delivery API as pure Markdown. Any links or images referenced in the Markdown editor have to be external as we do not parse the Markdown content.

## Appearance
![Markdown Field Editor](/images/field-editor-markdown.png)

## Settings
| Setting name | Summary|
| ---| --- |
| [Name](/content-types/field-editors/field-settings.md#name) | A text label to identify the field in an entry.|
| [Field ID](/content-types/field-editors/field-settings.md#field-id) | A sanitised name to be used by the API. |

## Supported validation
This field editor supports the following validation methods:

- [Required field](/content-types/validation/required-validation.md)

## Properties

### Common properties
| Property name | Summary|
| ---| --- |
| [Content guidelines](/content-types/field-editors/field-properties.md#content-guidelines) |  Provides guidance to an author for the expected content that the field should contain. |
| [Size](/content-types/field-editors/field-properties.md#editor-size) | Determines the size of the rendered editor in the entry editor. The default value is set to *Medium*. |


### Show toolbar
This setting lets you to prevent the editor toolbar from being displayed. This would require an author to understand how to write in the Markdown syntax.

The default is set to *No*.

### Show status
This setting changes the visibility of the character and word count below the Markdown editor.

The default is set to *No*.

### Allow fullscreen
It's possible to edit Markdown in a fullscreen window within Contensis. This setting determines if authors should be allowed to enter fullscreen.

The default is set to *No*.

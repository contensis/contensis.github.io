# Location field editor
The location field editor enables an author to provide an accurate location within an entry. A location can be set using the search which is powered by Google places, or alternatively, by navigating using the map.

Finer adjustments to location can be set by dragging the map pin to an exact position, or alternatively, entering latitude / longitude values in to the editor.

## Appearance
![Location Field Editor](/images/field-editor-location.png)

## Settings
| Setting name | Summary|
| ---| --- |
| [Name](/content-types/field-editors/field-settings.md#name) | A text label to identify the field in an entry.|
| [Field ID](/content-types/field-editors/field-settings.md#field-id) | A sanitised name to be used by the API. |
| [Default value](/content-types/field-editors/field-settings.md#default-value) | You can set a default map location when the field editor is displayed. |

## Supported validation
This field editor supports the following validation methods.

- [Required field](/content-types/validation/required-validation.md)

## Properties
### Common properties
| Property name | Summary|
| ---| --- |
| [Content guidelines](/content-types/field-editors/field-properties.md#content-guidelines) |  Provides guidance to an author of the expected content that the field should contain. |
| [Size](/content-types/field-editors/field-properties.md#editor-size) | Determines the size of the rendered editor in the entry editor. Its default value is set to Medium. |

### Show latitude and longitude
It's possible to enter exact latitude and longitude values into the entry editor, however, most authors will want to use the search or set a location by using the map.

This setting determines if the latitude and longitude number fields should be present in the entry editor.

By default these fields are not displayed.

### Show search
If you want your authors to manually set the location by using the navigation controls then you can disable the search box from the field editor.

The search box is on by default.

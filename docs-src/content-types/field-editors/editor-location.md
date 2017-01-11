# Location field editor
Using the location field editor you can to provide an accurate location within an entry. A location can be set using the search which is powered by Google Places, or by navigate with the map.

Fine adjustments to location can be set by dragging the map pin to an exact position, or by entering latitude and longitude coordinates.

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
| [Size](/content-types/field-editors/field-properties.md#editor-size) | Determines the size of the rendered editor in the entry editor. Its default value is set to *Medium*. |

### Show latitude and longitude
It's possible to enter exact latitude and longitude values into the entry editor, however, most authors will want to use the search or set a location using the map.

This setting determines if the latitude and longitude number fields should be shown in the entry editor. By default these fields are not displayed.

### Show search
If you want your authors to manually set the location using the navigation controls then you can disable the search box in the field editor. The search box is enabled by default.

## Place search limitations
The location field editor uses the Google Places API Web Service to carry out location searches. There is a default limit set by Google of 1,000 free requests per 24 hour period.

Each text search counts as 10 requests to this service, the default limit in a 24 period could quickly be met if your authors use location searches in their entries regularly.

### Increasing the limit
To increase the limit to 150,000 requests you'll need to verify your identity with Google by adding your billing information through the [Google developer console](https://console.developers.google.com). Once billing information has been added you can create an API Key via the Google API Console. This API key can then be applied to the project setting _Google_ApiKey_Places_.

> **Note:** The credit card details provided for billing are purely to validate identity. The card will not be charged for use of the Google Places API Web Service.

If you feel you need more than the 150,000 requests then you can purchase a Google Maps API premium plan.

Full details can be found at the Google Place API [usage an billing site](https://developers.google.com/places/web-service/usage)

# Project

A project object can be retrieved from the Delivery API to understand the languages that the project supports and which language is the primary language.

| Property | Type | Description |
| :------- | :--- | :---------- |
| Id | `string` | A unique project identifier |
| Name | `string` | The friendly name given to the project |
| Description | `string` | The description text given to a project |
| SupportedLanguages | `IReadOnlyList<string>` | An array of all the languages supported by the project |
| PrimaryLanguage | string | [LanguageCode](/localization.md) The primary language for the project |


## Example

```json
{
    "id": "movieDb",
    "name": "Movie Database",
    "description": "...",
    "supportedLanguage": [
        "en-GB",
        "en-US",
        "fr"
    ],
    "primaryLanguage": "en-GB"
}

```

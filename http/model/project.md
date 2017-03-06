# Project

A Project resource can be retrieved from the Delivery API to understand the languages that the project supports and which language is the primary language.

| Property | Type | Format | Description |
| :------- | :--- | :----- | :---------- |
| id | string | | A friendly unique project identifier |
| name | string |  | The name given to the project |
| description | string |  | The description text given to a project |
| supportedLanguages | string[...] |  | An array of all the languages supported by the project |
| primaryLanguage | string | LanguageCode  | The primary language for the project |


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
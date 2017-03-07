# ContentType

A Content Type resource can be retrieved from the Delivery API to understand the schema of an [entry](./entry.md). Entries are constructed and validated using the infomation defined in the Fields collection. The

| Property | Type | Format | Description |
| :------- | :--- | :----- | :---------- |
| id | string | | A friendly unique content type identifier |
| projectId | string |  | The project identifier |
| name | object | [LocalizedValue]()  | The friendly name given to a content type |
| description | object | [LocalizedValue]() | The description text given to a content type |
| entryTitleField | string |  | The id of the field which should be used as the title in entry listings |
| fields | object [...] | [Field](#field)  | A collection of fields that form the schema for an entry |
| enabled | boolean |  |  |
| defaultLanguage | string | [LanguageCode](/localization.md) |  |
| supportedLanguages | string [...] | [LanguageCode](/localization.md) |  |
| workflowId | string |  | The workflow that derived entries will  |
| dataFormat | string |  | Either 'entry' or 'asset' |
| previewUrl | string |  | The url that an example of an entry based on the content type can be viewed |
| version | object | [VersionInfo](#versioninfo) | Version infomation about the content type |

## Field

| Property | Type | Format | Description |
| :------- | :--- | :----- | :---------- |
| id | string |  | A unique field identifier |
| name | object | [LocalizedValue](#localizedvalue) | A friendly name for the field |
| description | object | [LocalizedValue](#localizedvalue) | The description for the field's purpose |
| dataType | string | [DataType](/fields/data-types.md) | The field data type |
| dataFormat | string | [DataType](/fields/data-formats.md) | The field data format |
| default | object | [LocalizedValue](#localizedvalue) | The default value for the field if no value is provided by an editor |
| editor | object | Editor | Configuration for the Contensis entry editor |


## VersionInfo

| Property | Type | Format | Description |
| :------- | :--- | :----- | :---------- |
| created | string | date-time | The date and time the entry was created |
| screatedBy | string | | The user id of who created the entry |
| modified | string | date-time | The date and time the entry version was last modified |
| modifiedBy | string | | The user id of who last modified the entry |
| published | string | date-time | The date and time the entry version was last published |
| publishedBy | string | | The user id of who last published the entry |
| versionNo | string | {Major}.{Minor} | The version of the entry | 

## Example

```json
{
    "id": "movie",
  "projectId": "website",
  "name": {
    "en-GB": "Movie"
  },
  "description": {
    "en-GB": "A movie type"
  },
  "entryTitleField": "title",
  "fields": [
    {
      "id": "title",
      "name": {
        "en-GB": "Title"
      },
      "dataType": "String",
      "dataFormat": null,
      "description": {},
      "default": {},
      "validations": null,
      "editor": {
        "id": "text",
        "instructions": {
          "en-GB": "The title of the movie"
        },
        "properties": {
          "placeholderText": {
            "en-GB": "Enter the full title of the movie appropriate to the region"
          }
        }
      }
    },
    {
      "id": "tagline",
      "name": {
        "en-GB": "Tagline"
      },
      "dataType": "String",
      "dataFormat": null,
      "description": {},
      "default": {},
      "validations": null,
      "editor": null
    },
    {
      "id": "overview",
      "name": {
        "en-GB": "Overview"
      },
      "dataType": "String",
      "dataFormat": "html",
      "description": {},
      "default": {},
      "validations": null,
      "editor": null
    },
    {
      "id": "releaseDate",
      "name": {
        "en-GB": "Release Date"
      },
      "dataType": "DateTime",
      "dataFormat": null,
      "description": {},
      "default": {},
      "validations": null,
      "editor": {
        "id": "date",
        "instructions": {
          "en-GB": "The release date of the movie"
        },
        "properties": {}
      }
    },
    {
      "id": "actors",
      "name": {
        "en-GB": "Actors"
      },
      "dataType": "ObjectArray",
      "dataFormat": "entry",
      "description": {},
      "default": {},
      "validations": {
        "contentType": {
          "contentType": "dan"
        }
      },
      "editor": {
        "id": "entry",
        "instructions": {
          "en-GB": ""
        },
        "properties": {
          "placeholderText": {
            "en-GB": "Add the main actors"
          }
        }
      }
    }
  ],
  "enabled": true,
  "defaultLanguage": "en-GB",
  "supportedLanguages": [
    "en-GB",
    "fr-FR",
    "de-DE",
    "es"
  ],
  "workflowId": "ContensisMultilingual",
  "dataFormat": "entry",
  "previewUrl": "http://www.mymoviewebsite.com/movies/terminator"
  "version": {
    "createdBy": "topdog",
    "created": "2017-03-07T14:37:27.0998174+00:00",
    "modifiedBy": "topdog",
    "modified": "2017-03-07T14:39:16.3337294+00:00",
    "publishedBy": "topdog",
    "published": "2017-03-07T14:39:19.3495296+00:00",
    "versionNo": "1.0"
  }
}

```
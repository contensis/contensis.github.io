# Entries

A full [overview of entry concepts can be found here](https://contensis.github.io/docs/entries/).

An entry definition in the Delivery API contains a mixture of standard properties and properties that have been defined by the content type that an entry is based on. 

## Data properties

Data properties are items defined by the fields set in a content type. 

## Standard properties

These are the standard properties that all entries have. The language property is the indexer for the entry data as an entry can have multiple language variations which can be be edited and versioned independently using the Management API. In the Delivery API context only a single language variation is available on an entry. 

### Entry

| Property | Type | Format | Description |
| :------- | :--- | :----- | :---------- |
| [Field] | Any | Any | Field data that is defined in the associated [Content Type](./content-type.md). <br />The data is keyed by a unique field id.  |
| sys | object | [Sys](#sys) | The container of the entry system data |

### Sys

| Property | Type | Format | Description |
| :------- | :--- | :----- | :---------- |
| id | string | GUID | The entry identifier as a 128 bit GUID|
| projectId | string | | The API identifer of the project the entry belongs to |
| contentTypeId | string | | The API identifier of the content type that the entry is based on |
| dataFormat | string | | Either 'entry' or 'asset' |
| language | string | CultureCode | The language of the entry variation as  |
| uri | string | URI | The entry uri |
| metadata | object | | Metadata associated with the entry instance |
| version | object | [VersionInfo](#versioninfo) | Version info specific to the entry variation |

### VersionInfo

| Property | Type | Format | Description |
| :------- | :--- | :----- | :---------- |
| created | string | date-time | The date and time the entry was created |
| screatedBy | string | | The user id of who created the entry |
| modified | string | date-time | The date and time the entry version was last modified |
| modifiedBy | string | | The user id of who last modified the entry |
| published | string | date-time | The date and time the entry version was last published |
| publishedBy | string | | The user id of who last published the entry |
| versionNo | string | {Major}.{Minor} | The version of the entry | 


{% method -%}

## Entry example

This JSON shows an example entry based on a Movie content type:

{% sample lang="json" -%}
```json
{
    "title": "Back to the future",
    "tagline": "He's the only kid ever to get into trouble before he was born.",
    "overview": "Marty McFly, a typical American teenager of the Eighties, is accidentally sent back to 1955 in a plutonium-powered DeLorean \"time machine\" invented by slightly mad scientist. During his often hysterical, always amazing trip back in time, Marty must make certain his teenage parents-to-be meet and fall in love - so he can get back to the future.",
    "trailer": "https://www.youtube.com/watch?v=qvsgGtivCgs",
    "releaseDate": "1985-07-02T23:00:00Z",
    "actors": [
        {
            "sys": {
                "id": "a1c983d6-4aaf-4456-9f3d-a6eac3139f1c",
                "language": "en-GB",
                "dataFormat": "entry"
            }
        },
        {
            "sys": {
                "id": "16f6f2de-e901-4bda-bf3f-092b93ae62a9",
                "language": "en-GB",
                "dataFormat": "entry"
            }
        },
        {
            "sys": {
                "id": "09b87c0b-67b2-4028-9358-e29ff16f11da",
                "language": "en-GB",
                "dataFormat": "entry"
            }
        }
    ],
    "sys": {
        "id": "71f73a9b-2a13-4d63-bcc1-e8ee5047b01c",
        "contentTypeId": "movie",
        "projectId": "movieDb",
        "language": "en-GB",
        "uri": "/api/projects/movieDb/entries/71f73a9b-2a13-4d63-bcc1-e8ee5047b01c",
        "dataFormat": "entry",
        "metadata": {},
        "version": {
            "createdBy": "s.derrickson",
            "created": "2016-10-12T09:29:18.5144641+01:00",
            "modifiedBy": "b.cumberbatch",
            "modified": "2016-10-13T10:15:12.1973648+01:00",
            "publishedBy": "b.cumberbatch",
            "published": "2016-10-13T10:15:12.1973648+01:00",
            "versionNo": "2.0"
        }
    }
}
```
{% endmethod %}
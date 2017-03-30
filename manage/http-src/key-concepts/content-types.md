# Content types

## Get a content type

Gets an existing content type by the content type id.

<span class="label label--get">GET</span> /api/management/projects/**{projectId}**/contenttypes/**{contentTypeId}**

### Example request

```http
GET: /api/delivery/projects/movieDb/contenttypes/movie/
```

### Response messages

| HTTP status code | Reason | Response model |
|:-|:-|:-|
| 200 | Success | [Content Type](/model/content-type.md) |
| 404 | Project not found | [Error](/key-concepts/errors.md) |
| 500 | Internal server error | [Error](/key-concepts/errors.md) |








## Create a content type

Creates a new content type resource.

<span class="label label--post">POST</span> /api/management/projects/**{projectId}**/contenttypes/

### Example request

```http
POST: /api/delivery/projects/movieDb/contenttypes/

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
      "dataType": "string",
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
      "dataType": "string",
    },
    {
      "id": "overview",
      "name": {
        "en-GB": "Overview"
      },
      "dataType": "String",
      "dataFormat": "html",
    },
    {
      "id": "releaseDate",
      "name": {
        "en-GB": "Release Date"
      },
      "dataType": "dateTime",
      "validations": null
    },
    {
      "id": "actors",
      "name": {
        "en-GB": "Actors"
      },
      "dataType": "ObjectArray",
      "dataFormat": "entry",
      "validations": {
        "contentType": {
          "contentType": "actor"
        }
      }
    }
  ],
  "defaultLanguage": "en-GB",
  "supportedLanguages": [
    "en-GB",
    "fr-FR",
    "de-DE",
    "es"
  ],
  "workflowId": "ContensisMultilingual",
  "dataFormat": "entry"
}
```

### Response messages

| HTTP status code | Reason | Response model |
|:-|:-|:-|
| 200 | Success | [Content Type](/model/content-type.md) |
| 404 | Project not found | [Error](/key-concepts/errors.md) |
| 500 | Internal server error | [Error](/key-concepts/errors.md) |
**TODO: Add validation responses**

### Validations

| Type | Description |
|-|-|
| Project does not exist | A project must exist to be able to create content types |
| Non-unique id | The content type must be unique for the project |

### Remarks

If the *defaultLanguage* value is not included in the *supportedLanguages* array then it will automatically added by the service when the project is created. Additionally, if the *defaultLanguage* is not specified then the [project](/model/project.md) *primaryLanguage* will be automatically set as the value by the service.





## Update a content type

Creates a new content type resource.

<span class="label label--put">PUT</span> /api/management/projects/**{projectId}**/contenttypes/**{contentTypeId}**

### Example request

```http
PUT: /api/delivery/projects/movieDb/contenttypes/movie

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
      "dataType": "string",
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
      "dataType": "string",
    },
    {
      "id": "overview",
      "name": {
        "en-GB": "Overview"
      },
      "dataType": "String",
      "dataFormat": "html",
    },
    {
      "id": "releaseDate",
      "name": {
        "en-GB": "Release Date"
      },
      "dataType": "dateTime",
      "validations": null
    },
    {
      "id": "actors",
      "name": {
        "en-GB": "Actors"
      },
      "dataType": "ObjectArray",
      "dataFormat": "entry",
      "validations": {
        "contentType": {
          "contentType": "actor"
        }
      }
    }
  ],
  "defaultLanguage": "en-GB",
  "supportedLanguages": [
    "en-GB",
    "fr-FR",
    "de-DE",
    "es"
  ],
  "workflowId": "ContensisMultilingual",
  "dataFormat": "entry"
}
```

### Response messages

| HTTP status code | Reason | Response model |
|:-|:-|:-|
| 200 | Success | [Content Type](/model/content-type.md) |
| 404 | Project not found | [Error](/key-concepts/errors.md) |
| 500 | Internal server error | [Error](/key-concepts/errors.md) |
**TODO: Add validation responses**

### Validations

| Type | Description |
|-|-|
| Project does not exist | A project must exist to be able to create content types |
| Non-unique id | The content type must be unique for the project |

### Remarks

If the *defaultLanguage* value is not included in the *supportedLanguages* array then it will automatically added by the service when the project is created. Additionally, if the *defaultLanguage* is not specified then the [project](/model/project.md) *primaryLanguage* will be automatically set as the value by the service.
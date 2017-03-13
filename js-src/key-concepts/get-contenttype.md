# Get a single content type

**GET:** /api/delivery/**{projectId}**/contenttypes/**{contentTypeId}**

## Parameters

| Name | Parameter type | Type | Format | Description |
|:-|:-|:-|:-|:-|
| projectId | path | string | | The project identifier |
| contentTypeId | path | string | | The content type identifier |

## Example request

@TODO: Dotnet example to JS

## Response messages

| HTTP status code | Reason | Response model |
|:-|:-|:-|
| 200 | Success | [Content type](/model/content-type.md) |
| 404 | Project not found | [Error](/key-concepts/errors.md) |
| 500 | Internal server error | [Error](/key-concepts/errors.md) |

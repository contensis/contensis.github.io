# Get a single project

**GET:** /api/delivery/**{projectId}**

## Example request

```http
GET: /api/delivery/projects/movieDb
```

## Response messages

| HTTP status code | Reason | Response model |
|:-|:-|:-|
| 200 | Success | [Project](/model/project.md) |
| 404 | Project not found | [Error](errors.md) |
| 500 | Internal server error | [Error](errors.md) |

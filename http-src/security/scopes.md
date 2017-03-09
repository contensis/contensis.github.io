# Scopes

OAuth2 Scopes allow a developer to specify which resource access their application requires. These are included as a space-separated list value for the scope parameter when invoking an [Authentication](./authentication.md) request.

| Scope name | Associated methods |
|:-|:-|
| Entry_Read | <ul><li>[Get Entry by id](/accessing/get-entry.md)</li><li>[List Entries](/accessing/list-entries.md#listall)</li><li>[List Entries for content type](/accessing/list-entries.md#listbycontenttype)</li></ul> |
| ContentType_Read | [Get content type](/accessing/get-contenttype.md) |
| Project_Read | [Get project](/accessing/get-project.md) |

## Example request with scopes

```http
POST: https://cms-yourcontensis.com/authenticate/connect/token
Content-Type: application/x-www-form-urlencoded
Accept: application/json

grant_type=client_credentials&
client-id=bda30e56-4faf-412c-b460-6fce9342b162&
client-secret=1e2759cee76b4ae7947722be71cc33e1-56a63ae1361241fdab7c9ee90cc8a6b3-6dc4c02b8eda43d49de499ad5eef1160&
scope=Entry_Read ContentType_Read Project_Read
```
# Scopes

OAuth2 Scopes allow a developer to specify which resource access their application requires. These are included as a space-separated list value for the scope parameter when invoking an [Authentication](./authentication.md) request.

|Scope name|Associated methods|
|-|-|
|Entry_Read|[Get Entry by id](/accessing/get-entry.md)<br />[List Entries](/accessing/list-entries.md#listall)<br />[List Entries for content type](/accessing/list-entries.md#listbycontenttype)|
|ContentType_Read|[Get content type](/accessing/get-contenttype.md)|
|Project_Read|[Get project](/accessing/get-project.md)|
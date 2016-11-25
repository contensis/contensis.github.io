# Errors

Things go wrong, either because the client is asking for something that does not exist, a network failure occurred or a bug is in the code. All non-success HTTP responses are treated as errors and are wrapped up in the client APIs to allow them to be handled.

## Error types

| Status Code | Error Code | Description |
| ----------- | -------------- | ----------- |
| 400 | BadRequest | The action is not valid |
| 403 | AccessDenied | The action is not authorized for the current user |
| 404| NotFound | The resource does not exist at the specified endpoint |
| 500 | ServerError | Something went wrong processing the request |

Ensure all status codes we expose are covered

## Handling errors

Errors returned as HTTP errors are subsequently handled in an appropriate language specific manner.

{% method -%}
### Example

Handling .NET exceptions:

{% sample lang="cs" -%}
```cs
try
{
    // Get a specific entry
    var entry = filmProject.Entries.Get("9c64e11e-fcf0-44a6-adff-41e13de15515");

    // Update a value
    entry.Set("yearOfRelease", 1978);

    // Commit the change
    entry.Save();
}
catch(ValidationException valEx)
{
    // Validation error(s)
}
catch(ApiException apiEx)
{
    // Something went wrong, likely on the server
}
catch(Exception ex)
{
    // Something else went wrong and was unhandled
}
```

{% sample lang="js" -%}
```js
// TODO
```

{% endmethod %}
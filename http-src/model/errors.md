# Errors

Things go wrong, either because the client is asking for something that does not exist, a network failure occurred or a bug is in the code. The Delivery API returns error detail in a generic format so that it can be easily handled in a consistent way. Detailed error information is not exposed in the response to ensure security sensitive details are not leaked. 

## Error types

Below are the current status codes returned from the Delivery API.

| Status Code | Error Code | Description |
| ----------- | -------------- | ----------- |
| 400 | BadRequest | The action is not valid |
| 403 | AccessDenied | The action is not authorised for the current user |
| 404 | NotFound | The resource does not exist at the specified endpoint |
| 500 | ServerError | Something went wrong processing the request |


## Error response body structure

| Name | Type | Format | Description |
| :--- | :--- | :----- | :---------- |
|logId|string|GUID|The logId as a 128 bit GUID.<br />This can be used within the Contensis log search screen to understand further details about the error |
|message|string||A description of the error|
|data|any||The logId as a 128 bit GUID. Will be null for validation errors|
|type|string||The type of error - for the Delivery API, this will always be 'error'|

## Example

```http
500 - ServerError
{
    "logId": "63cb1df0-b82a-459e-accc-635e187f3b8b",
    "message": "An error occurred ",
    "data": {
        "entryId": "ba8a92bd-0e5f-465e-acec-3cdb3db38df6",
        "projectId" "moveiDb"
    },
    "type": "error"
}
```

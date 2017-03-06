# Authorization

## Bearer token

On a success authentication response the access_token value must be set as the Authorization HTTP header for all REST requests and must be formatted as follows:

```http
Authorization: bearer {access_token}
```

Periodically the access token will expire to ensure that if the access token is compromised then any grants are short lived. This expiry can be forecast by using the "expires_in" value returned from an Authentication response or can be handled by catching a `401 - Unautorized` response.

```http
401 - Unauthorized
{
  "message": "Authorization has been denied for this request."
}
```

On an expiry a new access token will need to be requested using the same mechanism as the initial token request.

>*NOTE*  
>If you want to implement your own Delivery API wrapper, then the implementation must implement the OAuth2 Client Credential flow as specified in [RFC-6749 standard](https://tools.ietf.org/html/rfc6749#section-4.4) using the discovery document located at `https://*YOUR_CMS_URL*/authenticate`.
# Authentication

## Overview

To access any resource from the Delivery API, a client needs to be authenticated with the Zengenti OAuth2 Identity provider, which is hosted alongside the Contensis web application. Websites are authenticated using the [Client Credential flow](https://www.membrane-soa.org/service-proxy-doc/4.2/security/oauth2/flows/credentials/) which grants access to resources in a project.

The client provides both a *clientId* and a *shared secret* (which can be created and obtained from the [API Management screens]()) as part of the [API initialization](/delivery-api/api-instantiation.md). These are used to request an *access token* from the authentication provider which are then cached locally and passed along with each request as a HTTP header to the Delivery API services. If the authentication request fails then a 401 HTTP status code is returned and an exception is thrown.

Periodically the access token will expire to ensure that if the access token is compromised then any grants are short lived. On an expiry a new access token is requested using the same mechanism as the initial token request. All this functionality is wrapped up in the C# Delivery API.
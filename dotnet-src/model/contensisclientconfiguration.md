# ContensisClientConfiguration

The ContensisClientConfiguration is a container for the options that are required for setting the defaults settings.

## Syntax

```cs
// Constructor
public ContensisClientConfiguration(string rootUrl, string projectId, VersionStatus defaultVersionStatus = VersionStatus.Published,
    string clientId = null, string sharedSecret = null)
{
}

```

## Properties

| Name | Type | Description |
| :--- | :--- | :---------- |
| RootUrl | string | The url to the root of the Delivery API services |
| ProjectId | string | The project identifer, e.g. "movieDb" |
| DefaultVersionStatus | VersionStatus | The default version to pass for all [Entry](/model/entry.md) requests |
| ClientId | string | The client id value obtained from the [API Management screens](https://contensis.github.io/docs/api-keys/) |
| SharedSecret | string | The shared secret value obtained from the [API Management screens](https://contensis.github.io/docs/api-keys/) |
# API instantiation

## Default configuration

The default configuration can be set once on the application startup, which will be effective for all ContensisClient instantiations, negating the need to provide configuration values each and every time the API is used. On the startup of a Contensis website, the configuration code is automatically set to reflect the context of the publishing server, ensuring that the correct service root url, project API id and version status (Published or Latest) are set. 

Additionally, the security properties are set, which simplifies the usage of the API. The client ID and shared secret are obtained from the API key management screen. This is then used to call the security service to obtain a claims-based bearer token and to validate that the user can access resources from the service. 

<!--The list of scopes define what you would like your client to be able to do ([see the scopes section for more information](./scopes.md)).-->

This same approach can be used in non-Contensis based frameworks such as ASP.NET MVC or the Nancy framework.

##### API initialisation

This example demonstrates how the default configuration can be set using the [ClientClientConfiguration](/model/contensisclientconfiguration.md) type.

```cs
using Zengenti.Contensis.Delivery;

var defaultConfiguration = new ContensisClientConfiguration(
    rootUrl: "http://cms.contensis.com",
    projectApiId: "myProject",
    defaultVersionStatus: VersionStatus.Latest, // default: Published
    clientId: "651465e0-2fb8-4b0f-aa2f-1ab34cfe0513",
    sharedSecret: "2327d623-d44e-41ef-a837-717a626f4b75-098348eb-b0a6-4023-a64a-805536024dfb-1a558c9c-49dc-4709-9e8b-c203f60fda80"
);
 
ContensisClient.Configure(defaultConfiguration);
```

## Client creation

All operations for the API hang off the ContensisClient type, which is created using the static method ContensisClient.Create(). The Create() method allows parts of the Default configuration to be partially or completely overridden for that instance.


##### Creating a ContensisClient

```cs
@using Zengenti.Contensis.Delivery;
 
@{
    // Create with full configuration settings
    var client = ContensisClient.Create("projectId", "http://cms.contensis.com", "{client_id}", "{shared_secret}", versionStatus = VersionStatus.Latest);
    
    // Create with default configuration
    var client = ContensisClient.Create();

    // Create with default configuration, but targetting a different project
    var client = ContensisClient.Create("sharedAssets");

}@

```
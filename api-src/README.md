# Instantiation

## Default Configuration

Default configuration can be set once on the application startup which will be effective for all ContensisClient instantiations, negating the need to provide configuration values each and every time the API is used. On the startup of a Contensis website, the configuration code is set to reflect the context of the publishing server, ensuring that the correct service url, project API id, project default language and delivery context \(server type - preview or live\) are set. Additionally the security properties are set, which simplifies the usage of the API. This same approach can be used in non-Contensis based frameworks such as ASP.NET MVC or the Nancy framework.




# Delivery API Docs

## Introduction

The Delivery API is our primary API, designed and focused on enabling you to get content and data into your webpages or applications as quickly and easy as possible. The data consumed from this API is readonly and focused solely on content retrieval for information websites or mobile applications. 

The API is primarily a set of RESTful services to ensure maximum compatibility, delivering content as JSON data and resource files (assets) as text or binary files. 

We envisage that the majority of requirements in your application can be fulfilled using this API, however if your requirements entail the need to add or update content, then take a look at our [Management API]() instead.

## Documentation

The documentation is mainly example-driven with API references to the types for the specific languages:

## Key Concepts

[Get started with the Delivery API Quickstart](./getting-started.md)

[API Instantiation](./api-instantiation.md)

[Getting an Entry](./accessing-entries/entry-get.md)

[Listing Entries by Type](./accessing-entries/entries-list.md)

[Searching for Entries](./accessing-entries/entry-search.md)

## Models

Entries [ [HTTP](./model/http/entry-http.md), [.NET](./model/dotnet/entry-dotnet.md) ]

Assets [ [HTTP](./model/http/asset-http.md), [.NET](./model/dotnet/asset-dotnet.md) ]

Date Range [ [HTTP](/common/types/http/daterange-http.md), [.NET](/common/types/dotnet/daterange-dotnet.md) ]

Quote [ [HTTP](/common/types/http/quote-http.md), [.NET](/common/types/dotnet/quote-dotnet.md) ]

Location [ [HTTP](/common/types/http/location-http.md), [.NET](/common/types/dotnet/location-dotnet.md) ]

Composed Field [ [HTTP](/common/types/http/composed-http.md), [.NET](/common/types/dotnet/composed-dotnet.md) ]
# Content Modelling

You define content models in Contensis by creating content types  against a project. Content modelling is restricted to the content types in a given project although you can access content types against multiple projects through our APIs.

## Content types
A content type describes a type of content broken down into chunks.

> *e.g.* A ‘Film’ content type could contain the following chunks. Title, Film Poster, Length/Run Time, Budget, Overview, Director and cast members.

You create a content type using our content type builder or you can programmatically create a content type defined in JSON using our Management API.

Chunks in a content type are defined by fields. A field allows input of a particular type of data. A range of [field types]() are supported.

A field has a name, a data type and a set of additional properties such as validation, editor types and editorial guidelines.

Content types can be linked together using entry reference fields to aid the building of rich content models and relationships.

> *e.g.* Linking a film to a list of cast members located in a content type of people.

## Entries
Each item of content created from a content type is referred to as an entry. An entry contains the structured chunks of content defined by the content type.

In our film content type example, an entry would represent a single film containing its title, artwork, release date, overview text and other field values. Additional films can be added by creating new entries.

## Summary
These two core concepts allow rich content models to be defined and used in your website or application and form the basis of content modelling in Contensis.


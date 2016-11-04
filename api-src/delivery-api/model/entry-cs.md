# Overview

A full [overview of entries can be found here [TODO]]()

An entry definition in the Delivery API contains a mixture of standard properties and properties that have been defined by the content type that an entry is based on. 

## Standard Properties

These are the standard properties that all entries have. The languageCode property is the indexer for the entry data as an entry can have multiple language variations which can be be edited and versioned independently using the Management API. In the Delivery API context only a single language variation is available on an entry. 

### Entry

| Property | Type | Description |
| :------- | :--- | :---------- |
| Id | Integer | The entry identifier |
| ContentTypeId | string  | The API identifier of the Content Type that the Entry is based on |
| ProjectId | string | The API identifer of the project the entry belongs to |
| DataFormat | string | Either 'entry' or 'asset' |
| LanguageCode | string | The language of the Entry instance |
| Version | VersionInfo | Version information for the Entry | 
| MetaData | MetaData | MetaData associated with the Entry instance | 

### VersionInfo

| Property | Type | Description |
| :------- | :--- | :---------- |
| Created | DateTime | The date the entry was created |
| CreatedBy | string | The user id of who created the entry |
| Modified | DateTime | The date the entry version was last modified |
| ModifiedBy | string | The user id of who last modified the entry |
| Published | DateTime | The date the entry version was last published |
| PublishedBy | string | The user id of who last published the entry |

## Methods

| Method | Returns | Description |
| :----- | :------ | :-----------|
| [Get(string fieldName)](./entry-methods-cs.html#get) | dynamic | Gets a field item by name and returns a dynamic object |
| [Get`<Type>`(string fieldName)](./entry-methods-cs.html#gett) | Type | Gets a field item by name and attempts to cast to the specified generic type |
| [HasValue(string fieldName)](./entry-methods-cs.html#hasvalue) | bool | A helper function to determine whether a field exists of has a value |
# Overview

Entries purpose and [full overview can be found here]("#")

[NEED TO TALK ABOUT ENTRY VARIATIONS]

## Properties

| Property | Type | Description |
| :------- | :--- | :---------- |
| Id | Integer | The entry identifier |
| ContentTypeId | string  | The API identifier of the Content Type that the Entry is based on |
| ProjectId | string | The API identifer of the project the entry belongs to |
| DataFormat | string | Either 'entry' or 'asset' |
| LanguageCode | string | The language of the Entry instance |
| Version | VersionInfo | Version information for the Entry | 
| MetaData | MetaData | MetaData associated with the Entry instance | 

## Methods

| Method | Returns | Description |
| :----- | :------ | :-----------|
| Get(string fieldName) | dynamic | Gets a field item by name and returns a dynamic object |
| Get`<Type>`(string fieldName) | Type | Gets a field item by name and attempts to cast to the specified generic type |
| HasValue(string fieldName) | bool | A helper function to determine whether a field exists of has a value |
# Overview

A full [overview of entries can be found here [TODO]]()

An entry definition in the Delivery API contains a mixture of standard properties and properties that have been defined by the content type that an entry is based on. 

## Standard Properties

These are the standard properties that all entries have. The languageCode property is the indexer for the entry data as an entry can have multiple language variations which can be be edited and versioned independently using the Management API. In the Delivery API context only a single language variation is available on an entry. 

| Property | Type | Description |
| :------- | :--- | :---------- |
| id | string | The entry identifier as GUID |
| contentTypeId | string  | The API identifier of the Content Type that the Entry is based on |
| projectId | string | The API identifer of the project the entry belongs to |
| dataFormat | string | Either 'entry' or 'asset' |
| [languageCode] | object | The container of the Entry data |
| [languageCode].version | object | Version information for the Entry | 
| [languageCode].version.created | string | The date the entry was created |
| [languageCode].version.createdBy | string | The user id of who created the entry |
| [languageCode].version.modified | string | The date the entry version was last modified |
| [languageCode].version.modifiedBy | string | The user id of who last modified the entry |
| [languageCode].version.published | string | The date the entry version was last published |
| [languageCode].version.publishedBy | string | The user id of who last published the entry |
| [languageCode].metadata | object | Metadata associated with the Entry instance | 


{% method -%}

## Example

This json shows an example Entry based on a Film Content Type:

{% sample lang="json" -%}
```json
{
    "id": "71f73a9b-2a13-4d63-bcc1-e8ee5047b01c",
    "contentTypeId": "film",
    "projectId": "Website",
    "dataFormat": "entry",
    "en-GB": {
        "title": "Doctor Strange",
        "yearOfRelease": 2016,
        "overview": "Dr. Stephen Strange's (Benedict Cumberbatch) life changes after a car accident robs him of the use of his hands. When traditional medicine fails him, he looks for healing, and hope, in a mysterious enclave. He quickly learns that the enclave is at the front line of a battle against unseen dark force…",
        "meta": {},
        "version": {
            "createdBy": "s.derrickson",
            "created": "2016-10-12T09:29:18.5144641+01:00",
            "modifiedBy": "b.cumberbatch",
            "modified": "2016-10-13T10:15:12.1973648+01:00",
            "publishedBy": "b.cumberbatch",
            "published": "2016-10-13T10:15:12.1973648+01:00",
            "versionNo": "2.0"
        }
    }
}
```
{% endmethod %}
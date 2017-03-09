# Linked content

An entry can link to other entries or assets as Entry, Asset or Image field types either defined as a standard entry field or as a composed field type in the content type. These link object can be singular or arrays of links of the same content type e.g. Actors. Linked content can be [unresolved](#unresolved-entries) or [resolved](#resolved-entries) depending on whether a linkDepth value has been provided as a query string parameter to an entry retrieval operation.

## Unresolved entries

An unresolved entry (or asset) is essentially a subset of the entry structure with enough information to get the correct entry variation with a subsequent HTTP call. Unresolved entries and assets is the default behaviour for linked content.

| Property | Type | Format | Description |
| :------- | :--- | :----- | :---------- |
| id | string | GUID | The entry identifier as a 128 bit GUID |
| dataFormat | string | | Either 'entry' or 'asset' |
| language | string | [Language code](/localization.md) | [Optional] The language code of the linked entry variation |

```json
{
    "id": "0a48e187-43e0-4df0-ae62-8eba4d478036",
    "dataFormat": "entry",
    "language": "en-GB"
}
```

## Resolved entries
Entries can be resolved automatically to a maximum depth of 10 using the linkDepth parameter in any retrieval operation. Being able to resolve entries in a single HTTP call can potentially have major benefits to the render performance of your webpage or application, requiring much less network requests, but can also be detrimental if the linkDepth is too deep or there are many link fields. 


### Resolution rules 
When a linkDepth is provided to an entry retrieval operation to resolve linked content, then the following rules apply:

- If a language **is** specified, then the specific language variation will be returned
- If a language **is** specified but the specific language variation does not exist, then `null` will be returned or will not be included in the array
- If a language **is not** specified, then the *defaultLanguage* value defined in the [content type](/model/content-type.md) will be used to select the appropriate entry variation to return.
- If a language **is not** specified and there is no default variation, then null is returned.
## Listing entries
Requesting a list of entries can be achieved by using one of the List method overloads.

list(contentTypeId: string): Promise<PagedList<Entry>>;
list(options: EntryListOptions): Promise<PagedList<Entry>>;

### Parameters
| Name | Description |
|:--|:--|
| id | The id of the entry |
| options | An object specifying the contentTypeId, language, pageOptions, order, linkDepth, fields. |

### Returns
A Promise that will resolve with a PagedList of entries

```js
(function(Zengenti) {
    var client = Zengenti.Contensis.Client.create();    
    client.entries.list('movies').then(function (films) {
        // films are available
        // films.pageIndex
        // films.pageSize
        // films.totalCount
        // films.items
    }, function(error) {
        console.error(error);
    });

    client.entries.list({ contentTypeId: 'movies', language: 'fr-FR', pageOptions: { pageIndex: 1, pageSize: 10 } }).then(function (films) {
        // films are available        
    }, function(error) {
        console.error(error);
    });

})(Zengenti);
```

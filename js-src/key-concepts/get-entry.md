# Get a single entry
Requesting an individual entry can be achieved by using the get method on the client's entries property.

get(id: string): Promise<Entry>;
get(options: EntryGetOptions): Promise<Entry>;

### Parameters			
| Name | Description |
|:--|:--|
| id | The id of the entry |
| options | An object specifying the id, language and linkDepth.|


### Returns
A Promise that will resolve with the entry
```js
(function(Zengenti) {
    var client = Zengenti.Contensis.Client.create();
    var movieId = 'd11315cb-4278-455b-84bb-04698db0ebd2';
    // Get the default language variation
    client.entries.get(movieId).then(function(film) {       
        // film is available to use
    }, function(error) {
        console.error(error);
    });
    // Get the French variation of the film with a link depth of 2
   client.entries.get( { id: movieId, language: 'fr-fr', linkDepth: 2 }).then(function(film) {
        // film is available to use
    }, function(error) {
        console.error(error);
    });
})(Zengenti);
```

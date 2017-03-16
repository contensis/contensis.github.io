# Get a list entries by content type
Requesting all entries for a content type can be achieved by using the list method on the client's entries property.

list(contentTypeId: string): Promise<PagedList<Entry>>; @TODO: document paged list
list(options: EntryListOptions): Promise<PagedList<Entry>>; @TODO: document options

### Parameters			
| Name | Description |
|:--|:--|
| contentTypeId | The id of the content type |
| options | An object specifying the content type id, language, page options, ordering, fields to return and linkDepth.|


### Returns
A Promise that will resolve with a paged list of entries

### Example - using content type id
```html
<ul id="film_list">
</ul>
```

```js
(function(Zengenti) {
    // Create a client
    var client = Zengenti.Contensis.Client.create();

    $(function() {
        // Get a list of movies
        client.entries.list('movies').then(function(listOfFilms) {    

            for (var i = 0, ilen = listOfFilms.items.length; i < ilen; i++) {
                // loop through the entries adding their title to the list
                var film = listOfFilms.items[i];
                $('#film_list').append($('<li />').text(film.title));
            }

        }, function(error) {
            console.error(error);
        });

    });
})(Zengenti);
```

### Example - using entry list options

```html
<ul id="film_list">
</ul>
```

```js
(function(Zengenti) {
    // Create a client
    var client = Zengenti.Contensis.Client.create();

    $(function() {
        // specify the options
        var options = {
            contentTypeId: 'movies', // get a list of movies
            language: 'fr-FR',  // get french variations
            order: ['title'],   // order by title field
            fields: ['title'],  // only return title field
            linkDepth: 1
        };

        // Get the list using the options
        client.entries.list(options).then(function(listOfFilms) {    

            for (var i = 0, ilen = listOfFilms.items.length; i < ilen; i++) {
                // loop through the entries adding their title to the list
                var film = listOfFilms.items[i];
                $('#film_list').append($('<li />').text(film.title));
            }

        }, function(error) {
            console.error(error);
        });

    });
})(Zengenti);
```
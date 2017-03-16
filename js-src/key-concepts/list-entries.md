# Get a list of all entries by content type
Requesting all entries for a content type can be achieved by using the list method on the client's entries property.

list(): Promise<PagedList<Entry>>; @TODO: document paged list
list(options: EntryListOptions): Promise<PagedList<Entry>>; @TODO: document options

### Parameters			
| Name | Description |
|:--|:--|
| options | An object specifying the language, page options, ordering, fields to return and linkDepth.|


### Returns
A Promise that will resolve with a paged list of entries

### Example - using content type id
```html
<ul id="entry_list">
</ul>
```

```js
(function(Zengenti) {
    var client = Zengenti.Contensis.Client.create();
    client.entries.list().then(function(listOfEntries) {    

        for (var i = 0, ilen = listOfEntries.items.length; i < ilen; i++) {
            var entry = listOfEntries.items[i];
            $('#entry_list').append($('<li />').text(film.entryTitle));
        }

    }, function(error) {
        console.error(error);
    });
})(Zengenti);
```

### Example - using entry list options

```html
<ul id="entry_list">
</ul>
```

```js
(function(Zengenti) {
    var client = Zengenti.Contensis.Client.create();
    var options = {
        language: 'fr-FR',
        order: ['entryTitle'],
        fields: ['entryTitle']
        linkDepth: 1
    };
    client.entries.list(options).then(function(listOfEntries) {    

        for (var i = 0, ilen = listOfEntries.items.length; i < ilen; i++) {
            var entry = listOfEntries.items[i];
            $('#entry_list').append($('<li />').text(film.entryTitle));
        }

    }, function(error) {
        console.error(error);
    });
})(Zengenti);

(function(Zengenti) {
    // Create a client
    var client = Zengenti.Contensis.Client.create();

    $(function() {
        // specify the options
        var options = {
            language: 'fr-FR',  // get french variations
            order: ['entryTitle'],   // order by entryTitle field
            fields: ['entryTitle'],  // only return entryTitle field
            linkDepth: 1
        };

        // Get the list using the options
        client.entries.list(options).then(function(listOfEntries) {    

            for (var i = 0, ilen = listOfEntries.items.length; i < ilen; i++) {
                // loop through the entries adding their title to the list
                var entry = listOfEntries.items[i];
                $('#entry_list').append($('<li />').text(film.entryTitle));
            }

        }, function(error) {
            console.error(error);
        });

    });
})(Zengenti);
```
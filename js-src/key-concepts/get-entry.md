# Get a single entry
Requesting an individual entry can be achieved by using the get method on the client's entries property.

get(id: string): Promise<Entry>;
get(options: EntryGetOptions): Promise<Entry>; @TODO: document options

### Parameters			
| Name | Description |
|:--|:--|
| id | The id of the entry |
| options | An object specifying the id, language and linkDepth.|


### Returns
A Promise that will resolve with the entry

### Example - using entry id
```html
<h1 id="film_title"></h1>
<p id="film_overview"></p>
```

```js
(function(Zengenti) {
    var client = Zengenti.Contensis.Client.create();
    var movieId = 'd11315cb-4278-455b-84bb-04698db0ebd2';
    // Get the default language variation
    client.entries.get(movieId).then(function(film) {       
        $('#film_title').text(film.title);
        $('#film_overview').text(film.overview);
    }, function(error) {
        console.error(error);
    });
})(Zengenti);
```

### Example - using entry get options

```html
<h1 id="film_title"></h1>
<p id="film_overview"></p>
```

```js
(function(Zengenti) {
    var client = Zengenti.Contensis.Client.create();
    var movieId = 'd11315cb-4278-455b-84bb-04698db0ebd2';   
    // Get the French variation of the film with a link depth of 2
   client.entries.get( { id: movieId, language: 'fr-fr', linkDepth: 2 }).then(function(film) {
        $('#film_title').text(film.title);
        $('#film_overview').text(film.overview);
    }, function(error) {
        console.error(error);
    });
})(Zengenti);
```
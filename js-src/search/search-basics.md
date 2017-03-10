# Search
```js
search(query: Query): Promise<PagedList<Entry>>;
```


## Query
The query to execute

```js
(function(Zengenti) {

    var client = Zengenti.Contensis.Client.create();
    var Query = Zengenti.Contensis.Query;
    var Op = Zengenti.Contensis.Op;

    var query = new Query(
        Op.contains('title', 'Batman'),
        Op.greaterThan('runtime', 200)
    );

    client.entries.search(query).then(function(films) {
        // films are available
        // films.pageIndex
        // films.pageSize
        // films.totalCount
        // films.items

    }, function(error) {
        console.error(error);
    });  

})(Zengenti);
```


## Sub-queries
```js
var query = new Query(
    Op.contains('title', 'Batman'),
    Op.or(
        Op.greaterThan('releaseDate', 1960),
        Op.contains('tagline', 'gotham')
    )
);
```


## Ordering
```js
var OrderBy = Zengenti.Contensis.OrderBy;
```

Order by 'releaseDate'.
```js
query.orderBy = OrderBy.asc('releaseDate');
```

Order by 'releaseDate' in a descending direction.
```js
query.orderBy = OrderBy.desc('releaseDate');
```

Multiple order clauses.
```js
query.orderBy = OrderBy.asc('title').desc('releaseDate');
```


## Paging
```js
query.pageSize = 50;
query.pageIndex = 1;
```

### Weightings
All query operators can have a weight applied.

```js
var query = new Query(
  Op.equalTo('first', 7).weight(10)
);
```

## Full example
```js
(function(Zengenti) {
    var client = Zengenti.Contensis.Client.create();
    var Query = Zengenti.Contensis.Query;
    var Op = Zengenti.Contensis.Op;
    var OrderBy = Zengenti.Contensis.OrderBy;
    var query = new Query(
        Op.contains('title', 'Batman'),
        Op.or(
            Op.greaterThan('releaseDate', 1960),
            Op.contains('tagline', 'gotham')
        )
    );
    query.orderBy = OrderBy.asc('title').desc('releaseDate');
    query.pageSize = 50;
    query.pageIndex = 1;

    client.entries.search(query).then(function(films) {
        // films are available
        // films.pageIndex
        // films.pageSize
        // films.totalCount
        // films.items

    }, function(error) {
        console.error(error);
    });
})(Zengenti);
```

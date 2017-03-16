# Image
An image type is a container of an image asset with an associated caption.

## Properties

| Name | Type | Format | Description |
| :------- | :--- | :----- | :---------- |
| asset | object | [Asset](/model/asset.md) | The asset that is linked to from the entry |
| caption | string |  | The image caption, defined in the entry |

> **Note** The caption property allows instance specific text to be associated with a linked image asset.


## Example

```html
<figure id="film_cover">
    <img />
    <figcaption />
</figure>
```

```js
(function(Zengenti) {
    // Create a client
    var client = Zengenti.Contensis.Client.create();

    $(function() {
        var movieId = 'd11315cb-4278-455b-84bb-04698db0ebd2';

        // Get the default language variation of the film
        client.entries.get(movieId).then(function(film) {    
            // Get the cover image value
            var coverImage = film.coverImage;  

            // display the cover image
            $('img', '#film_cover')
    	        .attr({
                	src: coverImage.asset.uri,
                    altText: coverImage.asset.properties.altText,
                    width: coverImage.asset.properties.width,
                    height: coverImage.asset.properties.height
                });
            // display the image caption
            $('figcaption', '#film_cover')
    	        .text(coverImage.caption);

        }, function(error) {
            console.error(error);
        });

    });
})(Zengenti);
```

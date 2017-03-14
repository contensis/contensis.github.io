# Get the current project

Requesting the current project can be achieved by using the get method on the client's project property.

**get(): Promise&lt;Project&gt;**

### Returns
A Promise that will resolve with the project
```html
<select id="language_selector"></select>
```

```js
(function(Zengenti) {
    var client = Zengenti.Contensis.Client.create();

    $(function() {
        client.project.get().then(function(currentProject) {
            var options = currentProject.supportedLanguages.map(function(lang) {

                var selected = (lang === currentProject.primaryLanguage) ? 'selected' : '';

                return $('<option />')
                    .val(lang)
                    .text(lang)
                    .attr('selected', selected);
    		});

            $('#language_selector').append(options);

    	}, function(error) {
            console.error(error);
    	});    
    });
    
})(Zengenti);
```

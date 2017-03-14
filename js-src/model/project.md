# Project
A project resource can be retrieved from the Delivery API to understand the languages that the project supports and which language is the primary language.

## Properties

| Name | Type | Format | Description |
| :------- | :--- | :----- | :---------- |
| id | string | | A unique project identifier |
| name | string |  | The friendly name given to the project |
| description | string |  | The description text given to a project |
| supportedLanguages | string [...] |  | An array of all the languages supported by the project |
| primaryLanguage | string | [Language code](/localization.md)  | The primary language for the project |


## Example

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

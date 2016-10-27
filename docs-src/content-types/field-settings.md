# Field Settings

## Name
The name property describes the field content. The name entered here will be displayed to an author when creating an entry. Its used to identify the chunk of content.

The name entered is also used to generate the field ID. 

## Field ID
The Field ID is used to identify the field within a content type through the API. Field IDs have to be unique within a content type. 

The field ID is automatically generated when entering a field name. You can update the field name up until the content type is saved, any name you enter will be sanitised.[^1] [^2]  

## Default value
The default value property sets the default content for a field when an entry is created. If no change is made by an author when editing the entry then the default entry will be used.

*e.g.* By default location fields are set to have a default location of London. If the default location is not updated by an author then the location for the entry will be set to London.

The type of default value input will vary between editors. 

## Format
Some fields support different formats of data. By changing the data format you are specifying that type of data that is stored and returned via the API. 

Depending on the format you specify you may be provided with different types of field editor for the field.

e.g. If you we're to select the date field and change its format from single to range you'd be provided with a set of editor that support date from and date to.

## Display field
The display field is used in listings, the entry reference field editor and through the API to identify entries.

For a content type to be published it requires a single text field to be present.

The first text field added to the content type will be set as the display field, if you decide you want to use another field for your displayed field you can change it at a later date.


**Footnotes**:
----
[^1]: Change the behaviour of the field id. It should be possible to change the field ID up until the content type has been published.

[^2]: What happens if a fieldID is entered that matches an existing ID?

# Field settings

## Name
The *Name* property describes the field content. The *Name* entered here will be displayed to an author when creating an entry. It's used to identify the chunk of content. This *Name* is also sanitised and used to generate the *Field ID*.

> The *Name* field is limited to 50 alphanumeric characters or symbols.

## Field ID
The *Field ID* is used to identify the field within a content type through the API. The *Field ID* is automatically generated when creating a *Name* and sanitised for use as the *Field ID*. 

*Field ID's* have to be unique within a content type. If you attempt to use a *Name* that is already in use then a number will be appended to the *Field ID*.

> The *Field ID* is limited to 50 alphanumeric characters, symbols are not supported.

## Default value
The *Default* value property sets the initial content for a field when an entry is created. If no change is made by an author when editing the entry then the default value will be used.

*e.g.* Default location fields are set to London. So, if the default location isn't changed, that entry will be set to London.

The type of default value input will vary between editors.

## Format
Some fields support different *Formats* of data. By changing the data *Format* you are specifying the type of data that is stored and returned via the API.

Depending on the *Format* you specify you may be provided with different types of field editor for the field.

*e.g.* If you were to select the date field and change its *Format* from *single* to *range* you would see a set of editors that support *date from* and *date to*.

## Title field
The *Title* field is used in listings, the *Entry Field Editor* and through the API to identify entries.

> For a content type to be published it requires a single text field to be set as the *Title*.

The first text field added to the content type will be used as the *Title* field, if you decide you want to use another field for your *Title* field you can change it at a later date.

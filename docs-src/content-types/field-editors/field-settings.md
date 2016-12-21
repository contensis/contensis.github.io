# Field settings

## Name
The *Name* property describes the field content. The name entered here will be displayed to an author when creating an entry. It's used to identify the chunk of content.

This name is also used to generate the field ID.

> The name field is limited to 50 alphanumeric characters, symbols are supported.

## Field ID
The *Field ID* is used to identify the field within a content type through the API. *Field ID's* have to be unique within a content type.

The field ID is automatically generated when entering a field name. Any name you enter will be sanitised.

If you attempt to use a name already in use then a number will be appended to the field ID.

> The field ID is limited to 50 alphanumeric characters, symbols are not supported.

## Default value
The default value property sets the default content for a field when an entry is created. If no change is made by an author when editing the entry then the default entry will be used.

*e.g.* Default location fields are set to London. So, if the default location isn't changed, that entry will be set to London.

The type of default value input will vary between editors.

## Format
Some fields support different formats of data. By changing the data format you are specifying that type of data that is stored and returned via the API.

Depending on the format you specify you may be provided with different types of field editor for the field.

*e.g.* If you were to select the date field and change its format from *single* to *range* you would see a set of editors that support *date from* and *date to*.

## Title field
The title field is used in listings, the entry field editor and through the API to identify entries.

> For a content type to be published it requires a single text field to be set as the title.

The first text field added to the content type will be used as the title field, if you decide you want to use another field for your title field you can change it at a later date.

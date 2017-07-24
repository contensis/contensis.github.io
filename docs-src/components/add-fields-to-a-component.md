# Add fields to a component
A component is made up of a set of fields. Fields allow you to break up large blobs of content into smaller chunks, making content more flexible and reusable.

Fields comprise a type, format and a field editor. The supported types, formats and editors are outlined in the following [article](/Contensis/10/kb/content-types-and-entries/field-editors/Supported-fields-and-editors.aspx "Field editors").

## Add a field

With the component open for editing:

1.  Press on the **Field Type** button in the toolbox for the field that you want to add. The field will be added to the bottom of your component.
2.  The field you've added will be active and indicated by a green border.

### Set a field name

The settings for a field will be displayed in the right hand panel when the field is active.

Give the field a name that clearly identifies its content. The field name is used to generate a sanitised field ID that a developer will use with the API. The field name will also be visible to an author when they are creating an entry.

Read through our [field settings](/Contensis/10/kb/content-types-and-entries/field-editors/Field-settings.aspx "Field settings") article to get a better understanding of each setting.

> **Warning**: If a field name has previously been used and deleted from the component and is subsequently reused, any existing entries containing that field may have data preserved and would be returned via the Delivery API. Any pre existing data would also be shown in the entry editor.

## Reordering fields in a component

You can change the order of fields in a component by using the up and down buttons displayed for a field.

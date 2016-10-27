# Adding fields to a content type
A content type is made up of a number of fields. Fields allow us to break up large blobs of content into smaller chunks, making content more flexible and reusable.

## Adding a field
Adding fields to a content type is easy. With the content type open for editing:

1. Press on one of the field type buttons in the toolbox you want to add to your content type. The field will be added to the bottom of your content type.
2. The field you added will be active, indicated by the green border that surrounds the field.

### Set field name 
The properties for the field will be displayed in the right hand panel when a field is active.

Give the field a name that clearly identifies its content. The field name is used to generate a sanitised field ID that a developer will use through the API.

The field name will also be visible to an author when they are creating an entry.

> **Note:** Once a content type has been saved its not possible to change the generate field ID. If you want to change the name you'll need to do so before saving.

Read through our [field settings](/content-types/field-settings.md) article to get a better understanding of each setting.

## Adding a field with a name previously used [^1]




## Reordering fields in a content type
You can change the order of fields in a content type by using the up and down buttons displayed against a field. Simply press the up or down arrow buttons to change the field order.

#### Footnotes

----

[^1]
**Scenario:** Re add field with the same name
- **Given** I have a content type
- **and** the content type has entries
- **When** I re add a field that previously existed
- **Then** what happens to the historical data associated with the field?


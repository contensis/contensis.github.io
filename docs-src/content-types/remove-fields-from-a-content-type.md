# Remove fields from a content type
If you no longer require a field within a content type it can easily be removed by following the steps. Be aware that this field will be removed from any published entries.

> **Warning:** Removing a field and any associated data is irreversible, only do this if you are confident that field is no longer required.

With a content type open for editing:

1. Locate the field in you content type that you want to remove.
2. Press the cross button on the field to remove it from the content type. A confirmation screen will be displayed.
3. Press delete to confirm the removal of the field.
4. Press save, followed by publish to confirm your changes.

> **Note:** Any code created referencing the removed field would return null or the default value for the type through the Delivery API.
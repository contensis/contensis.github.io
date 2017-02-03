# Remove fields from a content type
If you no longer require a field within a content type it can be removed by following the steps.

With a content type open for editing:

1. Locate the field in the content type that you want to remove.
2. Press the **cross** on the field to remove it from the content type. A *Delete field* confirmation screen will be displayed.
3. Press **Delete**, then **Save**, followed by **Publish** to confirm your changes.

## Field removal behaviour
1. The data associated with the removed field for an entry is preserved until the entry is updated and saved.
2. Any code created referencing the removed field would return null or the default value for the type through the Delivery API.

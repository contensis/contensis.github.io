# Remove fields from a component
If you no longer require a field within a component it can be removed:

1.  Locate the field in the component that you want to remove.
2.  Press the **cross** on the field to remove it from the component. A _Delete field_ confirmation screen will be displayed.
3.  Press **Delete**, then **Save**, followed by **Publish** to confirm your changes.

## Field removal behaviour

The data associated with the removed field for an entry is preserved until the entry is updated and saved.

Any code created referencing the removed field would return null or the default value for the type through the Delivery API.

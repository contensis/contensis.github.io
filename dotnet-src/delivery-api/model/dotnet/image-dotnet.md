# Images

The Image type represents a link to an image with an associated caption, if required.

## Properties

| Property | Type | Description |
| :------- | :--- | :---------- |
| Caption | `string` | The image caption, defined in the entry |
| Asset | `Asset` | The asset that is linked to from the entry |

## Remarks

The caption property allows instance specific text to be associated with an image.

Unlike entry links, an asset link is always resolved so that the full asset details are included when retrieved.

## Example

{% method -%}

### Get an Image field object

{% sample lang="cs" -%}

```cs
@{
    // Retrieve a film by it's ID.
    var filmEntry = client.Get("0aabad4e-a083-4a88-bd75-b2674e2f8298");

    // Get the field value as an Image instance.
    var coverImage = film.Get<Image>("coverImage");
}

<figure>
  <img src="@coverImage.Asset.Uri" alt="@coverImage.Asset.Propeties["altText"]" width="304" height="228">
  <figcaption>@coverImage.Caption</figcaption>
</figure>

```
{% endmethod %}

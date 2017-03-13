# Getting started

In this section you will be guided through defining and creating content using the editor screens in the Contensis UI and then rendering the content out in a Razor view using the Delivery API. Throughout the documentation we use examples based on our sample MoviesDB project.

## Assumptions

- You have an understanding of creating content in the navigation tree.
- You know how to create and edit webpages and Razor Views.

## Create a new project

[Projects](https://contensis.github.io/docs/projects/create-a-project.html) are the home for all your content in Contensis. Create a new project called MoviesDB using the default values for assets and languages.

## Create a content type

You can [create a new content type](https://contensis.github.io/docs/content-types/create-a-content-type.html) easily in the content type editors in the Contensis UI. Create a content type called *Film* with the following fields:

| Field name | API ID | Type | Description |
| ---------- | ------ | ---- | ----------- |
| Name | name | Text | The name of the film |
| Synopsis | synopsis | Text | A overview of what the film is about |
| Year of release | yearOfRelease | Number (integer) | The year the film was released |
| Cover image | coverImage | Image | A reference to the cover image asset |

**TODO: define all needed films**

## Upload the film images

Content will benefit from the inclusion of images, so now add the cover images for the films. Images are added to Contensis by [uploading them into the contensis tree] and can then be referenced within an entry as either a direct [asset link](/linked-content.md) or as an [image](/linked-content.md#image). We will be using the image type so that we can add our captions!

- [the-dark-knight.jpeg]()
- Image 2
- Image 3
- etc.

## Create some films

Now it's time to create some content!

[Create entries](https://contensis.github.io/docs/entries/create-an-entry.html) for the films using the data in the table:

| Name | Overview | Year of release |
| ---- | -------- | --------------- |
| The Dark Knight | Batman raises the stakes in his war on crime. With the help of Lt. Jim Gordon and District Attorney Harvey Dent, Batman sets out to dismantle the remaining criminal organizations that plague the streets. The partnership proves to be effective, but they soon find themselves prey to a reign of chaos unleashed by a rising criminal mastermind known to the terrified citizens of Gotham as the Joker. |  2008 |



## Create a film listing in a razor view

Great, now we can start creating the Razor View that will render the film listing in a Webpage. First, ensure that you have a new webpage created with a placeholder that allows Razor Views - if you don't know how to create your own pages then [read this tutorial](https://zenhub.zengenti.com/Contensis/R83/Development/Razor/Razoroverview.aspx).

### Syntax

```cs
@using Zengenti.Contensis.Core.Api.Delivery // Reference the Delivery API

@{
    // Create a client to allow access to the content, this will use the
    // current project context
    var client = ContensisClient.Create();

    // Get the films as a PagedList of Entries
    var films = client.Entries.List("films");
}

<div class="film-listing">

@foreach(var film in films.Items)
{
    <div class="film">
        <div class="film-name">@film.Get("name")</div>
        <div class="film-synopsis">
            <img src="@film.Get("coverImage").Asset.Properties.Uri">
        </div>
        <div class="film-synopsis">@film.Get("synopsis")</div>
        <div class="film-year-of-release">@film.Get("yearOfRelease")</div>
    </div>
}

</div>
```

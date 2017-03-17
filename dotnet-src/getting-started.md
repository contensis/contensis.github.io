# Getting started

In this section you will be guided through rendering content created using the editor screens in the Contensis UI into Razor views using the .NET Delivery API. Throughout the documentation we use examples based on movies.

## Assumptions

- You have an understanding of managing and creating content in the navigation tree.
- You know how to create and edit webpages and Razor Views.

## Create a new project (optional)

[Projects](https://zenhub.zengenti.com/Contensis/9/kb/setup-and-configuration/Administration/Create-a-project.aspx) are the home for all your content in Contensis. Either use an existing test project or create a new project called MovieDB using the default values for assets and languages (you may need to [set up a publishing server](https://zenhub.zengenti.com/Contensis/9/kb/setup-and-configuration/Configuration/Setup-and-configure-a-publishing-server.aspx) to be able to run the examples if one is not set up already).



## Create a movie content type

You can [create a new content type](https://zenhub.zengenti.com/Contensis/9/kb/content-types-and-entries/content-types/create-a-content-type.aspx) easily in the content type editors in the Contensis UI. Create a content type called *Movie* with the following fields:

| Field name | Api id | Type | Description |
| ---------- | ------ | ---- | ----------- |
| Title | title | Text | The title of the movie |
| Overview | overview | Text | A overview of what the movie is about |
| Release Date | releaseDate | Date | The date the movie was released |
| Runtime | runtime | number (integer) | The runtime in minutes |
| Poster Image | posterImage | Image | A reference to the cover image asset |


## Create a folder

Lets create a folder called 'Movies Demo' in the Contensis navigation tree to contain our webpage and razor view files. In that folder create a child folder called *images* to contain our image files. If you don't already have one, then create a basic template that can be used to create the webpages from and assign the template to the new folder. Ensure that the folder also has *C# Razor View* and *Image* content types assigned.

We will end up with the following folder and file structure.

![Demo folder structure](/images/movie-demo-files.png)


## Create some movies

Now it's time to create some content!

Head over to either [IMDB](http://www.imdb.com/) or [The Movie DB](https://www.themoviedb.org/) and choose 5 of your favourite movies to use to create the entries.

Content will benefit from the inclusion of images, so add the cover images for the movies into the images folder and link to them from your newly created entries. Images are added to Contensis by [uploading them into the contensis tree](https://zenhub.zengenti.com/Contensis/9/kb/Assets-uploadable-content/Images/upload-an-image.aspx) and can then be referenced within an entry as either a direct [asset link](/key-concepts/linked-content.md) or as an [image](/key-concepts/linked-content.md#images). We will be using the image type so that we can add captions!


## Create a movie listing in a razor view

Next create the Razor View that will render the movie listing in a Contensis webpage. First, ensure that you have a new webpage called 'Movies' created in the demo folder with a placeholder that allows Razor Views. 

> **NOTE** 
> If you don't know how, then [learn how to create your own pages with Razor views](https://zenhub.zengenti.com/Contensis/R83/Development/Razor/Razoroverview.aspx).

Create a new C# Razor View called *Movie-Listing* within the demo folder with the following code. 

```cs
@using Zengenti.Contensis.Delivery

@{
    // Add foundation to help align elements
  	CurrentContext.Page.CSS.Add("https://cdnjs.cloudflare.com/ajax/libs/foundation/6.3.1/css/foundation.min.css");
  
    // Create a client to allow access to the content
    var client = ContensisClient.Create();

    // Get the movies as a PagedList type
    var movies = client.Entries.List("movie");
}

<div class="movie-listing">

@foreach(var movie in movies.Items)
{
  
    <div class="row">
        <div class="large-2 columns">
            <img src="@(movie.Get<Image>("posterImage").Asset.Uri)">
        </div>
        <div class="large-10 columns"><a href="./movie-record.aspx?id=@movie.Id">@movie.Get("title")</a></div>
    </div>
}

</div>
```

Submit and approve the razor view so that it can be used in a webpage. Insert the razor view into the placeholder in the Movies webpage and you can then preview the changes.

This should output the following webpage when previewed.

![movie-listing](/images/movie-listing.png)


## Create a movie record page

Now we have a listing page, lets create a record page to display further details about a movie.

First, create a new webpage based on your basic template called *Movie Record* and a new razor view called *Movie Record*.

Add the following code into the razor view and insert the razor view into a placeholder in the new webpage.


```cs

@using System.Web;
@using Zengenti.Contensis.Delivery

@{
    // Add foundation to help align elements
  	CurrentContext.Page.CSS.Add("https://cdnjs.cloudflare.com/ajax/libs/foundation/6.3.1/css/foundation.min.css");
  
    // Create a client to allow access to the content
    var client = ContensisClient.Create();
  
  	// Get entry id passed in on the querystring
  	var movieId = Request.QueryString["id"];

    // Get the entry by id
    var movie = client.Entries.Get(movieId);
}

<div class="movie-record">

    <div class="row">
        <div class="medium-2 columns"><img src="@(movie.Get<Image>("posterImage").Asset.Uri)" /></div>
        <div class="medium-10 columns"><h2>@movie.Get("title")</h2></div>
    </div>
  	<div class="row">
        <div class="medium-2 columns">Overview</div>
        <div class="medium-10 columns"><p>@movie.Get("overview")</p></div>
    </div>
  	<div class="row">
        <div class="medium-2 columns">Release Date</div>
        <div class="medium-10 columns">@movie.Get("releaseDate").ToShortDateString()</div>
    </div>
  	<div class="row">
        <div class="medium-2 columns">Runtime</div>
        <div class="medium-10 columns">@movie.Get("runtime") minutes</div>
    </div>


</div>

```

This should output the following webpage when previewed.

![movie-listing](/images/movie-record.png)



When writing documentation for ZenHub we use markdown and GitHub as a means of collaboration and not introducing presentation in to our writing.


## Front matter

We use front matter at the top of our markdown files in order to provide additional information outside of the article content that may be used by other systems.

```
---
keywords: keyword, keyword, keyword
description: This is the meta description used by search engines
title: This is the meta title of the page
menuname: This value will be displayed in a menu
path: /9/kb/content-types-and-entries/content-types/
---
```


## Notices

### Info box
```
<aside class="alert-box info">
This is an aside
</aside>
```

**Example**

<aside class="alert-box info">
<p><strong>Info</strong>: This is an info box</p>
</aside>

### Warning box

```
<aside class="alert-box warning">
This is an aside
</aside>
```
**Example**
<aside class="alert-box warning">
<p><strong>Warning</strong>: Deleting a content type is irreversible, only do this if you are confident that the entries and content type are not in use and are no longer required.</p>
</aside>

# Methods

When referring to API methods such as GET, PUT, POST etc we have introduced some basic HTML formatting to help give some additional semantic meaning that can also be styled.

## Examples

<ul>
  <li><span class="label label--put">PUT</span>  /api/delivery/projects/{projectId}</li>
  <li><span class="label label--post">POST</span> /api/delivery/projects/{projectId}</li>
  <li><span class="label label--get">GET</span> /api/delivery/projects/{projectId}</li>
  <li><span class="label label--delete">DELETE</span> /api/delivery/projects/{projectId}</li>
  <li><span class="label label--patch">PATCH</span> /api/delivery/projects/{projectId}</li>
</ul>

By wrapping the method type with a `<span></span>` tags and introducing a label class `class="label"` and a subsequent modifier class `class="label label--put"` we can provide some richer styling that couldn't be achieved with any other HTML element.

## PUT example

```
<span class="label label--put">PUT</span>
```

<span class="label label--put">PUT</span>

## PUT large example

```
<span class="label label--large label--put">PUT</span>
```

<span class="label label--large label--put">PUT</span>

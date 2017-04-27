# Code examples

When creating API documentation, GitBooks supports code highlighting using the prism highlighter.

## Multiline code examples

Multi line code examples should use fenced code blocks, with the optional language name indicated after the first set of back ticks. When GitBooks parses the code block it uses the language identifier as a css class for the highlighter to use.

This is a common convention used by various syntax highlighters across the web. Whilst the majority of the highlighters will detect the correct language, appending the language after the opening of the code block ensures the correct language is used by the highlighter.

A full list of supported highlighters can be found in the [Prism documentation](http://prismjs.com/index.html#languages-list).

### Explanation
A code example always requires an explanation, but this can be achieved in two ways. You have to ask yourself the question is this page highlighting a single concept or multiple?

#### Single concept
Where a page is about a single concept a simple heading of **Example** is sufficient as the page should provide the context to the example.

#### Multiple concepts
Where a page talks about multiple concepts, code examples should not be provided without any explanation. A simple paragraph explaining the code example should be provided before each example.


---

## Examples
The following two examples demonstrate the approach that should be taken when providing a code example.

### Example HTTP Response
This is an example from the HTTP Delivery API. The [page](https://developer.zengenti.com/contensis/api/delivery/http/key-concepts/errors.html) provides the context to the code example.

#### Markdown

```

`500 - ServerError`

```json
{
  "logId": "63cb1df0-b82a-459e-accc-635e187f3b8b",
  "message": "An error occurred requesting the entry",
  "data": {
      "entryId": "ba8a92bd-0e5f-465e-acec-3cdb3db38df6",
      "projectId" "moveiDb"
  },
  "type": "error"
}
```

<aside class="alert-box info">
<p><strong>Note</strong>: Please note this example is missing the  <code>```</code> closing fence block</p>
</aside>


#### Render

`500 - ServerError`

```json
{
  "logId": "63cb1df0-b82a-459e-accc-635e187f3b8b",
  "message": "An error occurred requesting the entry",
  "data": {
      "entryId": "ba8a92bd-0e5f-465e-acec-3cdb3db38df6",
      "projectId" "moveiDb"
  },
  "type": "error"
}
```

---

### c# Example
This is an example from the .NET Delivery API. The [page](https://developer.zengenti.com/contensis/api/delivery/dotnet/key-concepts/api-instantiation.html) has multiple concepts on the page and each code example has an explanation.

#### Markdown
```
This is how the majority of clients are created within Contensis razor views.

```cs
var client = ContensisClient.Create();
```

<aside class="alert-box info">
<p><strong>Note</strong>: Please note this example is missing the  <code>```</code> closing fence block</p>
</aside>

#### Render
This is how the majority of clients are created within Contensis razor views.

```cs
var client = ContensisClient.Create();
```  

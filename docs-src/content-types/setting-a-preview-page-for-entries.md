# Setting up a preview page for entries
If you want to enable a preview for your entry content then you'll need to provide a URL to a page that contains a razor view, that will render your content. 

1. Open the content type you want to set a preview for by pressing the edit icon in the content type listing screen.
2. When the content type builder opens, the settings for the content type are displayed in the right hand panel.
3. Enter a URL in the *Preview URL* text box with a query string parameter that expects the GUID of an entry

	*e.g.* http://mywebsite.com/products/products.aspx?id={GUID}&language={LANG}
	
	> **Note:** You can use the {GUID} and {LANG} strings to specify where you want the GUID and language of the entry to be placed in the URL.

4. Once the URL has been set a preview button will be present in the entry editor to preview your content.




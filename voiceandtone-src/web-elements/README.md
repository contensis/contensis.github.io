## Buttons and icons
When referring to specific buttons or icons – use the label or name as it is displayed in the UI.

- If a button is labelled (e.g. Save), always use the label
- If an icon isn’t labelled (e.g. Management Console), refer to it consistently:
Management Console – not “Cog icon,” the cog, etc
- Project Search – not the spyglass, the search icon
- When referring to a button, use of capitals is acceptable (to maintain consistency with Contensis UI)

## Bullet lists
Use bullet lists where appropriate, but don't shoehorn a paragraph into a list. 

- Be consistent about adding full stops at the end of a bullet item – don’t unless it’s a sentence.
- Be consistent about using capitals at the start of a bullet - don’t unless it’s a sentence.
- If the list is too long (15+), split it into two or more sub categories.

Keep the listed items in the same part of speech. For example, if you want to say that new features include a list of things, don't do this:

- The Forms builder lets you create customisable forms.
- Managing links
- Form element styling
- Emailing notifications

**Do this, instead:**

- Link management
- Form element styling
- Email notifications

## Click, tap or press
When documenting behaviour in the Contensis UI we should refer to a click as a press. This ensures we are covering touch behaviour or trackpad behaviour where a click isn't actually happening. 

## Code
Use monospaced fonts for short code snippets and settings. Use gists for longer bits of code.

## Headings
Headings are essential for SEO and accessibility. Headings range in importance from H1 to H6, and should be properly organised to make your page accessible to screen readers and search engines. 

Follow semantic headings. So, a heading 1 is followed by a heading 2 – and not a heading 3, 4, or 5.

**We use sentence-case capitalisation** in headings instead of title case. So, capitalise the first word (and any proper nouns), but not every word in a heading:

Sentence-case examples:
- Running a user-experience workshop
- Using CSS for site layout
- Creating Contensis templates

Title-case examples to avoid:
- Finding the Right People for your Team
- Inserting Scripts into a Template

## Images and videos
It’s sometimes quicker to share a concept using an image or video. Videos and images should reinforce the text on the page. Never introduce ideas in visuals that aren’t explained in the text on the page.

- Use alt-text to provide assistive technology with the meaning behind the image.
- Control image or video size, quality and format to deliver a fast loading, responsive site.
- Different types of images should be encoded into different formats depending on what type of image it is, what the browser supports, and what needs the page has. Consider this from the outset.

## Layout
A good rule of thumb is to consider your mobile readers from the start. 
Do you like swiping through pages of text when reading on a smartphone? Didn’t think so.

Avoid having more than 2 or 3 paragraphs in succession without a break.

- Use images, lists and blockquotes to break up the page.
- Use sub headings every few paragraphs to provide document structure aid skim reading.

## Links
Meaningful link text makes pages more friendly for visitors (especially those using screen readers) and search engines. The link text should always describe what the user will see when they click on it. It should never be "Click Here", "Here", or the URL itself. 

For example, if you want to link to a page about permissions, don't do this:

...an administrator needs to setup their permissions. <a href="https://zenhub.zengenti.com/Contensis/9/kb/setup-and-configuration/Administration/permissions.aspx">Click here</a> to read more about permissions.

**Do this, instead:**

...an administrator needs to setup their <a href="https://zenhub.zengenti.com/Contensis/9/kb/setup-and-configuration/Administration/permissions.aspx">permissions</a>.

### Formatting links
Links anywhere in body text should be underlined, but not in titles, long lists or landing pages. 

## Paragraphs
Each paragraph should address a single point or idea. They should not be too long, nor should they ramble. Start each paragraph with one or two sentences containing the key information or conclusion.

- Use blank lines to demarcate paragraphs. Do not indent the first line of a paragraph.

## Poster images
Make sure they’re compressed for web. Try to avoid images with white edges – this causes the image to bleed into the page. If you can't avoid white edges, add a grey stroke (in the HTML code).

Poster images for ZenHub videos need to be 1280 x 720px.

## Screenshots
- Screenshots illustrate a procedure that's difficult to understand. You don't have to have a screenshot for every step - just the ones where you want to make sure someone doesn't miss an important detail.
- They include enough context that someone can tell what part of the interface they are viewing, don't include the whole screen if its unnecessary, crop to the area thats valid.

## Tables
- Do not use bold headings
- Headings should always be in a `<thead>`
- Table body should always be in a `<tbody>`
- Tables need captions (right click, properties, add caption)
- Don’t have \<p> tags in table contents i.e. `<td>Hello</td>` not `<td><p>hello</p></td>`

## Underlining
Never underline anything that is not a link.

## Video
We usually show videos below the intro paragraph on a ZenHub page. It's good practice to display a helpful/informative poster image.

## URLS
We use lowercase characters in out URL structures in all cases.

For example: https://zenhub.zengenti.com/Contensis/10.1/kb/Assets-uploadable-content/Video/Insert-a-video.aspx

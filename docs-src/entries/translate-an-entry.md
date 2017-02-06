# Translate an entry
When you want to create content in an alternative language to the default you'll need to create a language variation.

A language variation is associated with a default language entry which acts as a container for all language variations. The number of languages available will depend on those supported for the [content type](/content-types/enable-disable-languages.md).

## Create a language variation
If you have created and published an entry in the default language of a content type, then a language variation of the entry will be visible for any supported languages in the entry listing.

1. Press the **Content Types & Entries** button in the sidebar. The **Content Types & Entries** drawer will open revealing a number of options.
2. Select **Entries** from the drawer to open the *Entries Listing* screen.
3. Select the language you want to display entries for from the *Language Filter* dropdown.
4. You can reduce the number of entries displayed by selecting the content type the entry is based on using the *Content Type Filter*. The entry listing will be updated to display all entries for the content type and languages you've selected.
5. Each entry in the listing has its own status, new entries requiring translation will be indicated by the *Not yet translated* [workflow state](/entries/workflow-states.md).
6. Locate the entry in the listing that you want to translate and press **Translate**. The entry will open in a split view editor for editing.

> The master language content will be displayed in the left hand panel, the other panel represents the language you are currently editing and its fields will be empty.

7. You can now populate the fields for the new language.
8. Press **Save** between any changes that have been made. When you are ready to publish the entry press the **Publish** button. The language variation will now be available through the Delivery API along with the default language content.

> The minor version will increment upon each save. Take a look at our [entry versioning](/entries/entry-versioning.md) article for more detail on how entries are versioned.

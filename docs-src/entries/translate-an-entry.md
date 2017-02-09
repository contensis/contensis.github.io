# Entry translation

## Overview
Entry translation follows a strict workflow and entries can only be created in another language once there is a published version of the default language. This workflow ensures that as the default language entry is updated, authors of different languages will see that a change has been made. The change will be highlighted by the entries workflow state e.g. an entry is *Awaiting Translation*.

All language variations are associated with a default language entry. The default language entry acts as a container for all language variations. The default language for an entry is the default language of the project. The number of languages available for a given entry will depend on those supported by the [content type](/content-types/enable-disable-languages.md).

Once an entry has been created and published in the default language then each of the language variations become available for translation.

## Translate an entry from the language panel
1. Press the **Content Types & Entries** button in the sidebar. The *Content Types & Entries* drawer will open revealing a number of options.
2. Select **Entries** from the drawer to open the *Entries Listing* screen.
3. You can reduce the number of entries displayed by selecting the content type the entry is based on using the *Content Type Filter*. The entry listing will be updated to display all entries for the content type you've selected.
4. Locate the entry in the listing that you want to translate. If the entry is available in other language variations then you will see *Available in other languages* in the language column of the listing. Press **Available in other languages** and the language panel will be displayed.
5. The language panel shows all available language variations for the selected entry. Entries not yet translated will have an action to translate, whilst those already translated will be available to edit. Pressing **Translate** or **Edit** will open the entry in a split view entry editor for translation.
	
	> The default language content will be displayed in the left hand panel, the other panel represents the language you are currently editing.

6. You can now populate the fields for the new language. If you come across a field that requires the same content from the default language, such as an image, you can use the copy field action from the default language field editor, this will save time where the content remains the same.
7. Press **Save** between any changes that have been made. When you are ready to publish the entry press the **Publish** button. The language variation will now be available through the Delivery API along with the default language content.

	> The minor version will increment upon each save. Take a look at our [entry versioning](/entries/entry-versioning.md) article for more detail on how entries are versioned.

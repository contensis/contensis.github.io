# Deleting entries
Deleting an *Entry* or language variation will permanently remove the entry from your project.

> **Note:** Deleting an entry is irreversible, only do this if you are confident that the entry is no longer required.

## Single language
If your content type contains a single language e.g. the default language assigned to the project, then follow these steps to delete an entry.

1. Press the **Content Types & Entries** button in the sidebar. The *Content Types & Entries* drawer will open revealing a number of options.
2. Select **Entries** from the drawer to open the *Entries* listing screen.
3. Locate the *Entry* you want to delete either by scrolling through the listing or by using the [filters](/entries/view-and-filter-entries.md).
3. Press the *Delete* button in the listing, a *Delete confirmation* window will appear.
4. Confirm the deletion of the entry by pressing the **Delete** button. The entry will be removed from any site or application that was using the entry.

## Multilingual entries
When a multilingual license key is present in Contensis the process of deleting an entry is similar but its worth taking note of the difference between deleting a default language and a language variation.

### Default language
Where an entry has been translated into multiple languages, deleting an entry in the default language will remove the default language entry and all its language variations.

The process is the same as for deleting a single language.

### Language variations
1. Press the **Content Types & Entries** button in the sidebar. The *Content Types & Entries* drawer will open revealing a number of options.
2. Select **Entries** from the drawer to open the *Entries* listing screen.
3. Locate the *Entry* you want to delete either by scrolling through the listing or by using the [filters](/entries/view-and-filter-entries.md).
3. Press the *Delete* button in the listing, a *Delete confirmation* window will appear.
4. Confirm the deletion of the entry by pressing the **Delete** button. The entry will be removed from any site or application that was using the entry.

> **Note:** You'll notice that the entry is still present in the listing with a translate button. As a language variation is associated with the master language entry, the language variations content is deleted and the API will not return a language variation for the language. The language variation is now ready for translation and returns to the '*Not yet translated*' [workflow state](/entries/workflow-states.md).

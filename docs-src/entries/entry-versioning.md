# Entry versioning
All changes to a entry are recorded in version history. It's version number will depend on the workflow state that the entry is in. When an entry is first created its version is 0.1.

> **Note:** in Contensis 9 its not possible to revert a entry to a previous version, however we are saving the changes about a entry to be used in a future release.

## Saving a entry
Each time a change is made to a content type and saved the minor version number is incremented and the changes are recorded in a diff.

> *e.g.* Adding some text within a field of a newly created entry and pressing save would increment the version number from 0.1 to 0.2. 

**No changes made**
When an entry has not changed since its last save then the save button button will be disabled.

## Publishing an entry
When an entry is ready for publishing, pressing the publish button in the entry editor will change the major version number against the entry.

> *e.g.* Having populated all the fields of my newly created entry and saved it. Pressing publish would increment the version number from 0.2 to 1.0 and moves the workflow state of the content type to published. Once published the publish button will become disabled.
# Entry versioning
All changes to a entry are recorded in version history. It's version number will depend on the workflow state that the entry is in. When an entry is first created its version is 0.1.

> **Note:** in Contensis 9 it's not possible to revert a entry to a previous version, however, we are saving the changes for entries so that they will be available for use in a future release.

## Saving a entry
Each time a change is made to an entry and saved, the minor version number is incremented and the changes are recorded in the version history.

> *e.g.* Adding some text to a field of a newly created entry and pressing save would increment the version number from 0.1 to 0.2.

**No changes made**
When an entry has not changed since its last save then the save button will be disabled.

## Publishing an entry
When an entry is ready for publishing, pressing the publish button in the entry editor will change the major version number against the entry.

> *e.g.* Having populated all the fields of my newly created entry and saved it. Pressing publish would increment the version number from 0.2 to 1.0 and moves the workflow state of the entry to published. Once published the publish button will become disabled.

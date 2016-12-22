# Entry versioning
All changes to an *Entry* are recorded in version history. The version number will depend on the workflow state that the *Entry* is in. When an *Entry* is first created its version is 0.1.

> **Note:** in Contensis 9 it's not possible to revert an *Entry* to a previous version. Changes to *Entries* are being saved and will be made accessible in a future release.

## Saving an entry
Each time a change is made to an *Entry* and saved, the minor version number is incremented and the changes are recorded in the version history.

> *e.g.* Adding some text to a field of a newly created *Entry* and pressing **Save** would increment the version number from 0.1 to 0.2.

**No changes made**
When an *Entry* has not changed since its last save, the **Save** button will be disabled.

## Publishing an *Entry*
When an *Entry* is ready for publishing, pressing the **Publish** button in the *Entry* editor will change the major version number.

> *e.g.* Having populated all the fields of my newly created *Entry* and saved it. Pressing **Publish** would increment the version number from 0.2 to 1.0 and change the workflow state of the *Entry* to *Published*. Once published the **Publish** button will be disabled until further changes are made.

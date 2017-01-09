# Versioning
All changes to a content type are recorded in version history. The version number will depend on the workflow state that the content type is in. When a content type is first created its version number will be 0.1.

> **Note:** in Contensis 9 it is not yet possible to revert a content type to a previous version. Content type changes are being saved and will be made accessible in a future release.

## Saving a content type
Each time a change is made to a content type and saved the minor version number is incremented and the changes are recorded in a version history.

> *e.g.* Adding a field to a newly created content type and pressing **Save** would increment the version number from 0.1 to 0.2.

## Publishing a content type
When a content type is ready for publishing, pressing the **Publish** button in the *Content Type Builder* will change the major version number.

> *e.g.* Having added all my fields to a newly created content type and saved it. Pressing **Publish** increments the version number from 0.2 to 1.0 and changes the workflow state of the content type to *Publish*.

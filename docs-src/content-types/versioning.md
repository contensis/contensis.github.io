# Versioning
All changes to a content type are recorded in version history. It's version number will depend on the workflow state that the content type is in. When a content type is first created its version is 0.1.

> **Note:** in Contensis 9 its not possible to revert a content type to a previous version, however we are saving the changes about a content type to be used in a future release.

## Saving a content type
Each time a change is made to a content type and saved the minor version number is incremented and the changes are recorded in a diff.

> *e.g.* Adding a field to a newly created content type and pressing save would increment the version number from 0.1 to 0.2.

### No changes made
When a content type has not changed since its last save, any subsequent presses of the save button will no affect the version number.

## Publishing a content type
When a content type is ready for publishing, pressing the publish button in the content type builder will change the major  version number against the content type.

> *e.g.* Having added all my fields to my newly created content type and saved it. Pressing publish increments the version number from 0.2 to 1.0 and moves the workflow state of the content type to publish.

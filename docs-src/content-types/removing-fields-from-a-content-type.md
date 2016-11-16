# Removing fields from a content type
The effect on removing a field from a content type will vary depending on the content types published state and wether any entries have been created.

With a content type open for editing simply press the cross button on the field to remove it from the content type.

> **Published content type with entries**
	When removing a field from a content type, its worth bearing in mind that the field may be in use by an entry.[^1]

## Footnotes:

[^1]:
**Scenario:** Remove a field from content type
- **Given** I have a content type
- **and** the content type has entries
- **When** I remove a field
- **Then** what happens to the data associated with the field?
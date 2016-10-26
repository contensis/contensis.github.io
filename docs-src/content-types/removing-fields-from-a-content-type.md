# Removing fields from a content type
The effect on removing a field from a content type will vary depending on the content types published state and wether any entries have been created.

To remove a field from a content type: 








## Footnotes:

**Scenario:** Remove a field from content type
- **Given** I have a content type
- **and** the content type has entries
- **When** I remove a field
- **Then** what happens to the data associated with the field?

**Scenario:** Re add field with the same name
- **Given** I have a content type
- **and** the content type has entries
- **When** I re add a field that previously existed
- **Then** what happens to the historical data associated with the field?



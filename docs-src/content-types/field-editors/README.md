# Supported fields and editors
A field may support different types of field editor, e.g *Text* or *Multiline text*. The selected option will then determine what options are available to authors.

## Field types that support multiple field editors
Each of the following field types have support for different data formats. In some instances a data format may have multiple field editors available, if there are various ways to capture the data.

> *e.g.* Date / Time field has a field editor that simply captures the date or one that will capture date and time.

### Text
| Format   | Field Editor              |
| -------- | ------------------- |
| Text     | [Text](/content-types/field-editors/editor-text.md)         |
| Text     | [Multiline Text](/content-types/field-editors/editor-multiline-text.md)      |
| Heading  | [Heading](/content-types/field-editors/editor-heading.md)             |

### Markup
| Format   | Field Editor              |
| -------- | ------------------- |
| HTML     | [HTML](/content-types/field-editors/editor-html.md)                |
| Markdown | [Markdown](/content-types/field-editors/editor-markdown.md)            |

### Number
| Format   | Field Editor              |
| -------- | ------------------- |
| Integer  | [Integer](/content-types/field-editors/editor-number.md)             |
| Decimal  | [Decimal](/content-types/field-editors/editor-number.md)             |

### List
| Field Editor              |
| ------------------- |
| [List](/content-types/field-editors/editor-list.md)                |
| [Searchable Dropdown](/content-types/field-editors/editor-searchable-dropdown.md) |

### Date
| Format   | Field Editor              |
| -------- | ------------------- |
| Single   | [Date](/content-types/field-editors/editor-date-datetime.md)                |
| Single   | [Date / Time](/content-types/field-editors/editor-date-datetime.md)         |
| Range    | [Date Range](/content-types/field-editors/editor-date-datetime.md)          |
| Range    | [Date / Time Range](/content-types/field-editors/editor-date-datetime.md)   |

## Field types that support single field editors
Each of the following field types have support for a single field editor.

| Field Type      | Field Editor              |
| --------------- | ------------------- |
| Boolean         | [Boolean](/content-types/field-editors/editor-boolean.md)    |
| Location        | [Location](/content-types/field-editors/editor-location.md)  |
| Taxonomy        | [Taxonomy Tree](/content-types/field-editors/editor-taxonomy.md)  |
| Composer        | [Composer](/content-types/field-editors/editor-composer.md)  |
| Quote           | [Quote](/content-types/field-editors/editor-quote.md)        |
| Asset           | [Asset Gallery](/content-types/field-editors/editor-asset.md)|
| Image           | [Image Gallery](/content-types/field-editors/editor-image.md)|
| Entry           | [Entry](/content-types/field-editors/editor-entry.md)    |

## Changing a field editor
With a content type open for editing:

1. Select the field you want to set a validation rule for and pick the **Editor** tab from the *Field Settings* panel. 
2. You will now be in the *Field Editor* panel. If there is more than one field editor available, choose one from the dropdown. e.g *Multiline Text*.
3. You can now set any additional properties that the field editor supports e.g *Content Guidelines* in the boxes below the 'Choose field editor' dropdown.
4. Press *Save* and *Publish* for the additional field editors to be made available for the entries in your project.

> Note: If you have a content type where entries already exist, there maybe potential data loss when changing field editors.

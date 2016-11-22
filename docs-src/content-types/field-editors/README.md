# Supported fields and editors
A field may support multiple editors, it depends on the format selected on the field to what editors are available. The tables below outline the supported editors.

## Field types that support multiple editors
Each of the following field types have support for different editors depending on the format selected. In some instances, some formats have multiple editors if there are various ways to capture the data.

> *e.g.* Date / Time field has an editor that simply captures the date or one that will capture date and time.

### Text
| Format   | Editor              |
| -------- | ------------------- |
| Text     | [Text](/content-types/field-editors/editor-text.md)         |
| Text     | [Multiline Text](/content-types/field-editors/editor-multiline-text.md)      |
| Heading  | [Heading](/content-types/field-editors/editor-heading.md)             |

### Markup
| Format   | Editor              |
| -------- | ------------------- |
| HTML     | [HTML](/content-types/field-editors/editor-html.md)                |
| Markdown | [Markdown](/content-types/field-editors/editor-markdown.md)            |

### Number
| Format   | Editor              |
| -------- | ------------------- |
| Integer  | [Integer](/content-types/field-editors/editor-number.md)             |
| Decimal  | [Decimal](/content-types/field-editors/editor-number.md)             |

### List
| Editor              |
| ------------------- |
| [List](/content-types/field-editors/editor-list.md)                |
| [Searchable Dropdown](/content-types/field-editors/editor-searchable-dropdown.md) |

### Date
| Format   | Editor              |
| -------- | ------------------- |
| Single   | [Date](/content-types/field-editors/editor-date-datetime.md)                |
| Single   | [Date / Time](/content-types/field-editors/editor-date-datetime.md)         |
| Range    | [Date Range](/content-types/field-editors/editor-date-datetime.md)          |
| Range    | [Date / Time Range](/content-types/field-editors/editor-date-datetime.md)   |

## Field types that support single editors
Each of the following field types have support for a single editor.

| Field Type      | Editor              |
| --------------- | ------------------- |
| Boolean         | [Boolean](/content-types/field-editors/editor-boolean.md)    |
| Location        | [Location](/content-types/field-editors/editor-location.md)  |
| Taxonomy        | [Taxonomy](/content-types/field-editors/editor-taxonomy.md)  |
| Composer        | [Composer](/content-types/field-editors/editor-composer.md)  |
| Quote           | [Quote](/content-types/field-editors/editor-quote.md)        |
| Asset           | [Asset Gallery](/content-types/field-editors/editor-asset.md)|
| Image           | [Image Gallery](/content-types/field-editors/editor-image.md)|
| Entry           | [Entry](/content-types/field-editors/editor-entry.md)    |

## Changing an editor

1. With a content type open for editing
2. Select the field that you want to change the editor for e.g. a text field. The properties panel will be displayed.
3. From the properties panel, select *Editor* from the panel navigation. If supported the *Choose a field editor* dropdown will be enabled.
4. Choose an editor from the dropdown. e.g Multiline text
5. Any additional properties that the editor supports will be displayed in the panel.
6. Save any changes you make.

> Note: In the event you have a content type where entries exist, there be potential data loss when changing editors.

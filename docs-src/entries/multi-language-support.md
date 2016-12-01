# Multi language support
When a multilingual license key is present in Contensis then entries can be created in multiple languages.

The languages that are available for an entry to be created against, is determined by those assigned to a [project](/projects/update-a-project.md) and [enabled](/content-types/enable-disable-languages.md) for a content type.

> **Note**: The default language is set against a project and cannot be changed once created.

## Language workflow
- An entry is a container for the default language and all its language variations.
- When an entry is created, its created in the default language, once published, additional language variations can be created.
- When creating a language variation you'll be provided a split view, with the default language displayed to translate from.
- Deleting an entry in the default language will remove the entry completely along with all language variations.
- Deleting a language variation of an entry has no effect on the default language. 
- A language variation can be recreated once deleted.

## Disabling a language
Given I have a content type with multiple language enabled
and I have entries in the default language
and I have entries translated into additional languages
When I disable a language
Then what happens to the existing entries?

1. Prompt on disable to delete entries
2. Are entries kept?
3. What happens if I enable the language again?


## Content 
- New content types get all languages by default 
- additional languages have to be enabled


## Supported languages
We support the following languages in Contensis.

| Languages | Region code  |
|:--|:--|
| Arabic | ar |
| Chinese | zh |
| Danish | da |
| Dutch | nl |
| English | en-GB  |
| American English | en-US |
| Canadian English | en-CA |
| Indian English | en-IN |
| French | fr |
| Dutch French | fr-NL|
| Irish Gaelic | ga-IE |
| Scottish Gaelic | gd-GB |
| German | de |
| Korean | ko |
| Portuguese | pt |
| Spanish | es |
| American Spanish | es-US |
| Mexican Spanish | es-MX |
| Welsh | cy |

**As a** content strategist **I want** my default language content published before language variations can be created **so that** the variations are kept in sync with the default content.

- **Given** I create an entry
- **and** the entry is saved
- **and** not published
- **When** I navigate to an alternative language in the entry listing screen
- **Then** the newly created entry should not be visible for translation

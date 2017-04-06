# Contensis HTTP Management API


## Introduction

## Key concepts

### Projects

|||
|-|-|
| [Get a project](/key-concepts/projects.md#get-a-project) | <span class="label label--get">GET</span> /api/management/projects/**{projectId}**/ |
| [Create a project](/key-concepts/projects.md#create-a-project) | <span class="label label--post">POST</span> /api/management/projects/ |
| [Update a project](/key-concepts/projects.md#update-a-project) | <span class="label label--post">PUT</span> /api/management/projects/**{projectId}**/ |
| [List projects](/key-concepts/projects.md#list-projects) | <span class="label label--get">GET</span> /api/management/projects/ |
| [Delete a project](/key-concepts/projects.md#delete-a-project) | <span class="label label--delete">DELETE</span> /api/management/projects/**{projectId}**/ |


### Content Types

|||
|-|-|
| [Get a content type](/key-concepts/content-types.md#get-a-content-type) | <span class="label label--get">GET</span> /api/management/projects/**{projectId}**/contenttypes/**{contentTypeId}** |
| [Create a content type](/key-concepts/content-types.md#create-a-content-type) | <span class="label label--post">POST</span> /api/management/projects/**{projectId}**/contenttypes/ |
| [Update a content type](/key-concepts/content-types.md#update-a-content-type) | <span class="label label--put">PUT</span> /api/management/projects/**{projectId}**/contenttypes/**{contentTypeId}** |
| [Publish a content type](/key-concepts/content-types.md#publish-a-content-type) | <span class="label label--post">POST</span> /api/management/projects/**{projectId}**/contenttypes/**{contentTypeId}**/workflow/ |
| [List content types](/key-concepts/content-types.md#list-content-types) | <span class="label label--get">GET</span> /api/management/projects/**{projectId}**/contenttypes/ |
| [Delete a content type](/key-concepts/content-types.md#delete-a-content-type) | <span class="label label--delete">DELETE</span> /api/management/projects/**{projectId}**/contenttypes/**{contentTypeId}**/ |

### Entries

|||
|-|-|
| [Get an entry](/key-concepts/projects.md#get-a-entry) | <span class="label label--get">GET</span> /api/management/projects/**{projectId}**/entries/**{entryId}** |
| [Create an entry](/key-concepts/entries.md#create-an-entry) | <span class="label label--post">POST</span> /api/management/projects/**{projectId}**/entries/ |
| [Update an entry](/key-concepts/projects.md#update-an-entry) | <span class="label label--put">PUT</span> /api/management/projects/**{projectId}**/entries/**{entryId}**
| [Publish an entry](/key-concepts/projects.md#publish-an-entry) | <span class="label label--post">POST</span> /api/management/projects/**{projectId}**/entries/**{entryId}**/workflow/
| [List entries](/key-concepts/projects.md#list-entries) | <span class="label label--get">GET</span> /api/management/projects/**{projectId}**/entries/ |
| [List entries by content type](/key-concepts/projects.md#list-entries) | <span class="label label--get">GET</span> /api/management/projects/**{projectId}**/contenttypes/**{contentTypeId}**/entries/ |
| [Delete an entry](/key-concepts/projects.md#delete-an-entry) | <span class="label label--delete">DELETE</span> /api/management/projects/**{projectId}**/entries/**{entryId}**


### Workflow

|||
|-|-|
| [Publish a resource](/key-concepts/content-types.md#publish-a-content-type) | |
| [Publish an entry](/key-concepts/content-types.md#publish-a-content-type) | |
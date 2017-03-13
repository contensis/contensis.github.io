# Paged list

A paged list is a structure that is used to describe paging details for listing and search results.

## Properties
| Name | Type | Format | Description |
| :------- | :--- | :----- | :---------- |
| pageIndex | number | int | The index of the result set to return |
| pageSize | number | int | The size of the result set to return |
| totalCount | number | int | The total number of results available |
| items | object [...] |  | A container for the items being returned |

## Example
The paged list properties provide the information required to implement paging.

@TODO: Example based on dotnet example

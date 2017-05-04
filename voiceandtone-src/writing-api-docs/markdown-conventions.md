# Markdown conventions
We use standard flavoured Markdown in our documentation.

## Bold
```
This is a paragraph and **this** is bold.
```
This is a paragraph and **this** is bold.

## Italic
```
This is a paragraph and *these terms are in italic*.
```
This is a paragraph and *these terms are in italic*.

## Links
```
[Link text](http://www.bbc.co.uk)
```
[Link text](http://www.bbc.co.uk)

## Tables
Tables in markdown can be tedious. An online generator like [Tables Generator](http://www.tablesgenerator.com/markdown_tables) or [Truben tables](http://truben.no/table/) can be helpful to generate them for you.

```
| First header | Second header |
|:--|:--|
| Row one, item one | Row one, item two |
| Row two, item one | Row two, item two |
```

| First header | Second header |
|:--|:--|
| Row one, item one | Row one, item two |
| Row two, item one | Row two, item two |

### Column alignment
If you feel the column contents should be aligned to a particular edge or centre, you can use the GitHub flavoured approach of using a colon `:` in the row separator.

```
| First header | Second header | Third header |
|:--|:--:|--:|
| Row one, item one | Row one, item two | Row one, item three |
| Row two, item one | Row two, item two | Row two, item three |
```

| First header | Second header | Third header |
|:--|:--:|--:|
| Row one, item one | Row one, item two | Row one, item three |
| Row two, item one | Row two, item two | Row two, item three |

## Headings
Headings use the hash `#` notation followed by a space. While some markdown editors allow you to not use the space, it provides a way to clearly parse the data later.

```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
```

# Heading 1
## Heading 2
### Heading 3
#### Heading 4

## Unordered lists
We use hyphenated unordered lists. Use `-` followed by a space. We do not use the `*` notation, because it can get confusing with it being used by **Bold** or *italics*.

```
- List item one
- List item two
- List item three
- List item four
```

- List item one
- List item two
- List item three
- List item four

## Ordered lists
Ordered lists use the number notation `1.` followed by a space.

```
1. List item one
2. List item two
3. List item three
4. List item four
```

1. List item one
2. List item two
3. List item three
4. List item four

### Sub items
```
1. List item one
2. List item two
  - sub item one
  - sub item two
3. List item three
4. List item four
```

1. List item one
2. List item two
  - sub item one
  - sub item two
3. List item three
4. List item four

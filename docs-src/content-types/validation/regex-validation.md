# Matches pattern
The *Matches pattern* validation method ensures that the value of a field matches a specific pattern defined by a regular expression.

A regular expression is a special text string for describing a search pattern. We use these expressions to validate the text that an author enters into a field of an entry.

## Appearance
![Matches pattern validation](/images/validation-matchespattern.png)

## How to set the validation
With a content type open for editing:

1. Select the field you want to set a validation rule for and pick the **Validation** tab from the *Field Settings* panel.
2. Choose the required regular expression pattern you want to use from the *Matches pattern* dropdown, or define your own using the *Custom* option.
3. An alternative validation message can be added by entering it in the *Validation message* text box. This will be displayed if the field fails validation when published.

## Setting a custom expression
You can use the *Custom* option in the matches pattern dropdown to create your own. Using a handy library and expression checker like [Regular Expression 101](https://regex101.com/) to test your expression, makes things easier.

> **Note:** Expressions need to be written using the full JavaScript syntax to be valid.

### Predefined regular expressions
We've included some predefined expressions covering some standard scenarios.

#### Website address

| Allowed values | Disallowed values |
| --- | --- |
| http://www.zengenti.com | special%character@zengenti.com |
| https://zenhub.zengenti.com | name@zengenti |
| http://zengenti.com/en-gb/products/contensis/contensis.aspx | notawebsite.com |

#### Email address

| Allowed values | Disallowed values |
| --- | --- |
| niceandsimple@example.com | Abc.example.com |
| very.common@example.com | A@b@c@example.com |
| a.little.lengthy.but.fine@dept.example.com | john..doe@example.com |

#### UK postcodes

| Allowed values | Disallowed values |
| --- | --- |
| SY8 3EG | SY8_3EG |
| sy83eg | sy8-3eg |
| SY83EG | sy8 £eg |

#### 12 hour time

| Allowed values | Disallowed values |
| --- | --- |
| 10:20 am | 12:15 |
| 10.42.01 AM| 101603|
| 09 26 03 PM | 12am |
| 7:35 PM | 10:67 |

#### 24 hour time

| Allowed values | Disallowed values |
| --- | --- |
| 10:20 | 1215 |
| 10.42.01| 101603|
| 09 26 03 | 12 am |
| 07:57 | 10:67 |

#### Title casing

| Allowed values | Disallowed values |
| --- | --- |
| This Is A Title | This is a title |
| This Is Another Tile | This is A title|

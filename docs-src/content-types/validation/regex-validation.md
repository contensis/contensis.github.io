# Regular expression pattern matching
This validation method ensures that the value of a field matches a specific pattern defined by a regular expression.

A regular expression is a special text string for describing a search pattern. We use these expressions to validate the text that an author enters into a field of an entry.

## Appearance
![Matches pattern validation](/images/validation-matchespattern.png)

## How to set the validation
With a content type open for editing:

1. Select the field you want to set a validation rule for and select the **Validation** tab from the *Field Settings* panel.
2. Choose the required pattern you want to use from the *Matches pattern* dropdown, or define your own using the *Custom* option.
3. You can also provide an alternative validation message to be displayed when the field fails validation on publish, by entering it in the *Validation message* text box.

## Setting a custom expression
You can use the custom option in the matches pattern dropdown to create your own. Using a handy library and expression checker like [Regular Expression 101](https://regex101.com/) to test your expression, makes things easier.

> **Note:** Expressions need to be written using the JavaScript syntax to be valid.

### Predefined regular expressions
We've included some predefined expressions covering some standard scenarios.

#### Website address

	/https?:\/\/(www\.)?[-a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,4}\b([-a-zA-Z0-9@:%_\+.~#?&\/\/=]*)/g

| Allowed values | Disallowed values |
| --- | --- |
| http://www.zengenti.com | special%character@example.com |
| https://zenhub.zengenti.com | name@example |
| http://zengenti.com/en-gb/products/contensis/contensis.aspx | notawebsite.com |

#### Email address

	^(?:(?:[\w`~!#$%^&*\-=+;:{}'|,?\/]+(?:(?:\.(?:"(?:\\?[\w`~!#$%^&*\-=+;:{}'|,?\/\.()<>\[\] @]|\\"|\\\\)*"|[\w`~!#$%^&*\-=+;:{}'|,?\/]+))*\.[\w`~!#$%^&*\-=+;:{}'|,?\/]+)?)|(?:"(?:\\?[\w`~!#$%^&*\-=+;:{}'|,?\/\.()<>\[\] @]|\\"|\\\\)+"))@(?:[a-zA-Z\d\-]+(?:\.[a-zA-Z\d\-]+)*|\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\])$


| Allowed values | Disallowed values |
| --- | --- |
| niceandsimple@example.com | Abc.example.com |
| very.common@example.com | A@b@c@example.com |
| a.little.lengthy.but.fine@dept.example.com | john..doe@example.com |

#### UK postcodes

	^([a-z]{1,2}[a-z0-9]{1,2})\s*?(\d[a-z]{2})$

| Allowed values | Disallowed values |
| --- | --- |
| SY8 3EG | SY8_3EG |
| sy83eg | sy8-3eg |
| SY83EG | sy8 £eg |

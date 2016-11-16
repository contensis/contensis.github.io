# Regular expression pattern matching
This validation method ensures that the value of a field matches a specific pattern defined by a regular expression.

A regular expression is a special text string for describing a search pattern. We use these expressions to validate the text that an author enters in a field of an entry.

## How to set the validation
With a content type open for editing:

- Select the field you want to set a validation rule against.
- With the field active the properties panel is displayed, select **Validation** from the panel navigation.
- Select from the matches pattern dropdown the required pattern you want to use, alternative you can define your own using the custom option.
- You can also provide an alternative validation message to be displayed when the field fails validation on save, by entering it in the *Validation message* text box.

## Setting a custom expression
You can use the custom option in the validation dropdown to create your own. Using a handy library and expression checker like [Regular Expression 101](https://regex101.com/) to test your expression, makes things easier.

> **Note:** Expressions need to be written in the Javascript syntax to be valid.

### Predefined regular expressions
We've included some predefined expressions covering some standard scenarios.

#### Website address

	/https?:\/\/(www\.)?[-a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,4}\b([-a-zA-Z0-9@:%_\+.~#?&\/\/=]*)/g

| Allowed Values | Disallowed Values |
| --- | --- |
| http://www.zengenti.com | special%character@example.com |
| https://zenhub.zengenti.com | name@example |
| http://zengenti.com/en-gb/products/contensis/contensis.aspx | notawebsite.com |

#### Email address

	^(?:(?:[\w`~!#$%^&*\-=+;:{}'|,?\/]+(?:(?:\.(?:"(?:\\?[\w`~!#$%^&*\-=+;:{}'|,?\/\.()<>\[\] @]|\\"|\\\\)*"|[\w`~!#$%^&*\-=+;:{}'|,?\/]+))*\.[\w`~!#$%^&*\-=+;:{}'|,?\/]+)?)|(?:"(?:\\?[\w`~!#$%^&*\-=+;:{}'|,?\/\.()<>\[\] @]|\\"|\\\\)+"))@(?:[a-zA-Z\d\-]+(?:\.[a-zA-Z\d\-]+)*|\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\])$


| Allowed Values | Disallowed Values |
| --- | --- |
| niceandsimple@example.com | Abc.example.com |
| very.common@example.com | A@b@c@example.com |
| a.little.lengthy.but.fine@dept.example.com | john..doe@example.com |

#### UK Postcodes

	^([a-z]{1,2}[a-z0-9]{1,2})\s*?(\d[a-z]{2})$

| Allowed Values | Disallowed Values |
| --- | --- |
| SY8 3EG | SY8_3EG |
| sy83eg | sy8-3eg |
| SY83EG | sy8 £eg |

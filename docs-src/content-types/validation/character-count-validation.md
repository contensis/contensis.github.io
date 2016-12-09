# Character count
Validates that the value of a text field is within a specified range. You can define a range by specifying the 'min' and the 'max' values (the values are included in the range). Alternatively, you can specify an individual 'min' or 'max' value to set a constraint on the minimum or maximum allowed value.

## Appearance
![Matches pattern validation](/images/validation-numberofcharacters.png)

## How to set the validation
With a content type open for editing:

- Select the field you want to set a validation rule against.
- With the field active, the properties panel will be displayed, select **Validation** from the panel navigation.
- Locate the Number of Characters validation and choose one of the following options from the dropdown:

**Between** provides the ability to set an expected character range. Set the minimum and maximum values.

> *e.g.* Requires between 200 - 300 characters

**Minimum of** allows you to set an expected minimum value that needs to be met.

> *e.g.* Requires a minimum of 200 characters

**Maximum of** allows you to set the maximum number of characters that can be entered.

> *e.g.* Requires a maximum of 200 characters

- You can also provide an alternative validation message to be displayed when the field fails validation on publish, by entering it in the *Validation message* text box.

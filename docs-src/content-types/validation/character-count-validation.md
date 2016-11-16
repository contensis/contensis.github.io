# Character count
Validates that the value of a text field is within a specified range. You can define a range by specifying the 'min' and the 'max' value (the values are included in the range). You can specify only 'min' or max values to set a constraint on the minimum and maximum allowed value.

## How to set the validation
With a content type open for editing:

- Select the field you want to set a validation rule against.
- With the field active the properties panel is displayed, select **Validation** from the panel navigation.
- Locate the Number of Characters validation and choose one of the following options from the dropdown.

**Between** provides the ability to set an expected character range. Set the minimum and maximum values.

> *e.g.* Requires between 200 - 300 characters

**Minimum of** allows you to set an expected value that needs to be met.

> *e.g.* Requires a minimum of 200 characters

**Maximum of** allows you to set the maximum number of characters that can be entered.

> *e.g.* Requires a maximum of 200 characters

- You can also provide an alternative validation message to be displayed when the field fails validation on save, by entering it in the *Error message* text box.

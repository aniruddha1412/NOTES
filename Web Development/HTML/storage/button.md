## Syntax:
```html
<form >
	<button>Submit</button>
</form>
```

## Attributes:
- **`type`** : specifies the behavior of the button. It can have one of the following values:
	- `submit` : When the button is clicked, it submits the form. (This is the default type of a button which is placed inside a `<form>` element)
	- `reset` : Resets all form fields to their default values when clicked.
	- `button` : A general button. Can be used for custom actions such as executing JavaScript functions. (This is the default type of a button which is placed outside a `<form>` element)
- **`value`** and **`name`**
- **`formaction`** : specifies the URL where the form data is submitted when the button is clicked. This is used to override the `action` attribute of the `<form>` for a particular button.
- **`formmethod`** : specifies the HTTP method to use when submitting the form with the button.
	- If not specified, the button uses the method set by the form's `method` attribute.
- **`formtarget`** : specifies where to display the response after form submission. It can take values like:
	- `_self`
	- `_blank`
	- `_parent`
	- `_top`
- **`formnovalidate`** : clicking the button will bypass form validation and submit the form even if there are invalid fields.
- **`onclick`** : defines a JavaScript function to be executed when the button is clicked.


## Syntax:
```html
<input type="text" name="username" value="default text" placeholder="Enter Username">
```

This type of input allows users to enter text data.

## Attributes:
- **`value`** : specifies the initial value of the text input field. This value will be pre-filled in the input field when the page loads.
	- When the form is submitted, the current **value** of the text input is sent to the server.
- **`name`** : The name of the input field. Used to refer to the data in the form when it is submitted to the server. Acts as the key for the submitted **value**.
- **`placeholder`** : Displays a short hint or description in the input field when it is empty.
- **`required`** : Specifies that the input field is compulsory to be filled for submitting the form, otherwise it won't allow to submit. It is a [[boolean attribute]].
- **`maxlength`** : Sets the maximum number of characters that can be entered into the text input.
- **`minlength`** : Sets the minimum number of characters that must be entered into the text input.
- **`pattern`** : Specifies a regular expressions that the input must match.
	```html
	<input type="text" pattern="[A-Za-z]{3,}">
	```
	
- **`readonly`** : Makes the input field non-editable while still allowing the value to be selected and copied.
- **`disabled`** : Disables the input field, making it non-selectable and non-editable. It is a [[boolean attribute]].
- **`autofocus`** : Automatically focuses on the input field when the page loads. It is a [[boolean attribute]].
- **`size`** : Specifies the visible width of the input field, in characters.
- **`autocomplete`** : Specifies whether the browser should automatically fill in the field or suggest values based on previously entered data.
	- Values:
		- `on`
		- `off`
- **`form`** : Specifies the form id of the form the input belongs to, when the `<input>` is placed outside a `<form>` element.
	```html
	<form id="myForm">
	</form>
	<input type="text" form="myForm">
	```

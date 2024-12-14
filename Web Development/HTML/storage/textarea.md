Used to create a multi-line text input field that allows user to enter longer text such as a description.

The use of the `value` attribute is discouraged with `<textarea>` element. When a form is submitted, the content within the `<textarea>` tags is sent as the value for that form field.
## Syntax:
```html
<textarea>Default text here</textarea>
```

## Attributes:
- **`rows`** : specifies the height of the textarea in terms of the number of text lines.
- **`cols`** : specifies the width of the textarea in terms of the number of characters.
- **`wrap`** : specifies how text in the textarea should be wrapped when submitted.
	- Values:
		- `soft` (default) : Text is wrapped in the UI but submitted as a single line of text (no line breaks are sent).
		- `hard` : Line breaks are included in the form submission.
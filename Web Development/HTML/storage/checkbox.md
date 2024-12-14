Checkboxes allows users to make binary choices: checked or unchecked.

## Syntax
```html
<input type='checkbox'>
```

## Attributes:
Following are the important attributes of `type='checkbox'`:
- **`checked`** : specifies whether the checkbox should be checked by default when the page loads.
- **`indeterminate`** (JavaScript Property) : represents a state where the checkbox is neither checked nor unchecked, usually used for a "partial" state in UI.
	```js
	const checkbox = document.querySelector("#partial");
	checkbox.indeterminate = true;
	```
	- The indeterminate state is visual only. It does not affect the `checked` or `value` state of the checkbox.
- **`value`** : defines the value submitted with the form when the checkbox is checked.
	- If the checkbox is checked, its `value` will be sent to the server.
	- If it is unchecked, no data is sent for that checkbox, as unchecked checkboxes are not submitted in form data.
```html
<input type="checkbox" value="yes">
```


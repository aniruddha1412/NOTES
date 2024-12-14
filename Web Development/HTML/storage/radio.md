Radio buttons allow the user to select only one option from a group of choices.

## Syntax:
```html
<input type='radio'>
```

## Attributes:
- **`checked`** : specifies that the radio button is selected by default when the page loads.
- **`name`** : This attributes groups radio buttons together. Radio buttons with the same `name` attribute are part of the same group, meaning only one button in that group can be selected at a time.
	```html
	<input type="radio" name="gender" value="male"> Male
	<input type="radio" name="gender" value="female"> Female
	```
- **`value`** : specifies the value sent to the server when the form is submitted, if the radio button is selected.
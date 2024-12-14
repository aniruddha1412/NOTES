Creates a date picker interface that allows user to select a date using a calendar widget or manually input a date in a valid format.

## Syntax:
```html
<input type='date'>
```

## Attributes:
Following attributes are unique to `type='date'`:
- **`min`** : specifies the earliest date that the input can accept.
	- The value should be a valid date string in the format `YYYY-MM-DD`.
	- `<input type='date' min='2001-06-31'`
- **`max`** : specifies the latest date that the input can accept.
- **`value`** : sets the default date for the input field.
	- If the value doesn't match the format or falls outside `min`/`max` limits, it is ignored.
- **`step`** : specifies the step interval for valid dates in days. The default value is 1 day.
	```html
	<input type='date' step='7'>
	```
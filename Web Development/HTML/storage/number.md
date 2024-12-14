## Syntax
```html
<input type='number'>
```

## Attributes:
Following attributes are unique to `type='number'`:
- **`min`** : specifies the minimum value that the field can accept.
- **`max`** : specifies the maximum value that the field can accept.
- **`step`** : specifies the increment for the numeric field.
	- Default value is `1`.
	- If the entered number is not a multiple of the step, it's considered invalid.
- **`valueAsNumber`** (JavaScript Property) : provides the numeric value of the input as a `number` type. The `value` property always returns a `string`, not a `number`, therefore this property is useful.
	```js
	const input = document.querySelector('input[type="number"]');
	console.log(input.valueAsNumber); // Returns the number
	```
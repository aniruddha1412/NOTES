Used to create a dropdown list, allowing users to choose from a list of options.

## Syntax:
```html
<select name="gender">
  <option value="male">Male</option>
  <option value="female">Female</option>
</select>
```

## Attributes:
- **`name`** : essential for identifying the `<select>` element when the form data is submitted. It represents the key in the form data that corresponds the the selected option's value.
- **`multiple`** : allows the user to select more than one option from the list.
	- When `multiple` is used, the dropdown becomes a list box where multiple selections can be made using the `Ctrl` key.
	- The multiple selected values are sent as an array when submitting.
- **`size`** : Specifies the number of visible options in the dropdown without scrolling.

### `<optgroup>` Element
It is used to group related `<option>` elements inside a `<select>` dropdown list.
```html
<select name="country">
  <optgroup label="Europe">
    <option value="france">France</option>
    <option value="germany">Germany</option>
  </optgroup>
  <optgroup label="Asia">
    <option value="india">India</option>
    <option value="china">China</option>
  </optgroup>
</select>
```

>[!Success] Rendered Output:
>![[Pasted image 20241209150756.png]]


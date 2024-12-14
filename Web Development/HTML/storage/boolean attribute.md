Boolean attributes are considered "true" when present in an element and "false" when absent.

Boolean attributes do not care what their value is.

#### Example:
```html
<input type="text" hidden="false">
<!-- This will still hide the element because it is basically same as writing: -->
<input type="text" hidden>
```
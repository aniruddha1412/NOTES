Form Serialization converts the state of the input fields of a form, into a string, which typically follows a "key=value" pattern, separated by an ampersand (`&`).

## Need for Form Serialization
- Browsers automatically handle `application/x-www-form-urlencoded` when submitting forms natively. However, if you're sending data with JavaScript (e.g., using `fetch` or `XMLHttpRequest`), you'll need to manually prepare and encode the data.
- If your server API expects data in a format other than `application/x-www-form-urlencoded`, you'll need to serialize the data into the desired format manually.
- Before sending the form data to the server, you might want to:
	- Validate the inputs (e.g., check if fields are not empty).
	- Add additional fields dynamically (e.g., adding a timestamp or user token).

## The `FormData` Object
The `FormData` object is a built-in JavaScript interface that allows developers to easily create and manage key-value pairs representing form fields and their values. It is especially useful when working with forms in modern web applications, particularly for sending form data via AJAX or `fetch` requests.

### Common Methods of `FormData`
- **`append(name, value)`** : adds a key-value pair to the `FormData` object. If a key already exists, the new value is added as a separate entry.
- **`delete(name)`** : deletes all entries with the specified key.
- **`get(name)`** : returns the first value associated with the specified key.
- **`getAll(name)`** : returns all values associated with the specified key as an array.
- **`has(name)`** : checks if the specified key exists in the `FormData` object.
- **`set(name, value)`** : sets a new value for a key. If the key exists, its value is replaced, otherwise, it adds a new key-value pair.
- **`entries()`** : returns an iterator of all key-value pairs in the `FormData` object.
- **`keys()`** : returns an iterator of all the keys in the `FormData` object.
- **`values()`** : returns an iterator of all the values in the `FormData` object.

## Methods of Form Serialization
```html
<form id="myForm">
  <input type="text" name="username" value="john_doe">
  <input type="password" name="password" value="mypassword">
  <input type="checkbox" name="subscribe" checked>
  <button type="submit">Submit</button>
</form>
```
### Manual Serialization
You can manually serialize form data by iterating over all form elements and collecting the `name` and `value` attributes.

```js
function serializeForm(form) {  
    const formData = new FormData(form);  
    let serializedData = [];  
  
    formData.forEach((value, name) => {  
        serializedData.push(`${encodeURIComponent(name)}=${encodeURIComponent(value)}`);  
    });  
  
    return serializedData.join('&');  
}  
  
const form = document.querySelector('#myForm');  
console.log(serializeForm(form));
```

### Serialization to URL-Encoded Format
```js
const form = document.querySelector('#myForm');
const formData = new FormData(form);
const serializedData = new URLSearchParams(formData).toString();

console.log(serializedData);
// Output: "username=JohnDoe&email=john@example.com"
```

### Serialization to JSON
```js
const form = document.querySelector('#myForm');
const formData = new FormData(form);

// Convert FormData to JSON
const jsonData = {};
formData.forEach((value, key) => {
  jsonData[key] = value;
});

console.log(JSON.stringify(jsonData));
// Output: {"username":"JohnDoe","email":"john@example.com"}
```

```html
<form action="" method="get">
    <div>
        <label for="name">Enter your name: </label>
        <input type="text" name="name" id="name" required />
    </div>
    <div>
        <label for="email">Enter your email: </label>
        <input type="email" name="email" id="email" required />
    </div>
    <div>
        <input type="submit" value="Subscribe!" />
    </div>
</form>
```

>[!success] Rendered Output:
> ![[Pasted image 20241208220454.png]] 

## Form Attributes
- **`action`** : specifies the URL where the form data will be sent when the form is submitted.
	- If the `action` attribute is omitted, the data is submitted to the current page (the same URL).
		```html
		<form action="/submit-form" method="POST">
		```

- **`method`** : specifies the HTTP method to use when submitting the form.

- **`target`** : specifies where to display the response after form submission.
	- Values:
		- `_self` : Opens the response in the same frame as the form.
		- `_blank` : Opens the response in a new tab or window.
		- `_parent` : Opens the response in the parent frame (if the form is in a nested frame).
		- `_top` : Opens the response in the full body of the window.
- **`enctype`** : specifies how the form data should be encoded when submitting it to the server, especially useful for file uploads.
	- Values:
		- `application/x-www-form-urlencoded` : Default value, data is encoded as key-value pairs.
		- `multipart/form-data` : Used when the form includes file input fields (`<input type="file">`).
		- `text/plain` : Data is sent as plain text.
- **`novalidate`** : specifies that the form should not be validated when submitted.
	- Usage:
	```html
	<form novalidate action="/submit-form" method="POST">
	```

## Input Types
1. [[text]]
2. [[password]]
3. [[email]]
4. [[number]]
5. [[date]]
6. [[checkbox]]
7. [[radio]]
8. [[file]]
9. [[textarea]]
10. [[select]]
11. [[button]]

## Grouping Related Inputs
### `<fieldset>` And `<legend>` Element

The `<fieldset>` element is a block-level element that creates a box around the grouped elements to group them visually and logically, while the `<legend>` element provides a caption or title for the group.
```html
<form action="/submit" method="POST">  
    <fieldset style="width: 40%">  
        <legend>Personal Information</legend>  
  
        <label for="name">Name:</label>  
        <input type="text" id="name" name="name" required>  
  
        <label for="email">Email:</label>  
        <input type="email" id="email" name="email" required>  
    </fieldset>  
  
    <fieldset style="width: 40%">  
        <legend>Shipping Address</legend>  
  
        <label for="address">Address:</label>  
        <input type="text" id="address" name="address" required>  
  
        <label for="zipcode">Zip Code:</label>  
        <input type="text" id="zipcode" name="zipcode" required>  
    </fieldset>  
  
    <button type="submit">Submit</button>  
</form>
```

>[!success] Rendered Output:
>![[Pasted image 20241209151349.png]]

## Form Serialization
*Reference:* [[Form Serialization]]


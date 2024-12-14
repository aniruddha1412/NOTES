It provides a file picker dialog, which enables users to choose one or more files to be uploaded.

## Syntax:-
```html
<input type='file'>
```

## Attributes:
- **`accept`** : specifies the types of files that the user can select.
	```html
	<input type='file' accept='image/*, .pdg, .docx'>
	```
	- The `accept` attributes accepts file types by MIME type (e.g., `image/png`, `application/pdf`, etc) or file extensions (e.g., `.jpg`, `.png`, etc). 
- **`multiple`** : allows the user to select multiple files for upload instead of just one. It is a boolean attribute.

## Accessing the Files Using JavaScript
```js
// Select the input element
const fileInput = document.getElementById('fileInput');

// Access the files when the user selects them
fileInput.addEventListener('change', () => {
  const files = fileInput.files; // FileList object
  console.log("Selected Files:", files);
});
```
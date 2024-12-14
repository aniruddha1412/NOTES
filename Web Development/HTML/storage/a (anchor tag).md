- The anchor `<a>` tag can be used as an anchor to other sections/elements on the same webpage.
```html
<a href='#section1'> Focus on Section 1 </a>

<p id='section1'>
	// lorem ipsum
</p>

<!-- Clicking the link will shift the focus of the viewport wherever the element with the id `section1` is >
```

- It can also be used to link to external webpages using an absolute address.
```html
<a href='https://google.com'> Google </a>
```

- It can also be used to link to internal webpages of the same website using a relative address.
```html
<a href='../index.html'>Back to Homepage</a>
```

- It can also be used to make a Heading into a link by wrapping the `<h1>` inside the `<a>` tag.
```html
<a href="https://developer.mozilla.org/en-US/">
  <h1>MDN Web Docs</h1>
</a>
```

- It can also be used to make an image into a link by wrapping the `<img>` tag inside the `<a>` tag.
```html
<a href="https://developer.mozilla.org/en-US/">
  <img src="mdn_logo.svg" alt="MDN Web Docs" />
</a>
```

***
### Important Attributes
- `href`
	- `mailto:` URLS
- `target`
	- `_self` : opens the link in the current tab or iframe
	- `_blank` : opens the link in new tab
	- `_parent` : opens the link in the parent page, when using `<iframe>`
- `title` : the title contains additional information about the link which will be displayed when we hover over the link

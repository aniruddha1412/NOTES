- Paragraphs `<p>` are block level elements.
- They will automatically close if another block-level element is parsed before the closing `</p>` tag.
- ![[Pasted image 20241124132229.png]]
- Do not nest `<p>` tags inside each other. HTML specifications do not allow this.
- Avoid placing block-level elements directly inside `<p>` tags, as this is invalid in HTML.

```html
<p> This is a paragraph </p>
<p> This is another paragraph </p>
```


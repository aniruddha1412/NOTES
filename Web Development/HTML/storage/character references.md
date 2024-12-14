An HTML character reference is a formatted pattern of characters that is used to represent another character in the rendered web page.

- These are used as replacements for characters that are reserved in HTML, such as the `<` and `>` symbols used by the HTML parser.

```html
<!-- Suppose you want the literal string "<Hello World>" to render on your webpage,
	but if you write: -->
<p>
	<Hello World>
</p>

<!-- The broswer will think that <Hello World> is a tag, 
and nothing will be rendered because it is not a valid tag. -->
```

### Solution:
```html
<p>
	&lt;HelloWord&gt;
</p>

<!-- Another Example -->
<a href="https://www.example.com" title="An &quot;interesting&quot; reference">A link to my example.</a>

```

***

![[Pasted image 20241125120501.png]]
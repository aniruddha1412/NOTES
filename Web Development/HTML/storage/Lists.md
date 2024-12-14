### **HTML Lists in Detail**

HTML provides three types of lists for organizing content: **unordered lists**, **ordered lists**, and **description lists**.

- `<ol>`, `<ul>`, `<li>`, `<dl>`, `<dt>`, `<dd>` are all block level elements.

### 1. Unordered Lists (`<ul>`)

- **Syntax**:
    ```html
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </ul>
    ```
    
- **Elements**:
    - `<ul>`: The container for the **unordered list**.
    - `<li>`: The **list item**, which is the content inside the unordered list.
    
***
### 2. Ordered Lists (`<ol>`)

- **Syntax**:
    ```html
    <ol>
      <li>First item</li>
      <li>Second item</li>
      <li>Third item</li>
    </ol>
    ```
    
- **Elements**:
    - `<ol>`: The container for the **ordered list**.
    - `<li>`: The **list item**, which is the content inside the ordered list.
- **Common Attributes**:
	- `type`: specifies the type of numbering for the list items
	  Accepted Values:
		- `1` : Decimal Numbers
		- `A` : Uppercase Letters
		- `a` : Lowercase Letters
		- `I` : Uppercase Roman Numerals
		- `i` : Lowercase Roman Numerals
	- `start`: specifies the starting value of the first item
	- `reversed`: reverses the numbering order

---

### 3. Description Lists (`<dl>`)
A description list is used for associating terms with their descriptions. It is commonly used for definitions or explaining terms.

- **Syntax**:
    ```html
    <dl>
      <dt>Term 1</dt>
      <dd>Description for term 1</dd>
      <dt>Term 2</dt>
      <dd>Description for term 2</dd>
    </dl>
    ```

- **Rendered Output:**![[Pasted image 20241208004906.png]]
- **Elements**:
    - `<dl>`: The container for the **description list**.
    - `<dt>`: **Definition Term**
    - `<dd>`: **Definition Description**
Custom attributes are user-defined attributes that allow you to embed additional information in HTML elements. These attributes are not part of the standard HTML specification but can be used to store extra data that can be accessed via JavaScript, CSS, or other scripts.

#### **Types Of Custom Attributes:**
1. **Data Attributes** (Recommended and Standardized)
2. **Non-Standard Custom Attributes** (Deprecated/Discouraged)

---

### 1. **Data Attributes (Preferred Way)**
Data attributes allow you to store custom data directly in an element. They are part of the HTML5 specification and have a specific syntax:

#### **Syntax:**
```html
data-*="value"
```
- **`*`** can be any name you choose.
- **`value`** is the data you want to store.

#### **Example:**
```html
<div id="user" data-user-id="12345" data-role="admin">
  Hello, User!
</div>
```

In this example:
- `data-user-id="12345"` stores a custom user ID.
- `data-role="admin"` stores the user's role.

#### **Accessing Data Attributes with JavaScript:**
You can access the custom data stored in these attributes using JavaScript:

```javascript
const userDiv = document.getElementById('user');

// Accessing data attributes
const userId = userDiv.getAttribute('data-user-id');
const role = userDiv.dataset.role;  // Modern way using 'dataset'

console.log(userId); // Output: 12345
console.log(role);   // Output: admin
```
# General

- Use soft-tabs with a two (or four) space indent. Spaces are the only way to guarantee code renders the same in any person’s environment.
- Paragraphs of text should always be placed in a <code><p></code> tag. 
- Break apart paragraphs using additional <code><p></code> tags (NOT <code><br></code>).
- Items in list form should always be in <code><ul></code>, <code><ol></code>, or <code><dl></code>. Never use a set of <code><div></code> or <code><p></code>.
- Even though quotes around attributes is optional, always put quotes around attributes for readability.
- Use semantic HTML elements to structure the page, don't use <code><div></code> everywhere. 

# Accessibility

- Every form input that has text attached **must** utilize a <code><label></code> tag. *Especially* radio or checkbox elements.
    - *Missing label elements will cause errors on [accessibility testing](http://wave.webaim.org/).*
- Labels can be hidden for design but are necessary for accessibility. Do not rely on placeholder text to label an input.
- Tab index should be set appropriately if page elements change common sense flow. Always try tabbing through your page at least once to see what happens and if you can access all links, menus, form inputs, and buttons.

# Forms

## Inputs & Labels

- Inputs should have *both* <code>id</code> and <code>name</code>
- Input <code>id</code> and <code>name</code> should be the same value for syncing front end to back end
- Form element itself can have both <code>id</code> and <code>name</code>
- Inputs can have multiple <code>label</code> tags
    - Take advantage of this to make additional text more semantic:

<pre><code>
<label for=“password”>Password:</label>  
<input type=“password” id=“password” name="password">  
<label for=“password”>*Your password must be at least 8 characters long.</label>
</code></pre>

- Since so many labels are styled separately from their inputs (or hidden), don't nest the input inside of its label:

<pre><code>
// Yes do this
<label for=“password”>Password:</label>  
<input type=“password” id=“password” name="password">

// Don't do this
<label>Password: 
    <input type=“password” id=“password” name="password">
</label> 
</code></pre>

## Fieldset

- <code>Fieldset</code> is quite useful for grouping form elements in a semantic manner, especially if similar input types are on the same screen
- Include a <legend> with <fieldset>, even if is it hidden from view. Screen readers can use it to help users.

<pre><code>
<fieldset>
    <legend>Login</fieldset>
    <label for=“password”>Password:</label>  
    <input type=“password” id=“password” name="password">
</fieldset>

<fieldset>
    <legend>Sign Up</fieldset>
    <label for=“password”>Password:</label>  
    <input type=“password” id=“password” name="password">
</fieldset>
</code></pre>

References:

* [GitHub HTML](http://primercss.io/guidelines/#html)
* [Labelling Forms](http://bitsofco.de/labelling-form-elements/)

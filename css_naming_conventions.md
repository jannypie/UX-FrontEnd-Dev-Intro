* BEM: Block Element Modifier
* Approach to class *naming*

<pre>
.block
.block__child 
.block--modified
.block__child--modified
</pre>

* Natural progression from defining components/objects
* Elements are the descendants of the Block
* Modifiers are small changes to repeating objects in the design
* Keep semantics in mind when naming objects
* Separate **structure** from **appearance**

<pre><code>
// Example Block-level object
.button {
  // All buttons have these same structural properties
  border: 1px solid gray;
  border-radius: 5px;
  padding: 5px 10px;

  // Default buttons have these same style properties
  background-color: gray;
  font-size: 0.8em;
  line-height: 1.2em;
}

// Example modifiers
.button--success {
  @extend .button;
  background-color: green;
}
.button--error {
   @extend .button;
  background-color: red;
}

// Example child elements
.button__text {
  color: white;
  font-weight: bold;
}
.button__icon {
  font-family: fonticons;
  color: white;
}
</code></pre>

* Define an element's modifiers in CSS, rather than adding both to the markup:

<pre><code>
// Together with the element they modify
.foo, .foo--bar, .foo--baz {
    display: block;
    background-color: green;
    color: red;
}
.foo--bar {
    color: blue;
}

// Using @extend after the element is defined
.foo {
    display: block;
    background-color: green;
    color: red;
}
.foo--bar, .foo--baz {
    @extend .foo;
    color: blue;
}

// This avoids having to fill up your HTML with repetitive classes
<div class="foo foo--bar"></div>
</code></pre>

* Child elements can be nested inside parents if specificity is needed, but aim to write CSS that doesn't make that a necessity. Don't nest just for parent > child relationships. Those should be obvious from the BEM class names.

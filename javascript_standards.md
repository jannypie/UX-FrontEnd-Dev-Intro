## General

- Variables and functions should be defined before they are used
- Variables and Functions should be camel-case starting with a lower-case: <code>myFunctionName, myVariableName</code>
- Only use $ in a name if the variable is a jQuery object to avoid confusion
- Do not use _ in a name to avoid confusion with underscore.js
- Avoid use of the <code>continue</code> statement. It tends to obscure the control flow of the function.

## Documentation / Commenting

> **Be generous with comments.** It is useful to leave information that will be read at a later time by people (possibly yourself) who will need to understand what you have done. The comments should be well-written and clear, just like the code they are annotating. An occasional nugget of humor might be appreciated. Frustrations and resentments will not.
>
> It is important that comments be kept up-to-date. Erroneous comments can make programs even harder to read and understand.
> - [Code Conventions](http://javascript.crockford.com/code.html)

<pre><code>
// Single line comments

/**
 * Block comments
 * @author      Firstname Lastname
 * @desc        Description of function (why, how)
 * @param      variableName: Description of this variable
 * @param      variableName: Description of this variable
 * @returns     Description of type of data expected to return
 */
</code></pre>

# ES6? 

Not until it's fully supported across the department, to avoid confusion for the next dev.

#Syntax

<pre><code>
var outer = function (c, d) {
    var e = c * d;

    function inner(a, b) {
        return (e * a) + b;
    }

    return inner(0, 1);
}
</code></pre>

- In general, end all statements with semi-colons. Don't rely on implicit semi-colons.

<pre><code>
if (something) {
    doSomething  //where my semicolon?
    doSomething;  //oh there it is
}
</code></pre>

- Define multiple variables on single lines: 

<pre><code>
var itemSelector,
      itemCount,
      itemSize;
</code></pre>

- Curly Braces: Because of implicit semicolon insertion, always start your curly braces on the same line as whatever they're opening. For example:

<pre><code>
if (something) { //same line
  // ...
} else { // same line
  // ...
}
</code></pre>



- [AirBnb](https://github.com/airbnb/javascript)
- [Google](https://google.github.io/styleguide/javascriptguide.xml#JavaScript_Style_Rules)

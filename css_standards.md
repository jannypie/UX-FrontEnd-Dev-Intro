- [Syntax](#syntax)
- [Structure](#structure)
- [Box-sizing](#boxsizing)

# General

* Avoid using IDs for styling; use classes instead.
* Classes starting with <code>.js-</code> should never be used in CSS styling. They should be reserved only as JS selectors.
* **Nesting**
    * Sass/SCSS nesting should be minimal and extend maximum 3 levels deep in general. If nesting starts to exceed this, re-evaluate naming conventions and specificity.
    * Nesting is best used for pseudo elements, modifiers and states. See [Beware selector nesting](http://www.sitepoint.com/beware-selector-nesting-sass/)
* !important is the devil
* Reducing bloat and complex selectors improves performance
* Avoid the descendent selector (i.e. don’t use <code>.sidebar h3</code>). Use classes instead.
* Avoid attaching classes to elements in your stylesheet (i.e. don’t do <code>div.header</code> or <code>h1.title</code>)

# <a name="syntax"</a>Syntax

<pre><code>
.foo, .foo--bar,
.baz {
    display: block;
    background-color: green;
    color: red;
}
</code></pre>

* Each selector is comma separated on a new line, unless directly related (i.e. a BEM block and its modifier: .foo, .foo--bar)
* Opening curly brace on same line as last selector
* Closing curly brace on its own line
* Property and value on same line, with space between colon: <pre>display: block;</pre>
* One declaration (property + value) per line
* Always end declarations with semi-colons (unless writing pure Sass)



# <a name="structure"></a>Organization

Example table of contents for organizing files and imports. 

<pre><code>
/**
 *
 * SETTINGS
 * Globally-available variables and config settings
 *
 * TOOLS/HELPERS
 * Useful mixins (if very few, can include with Settings)
 *
 * GENERIC
 * Normalize.css
 * Box-sizing
 * Font-imports (including icon fonts)
 *
 * TYPE
 * Body text
 * Headings.............H1–H6 styles
 * Hyperlinks
 * Lists
 * 
 * LAYOUT
 * Wrapping and constraining elements
 * Grid
 *
 * COMPONENTS
 * Recurring, re-usable sections or blocks
 * Buttons
 * Forms
 * Media elements
 * 
 * PARTIALS
 * Header
 * Footer
 * Nav
 * 
 * PAGES
 * 
 */
</code></pre>

# <a name="boxsizing"></a>Box-sizing

<pre><code>
/* apply a natural box layout model to all elements, but allowing components to change */
html {
  box-sizing: border-box;
}
*, *:before, *:after {
  box-sizing: inherit;
}
</code></pre>

References:

* [GitHub CSS Primer](http://primercss.io/scaffolding/)
* [CSSGuidelin.es](http://cssguidelin.es/)
* [[url:http://www.slideshare.net/jewlofthelotus/decoupling-the-frontend-through-modular-css|Decoupling the Frontend through modular CSS]]
* [OOCSS on Smashing Magazine](http://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/)
* [Paul Irish on box-sizing](http://www.paulirish.com/2012/box-sizing-border-box-ftw/)
* [BEM 101](https://css-tricks.com/bem-101/)

(Not the same as [[url:https://css-tricks.com/modular-future-web-components/|HTML Web Components]])

## Why have a library?

* Approach to DRY, semantic, reusable HTML/CSS
    * Separates *style* from *structure*
    * CSS handles styling regardless of markup, HTML can change somewhat without breaking everything
    * Drawn from concepts in Object-oriented CSS ([OOCSS](https://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/)), blocks__elements setup of [BEM](https://css-tricks.com/bem-101/), components in [Material Design](http://getmdl.io/components/index.html) and atom-based libraries eg [Pattern Lab](http://demo.patternlab.io/?p=viewall-atoms-global)
    * Makes CSS naming way easier

##How is a library built?

* Break your site design down into individual objects/components/modules. Looks for patterns that are repeated throughout the design.
    * Refer to [Pattern Lab](http://demo.patternlab.io/?p=all) for help
* Each object should follow **single responsibility** practices.
* Create a component library of re-usable styles throughout site.
* Encourage designers to contribute to component library. This should tie directly into their styleguide!
* Call out styles that are very similar but not exact. Is it possible to unify them into one?
* Avoid using HTML tags as CSS selectors

<pre><code>
// Not good: lots of repetition, tied to markup
.sidebar h3 { color: blue; font-size: 14px; }
.footer h3  { color: blue; font-size: 14px; }
article h2  { color: blue; font-size: 14px; }

// Better: DRY, clearly named
.subsection-header { color: blue; font-size: 14px; }
</code></pre>

References: 

- http://demo.patternlab.io/



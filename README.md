# SassyBeam (draft)

## Another “BEM-like” notation

Beam (or SassyBeam) allows the use of a [BEM](http://bem.info/method/definitions/)-like notation.

It is based on [Nicolas Gallagher's thoughs](http://nicolasgallagher.com/about-html-semantics-front-end-architecture/) and [Harry Roberts's adaptations](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/) while adding my personal touch…

### The Beam goals

1. Applying a BEM method like `.block__element--modifier`.
2. Keeping a light HTML markup:
    ```
    <div class="block block--mod1 block--mod2">
    ```
    becomes:
    ```
    <div class="block--mod1--mod2">
    ```
3. Managing the states via pseudo-classes, classes or a data-state attribute.
4. Allowing the nesting of blocks and elements … or not!
5. Maintaining the integrity of class names (no dynamic concatenation like `#{$block}__element`)/

## Usage

### via Bower

```
$ bower install SassyBeam
```

## Extra

* [Examples](https://github.com/thierrymichel/SassyBeam/tree/master/examples) (more coming soon…)
* [Documentation](http://htmlpreview.github.io/?https://github.com/thierrymichel/SassyBeam/blob/master/docs/)
* Credits
    - [@necolas](https://github.com/necolas)
    - [@csswizardry](https://github.com/csswizardry)

---

**Feel free to improve, comment, share, …**

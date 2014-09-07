# SassyBeam (draft)

## Another “BEM-like” notation

Beam (or SassyBeam) allows the use of a [BEM](http://bem.info/method/definitions/)-like notation but with a lighter HTML markup.

It is based on [Nicolas Gallagher's thoughs](http://nicolasgallagher.com/about-html-semantics-front-end-architecture/) and [Harry Roberts's adaptations](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/) while adding my personal touch…

### The Beam goals

1. Applying a BEM method like `.block__element--modifier`.
2. Keeping a light HTML markup:

    ```
    <div class="block block--mod1 block--mod2 block--mod3">
    ```
    becomes:
    ```
    <div class="block--mod1--mod2--mod3">
    ```
    
3. Managing the states via pseudo-classes, classes or a data-state attribute.
4. Allowing the nesting of blocks and elements … or not!
5. Maintaining the integrity of class names (no dynamic concatenation like `#{$block}__element`).

## Usage

### via Bower

```
$ bower install SassyBeam
```

#### .html

```
<div class="foo">
    <div class="foo__baz"></div>
    <div class="foo__baz--qux"></div>
</div>
<div class="foo--bar"></div>
```

#### .scss

```
@import 'sassybeam';

@include beam('foo') {
    property: value;

    @include beam('foo--bar') {
        property: value;
    }

    @include beam('foo__baz') {
        property: value;

        @include beam('foo__baz--qux') {
            property: value;
        }
    }
}
```

#### .css (output)

```
.foo, [class*="foo--"] {
  property: value;
}
[class*="foo--"][class*="bar"] {
  property: value;
}
.foo__baz, [class*="foo__baz--"] {
  property: value;
}
[class*="foo__baz--"][class*="qux"] {
  property: value;
}
```

## Extra

* [Examples](https://github.com/thierrymichel/SassyBeam/tree/master/examples) (more coming soon…)
* [Documentation](http://htmlpreview.github.io/?https://github.com/thierrymichel/SassyBeam/blob/master/docs/)

---

**Feel free to improve, comment, share, …**

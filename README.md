# vui-grid-system
[![Bower version][bower-image]][bower-url]
[![NPM version][npm-image]][npm-url]
[![Build status][ci-image]][ci-url]
[![Dependency Status][dependencies-image]][dependencies-url]

This component contains [Sass mixins](http://sass-lang.com) for laying out and positioning UI elements using the standard Brightspace grid system.

For further information on this other VUI components, see the docs at [ui.valence.d2l.com](http://ui.valence.d2l.com/).

## Installation

`vui-grid-system` can be installed from [Bower][bower-url]:
```shell
bower install vui-grid-system
```

Or alternatively from [NPM][npm-url]:
```shell
npm install vui-grid-system
```

Depending on which installation method you choose, use that path when doing the SASS import:

```scss
@import "bower_components/vui-grid-system/grid-system.scss";
// or...
@import "node_modules/vui-grid-system/grid-system.scss";
```

## Usage

**Set the grid container:**

Use the `vui-gs-container` mixin to setup the grid container.  It defines the grid-system as per VUI design guidelines, including number of columns, dimensions, etc.

```scss
.my-application {
	@include vui-gs-container();
}
```

**Create rows:**

Use the `vui-gs-row` mixin to create styles for a complete grid row that spans all the columns.  Floats will be cleared automatically so elements that follow in the DOM will be rendered below.

```scss
.my-row {
	@include vui-gs-row();
}
```

**Create spans:**

Use the `vui-gs-span` mixin to create styles to span one or more columns.  Supports properties for defining edge columns, forcing breaks, and changing context (number of columns).

```scss
// an element that spans 2 columns
.span-2 {
	@include vui-gs-span(2);
}

// an element that spans the last 2 columns (no right margin)
.span-last-2 {
	@include vui-gs-span(last 2);
}

// an element that spans 2 columns and then breaks floats
.span-2-break {
	@include vui-gs-span(2 break);
}

// an element that spans 2 of 6 columns (changes context)
.span-2-of-6 {
	@include vui-gs-span(2 of 6);
}
```

Notes for `vui-gs-span` arguments:

* `last` is used to indicate the last span in a row, so that gutter margins are not applied after the element, thereby preventing the last span from wrapping.
* `break` is used to indicate that current floats should be cleared after the span, forcing the following spans onto a new row. This is helpful in some cases since it means spans do not necessarily need to wrapped in row `div`s.
* `of` is used to indicate a change in context. This is useful when you want to create a set of nested spans based on a different number of columns.

## Coding styles

See the [VUI Best Practices & Style Guide](https://github.com/Brightspace/valence-ui-docs/wiki/Best-Practices-&-Style-Guide) for information on VUI naming conventions, plus information about the [EditorConfig](http://editorconfig.org) rules used in this repo.

[bower-url]: http://bower.io/search/?q=vui-grid-system
[bower-image]: https://img.shields.io/bower/v/vui-grid-system.svg
[npm-url]: https://www.npmjs.org/package/vui-grid-system
[npm-image]: https://img.shields.io/npm/v/vui-grid-system.svg
[ci-url]: https://travis-ci.org/Brightspace/valence-ui-grid-system
[ci-image]: https://img.shields.io/travis-ci/Brightspace/valence-ui-grid-system.svg
[dependencies-url]: https://david-dm.org/brightspace/valence-ui-grid-system
[dependencies-image]: https://img.shields.io/david/Brightspace/valence-ui-grid-system.svg

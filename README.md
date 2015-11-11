# vui-grid-system
[![Bower version][bower-image]][bower-url]
[![NPM version][npm-image]][npm-url]
[![Build status][ci-image]][ci-url]
[![Dependency Status][dependencies-image]][dependencies-url]

This component contains Sass mixins for laying out UI elements as per the standard Brightspace VUI design.

## Installation

Install from NPM:
```shell
npm install vui-grid-system
```

Install from Bower:
```shell
bower install vui-grid-system
```

## Usage

Import the mixins:

```scss
@import 'bower_components/vui-grid-system/grid-system.scss'; // or...

@import "node_modules/vui-grid-system/grid-system.scss";
```

Set the grid container - this sets up the grid system for the specified element:

```scss
.app {
	@include vui-gs-container;
}
```



For further information on this component and other VUI components, see the docs at [ui.valence.d2l.com](http://ui.valence.d2l.com/).

#### Coding styles

See the [VUI Best Practices & Style Guide](https://github.com/Brightspace/valence-ui-docs/wiki/Best-Practices-&-Style-Guide) for information on VUI naming conventions, plus information about the [EditorConfig](http://editorconfig.org) rules used in this repo.

[bower-url]: http://bower.io/search/?q=vui-grid-system
[bower-image]: https://img.shields.io/bower/v/vui-grid-system.svg
[npm-url]: https://www.npmjs.org/package/vui-grid-system
[npm-image]: https://img.shields.io/npm/v/vui-grid-system.svg
[ci-url]: https://travis-ci.org/Brightspace/valence-ui-grid-system
[ci-image]: https://img.shields.io/travis-ci/Brightspace/valence-ui-grid-system.svg
[dependencies-url]: https://david-dm.org/brightspace/valence-ui-grid-system
[dependencies-image]: https://img.shields.io/david/Brightspace/valence-ui-grid-system.svg

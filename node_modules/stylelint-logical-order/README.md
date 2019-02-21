# stylelint-logical-order

[![NPM version][version-img]][npm-url] [![Build status][ci-img]][ci-url] [![License][l-img]][l-url]

Stylelint config that sorts related property declarations by grouping together following the order:

1) Special
2) Position
3) Box Model
4) Border
5) Box
6) Spacing
7) Typography
8) Content Layout
9) Visual
10) Background
11) Transform
12) Animation
13) Svg
14) Misc.

```scss
.element {
	/* Position */
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	z-index: 10;

	/* Box Model */
	display: block;
	float: right;
	width: 100px;
	height: 100px;

	/* Spacing */
	margin: 10px;
	padding: 10px;

	/* Border */
	border: 2px solid red;
	border-bottom-width: 1px;
	border-left: none;

	/* Typography */
	color: #888;
	font: normal 16px Helvetica, sans-serif;
	line-height: 1.3;
	text-align: center;

	/* Content Layout */
	columns-count: 3;

	/* Background */
	background-color: #eee;

	/* Transform */
	transform-origin: 0 0;
	transform: translateX(-50%);

	/* Visibilty */
	opacity: 1;

	/* Animation */
	transition: all 1s;

	/* Svg */
	fill: red;
	stroke: 2;

	/* Misc */
	user-select: none;
}
```

## Usage

1.  Add stylelint and this package to your project:

```bash
npm install --save-dev stylelint stylelint-logical-order
# or, if you prefer yarn over npm:
yarn add --dev stylelint stylelint-logical-order
```

2.  Add this package to the end of your extends array inside Stylelint
    configuration (.stylelintrc for example):

```javascript
{
  "extends": [
    "stylelint-logical-order"
  ]
}
```

## Credits

[npm-url]: https://www.npmjs.com/package/stylelint-logical-order
[version-img]: https://img.shields.io/npm/v/stylelint-logical-order.svg?style=flat-square
[ci-url]: https://travis-ci.org/constverum/stylelint-logical-order
[ci-img]: https://img.shields.io/travis/constverum/stylelint-logical-order.svg?style=flat-square
[l-url]: https://www.npmjs.com/package/stylelint-logical-order
[l-img]: https://img.shields.io/npm/l/stylelint-logical-order.svg?style=flat-square

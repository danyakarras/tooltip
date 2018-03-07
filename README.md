# d2l-tooltip

[Polymer](https://www.polymer-project.org)-based web component for D2L tooltips.

## Usage

Include the [webcomponents.js](http://webcomponents.org/polyfills/) "lite" polyfill (for browsers who don't natively support web components), then import `d2l-tooltip.html`:

```html
<head>
	<script src="bower_components/webcomponentsjs/webcomponents-lite.js"></script>
	<link rel="import" href="../d2l-tooltip/d2l-tooltip.html">
</head>
```

<!---
```
<custom-element-demo>
	<template>
		<script src="../webcomponentsjs/webcomponents-lite.js"></script>
		<link rel="import" href="../d2l-typography/d2l-typography.html">
		<link rel="import" href="d2l-tooltip.html">
    	<custom-style include="d2l-typography">
	    	<style is="custom-style" include="d2l-typography">
			</style>
    	</custom-style>
    	<style>
			html {
				padding: 50px;
				font-family: 'Lato', 'Lucida Sans Unicode', 'Lucida Grande', sans-serif;
				font-size: 20px;
			}
			.box {
				width: 100px;
				height: 100px;
				background-color: #e57231;
				display: inline-block;
				color: White;
				display: flex;
				align-items: center;
				text-align: center;
			}
		</style>
    	<next-code-block></next-code-block>
	</template>
</custom-element-demo>
```
-->
```html
<span class="box" id="target">Hover me</span>
<d2l-tooltip for="target">Hello world!</d2l-tooltip>
```

Use the `postition` attribute to place the tooltip to the top, bottom, left, or right of your target element:
<!---
```
<custom-element-demo>
	<template>
		<script src="../webcomponentsjs/webcomponents-lite.js"></script>
		<link rel="import" href="../d2l-typography/d2l-typography.html">
		<link rel="import" href="d2l-tooltip.html">
    	<custom-style include="d2l-typography">
	    	<style is="custom-style" include="d2l-typography">
			</style>
    	</custom-style>
    	<style>
			html {
				padding: 50px;
				font-family: 'Lato', 'Lucida Sans Unicode', 'Lucida Grande', sans-serif;
				font-size: 20px;
			}
			.box {
				width: 100px;
				height: 100px;
				background-color: #e57231;
				display: inline-block;
				color: White;
				display: flex;
				align-items: center;
				text-align: center;
			}
		</style>
    	<next-code-block></next-code-block>
	</template>
</custom-element-demo>
```
-->
```html
<span class="box" id="target">Hover me</span>
<d2l-tooltip for="target" position="right">Hello world!</d2l-tooltip>
```

Custom CSS properties for styling:

- All three properties should be set to style the box correctly:
  - `--d2l-tooltip-background-color` - the color of the tooltip box
  - `--d2l-tooltip-border` - (e.g., `1px solid;`)
  - `--d2l-tooltip-border-color` - border color
- `--d2l-tooltip-mixin` - styles on the content within the tooltip

<!---
```
<custom-element-demo>
	<template>
		<script src="../webcomponentsjs/webcomponents-lite.js"></script>
		<link rel="import" href="../d2l-typography/d2l-typography.html">
		<link rel="import" href="d2l-tooltip.html">
    	<custom-style include="d2l-typography">
	    	<style is="custom-style" include="d2l-typography">
				.mixin-tooltip {
					--d2l-tooltip-background-color: #ffffff;
					--d2l-tooltip-border: 1px solid;
					--d2l-tooltip-border-color:  #d3d9e3;

					--d2l-tooltip-mixin: {
						width: 200px;
						box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.08);
						font-family: Lato;
						color: #565a5c;
					}
				}
			</style>
    	</custom-style>
    	<style>
			html {
				padding: 50px;
				font-family: 'Lato', 'Lucida Sans Unicode', 'Lucida Grande', sans-serif;
				font-size: 20px;
			}
			.box {
				width: 100px;
				height: 100px;
				background-color: #e57231;
				display: inline-block;
				color: White;
				display: flex;
				align-items: center;
				text-align: center;
			}
		</style>
    	<next-code-block></next-code-block>
	</template>
</custom-element-demo>
```
-->
```html
<span class="box" id="target">Hover me</span>
<d2l-tooltip for="target" position="right" class="mixin-tooltip">Hello world!</d2l-tooltip>
```

## Demo

To run the demo run `npm install`, `polymer serve`.

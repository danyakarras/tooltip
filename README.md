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
				.mixin-tooltip {
          --tooltip-background-color: #ffffff;
          --tooltip-border: 1px solid;
          --tooltip-border-color:  #d3d9e3;

          --tooltip-mixin: {
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
<span class="box" id="top">Hover me (top)</span>
<d2l-tooltip position="top" for="top">Top</d2l-tooltip>
```

Custom CSS properties for styling:

- All three properties should be set to style the box correctly:
  - `--tooltip-background-color` - the color of the tooltip box
  - `--tooltip-border` - (e.g., `1px solid;`)
  - `--tooltip-border-color` - border color
- `--tooltip-mixin` - styles on the content within the tooltip

## Demo

To run the demo run `npm install`, `npm start` and visit http://localhost:9998/components/d2l-tooltip/demo/

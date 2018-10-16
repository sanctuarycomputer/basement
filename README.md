<p align="center">
  <img src="basement_logo.svg" width="400"/>
</p>

# Basement
Ground floor CSS utility classes

# How to
Import any settings before the `src/index.scss` file and any default settings will get overwritten:
```
@import
  'overrides',
  'src/index';
```

# Usage with Webpack (or Create React App)

First, install the webpack deps for compiling sass:

```
yarn install basement sass-loader node-sass --dev
```

Add the following loader to your webpack config (you'll need to use [react-app-rewired](https://github.com/timarney/react-app-rewired) if you haven't ejected):

```
{
  test: /\.scss$/,
  loaders: [
    require.resolve('style-loader'),
    require.resolve('css-loader'),
    require.resolve('sass-loader'),
  ]
},
```

Then rename your `index.css` file to `index.scss` (and be sure to change any javascript imports to `import 'index.scss';`). Sass should be working nicely, now!

---

Now you can install basement:

```
yarn install basement --dev
```

And require it in `index.scss` like so:

```
@import '~basement/src/index';
```

# Settings

Overwriting these settings is encouraged! To do so, define them in a `.scss` file and import them before Basement.

| variable | description | default |
| --- | --- | --- |
| `$grid-columns` | Amount of columns in the grid. | `12` |
| `$colors` | Color map use for `color-<color>`, `bg-color-<color>`, and `border-color-<color>` classes. | `('black': #000, 'white': #FFF, 'blue': #0A3862);` |
| `$breakpoints` | Media query breakpoints. | `('sm': 640px, 'md': 832px, 'lg': 1024px, 'xl': 1152px)` |
| `$spacing-units` | Spacing units for padding and margin. | `0rem, .25rem, .5rem, .75rem, 1rem, 2rem, 3rem, 4rem, 6rem, 8rem;` |
| `$aspect-ratios` | Ratios for `.aspect-<ratio>` utility class. | `('square': (1, 1), 'landscape': (16, 9), 'portrait': (2, 3));`|
| `$dynamic_spacing` | Whether or not each margin and padding class is generated for each breakpoint. | `true` |
| `$decimal_deliminator` | The deliminator used to replace a `.` | `'_'` |
| `$dynamic-grid` | Whether or not each `col-<i>` class is generated for each breakpoint. | `true` |

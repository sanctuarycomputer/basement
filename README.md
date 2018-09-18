![Alt text](basement_logo_1200.png?raw=true "Basement Logo")

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
Spacing units for padding and margin.
```
$spacing-units: 0rem, .25rem, .5rem, .75rem, 1rem, 2rem, 3rem, 4rem, 6rem, 8rem;
```

Ratios for `.aspect-<ratio>` utility class.
```
$aspect-ratios: (
  'square': (1, 1),
  'landscape': (16, 9),
  'portrait': (2, 3)
);
```

Breakpoints
```
$breakpoints: (
  'sm': 640px,
  'md': 832px,
  'lg': 1024px,
  'xl': 1152px
);
```

Dynamic spacing (whether or not each margin and padding class is generated for each breakpoint).
```
$dynamic_spacing: true;
```

The deliminator used to replace a `.`
`mb1_5` = `margin-bottom: 1.5rem`
```
$decimal_deliminator: '_';
```

Dynamic grid (hether or not each `col-<i>` class is generated for each breakpoint).
```
$dynamic-grid: true;
```

Amount of columns in the grid.
```
$grid-columns: 12;
```

Color map.
```
$colors: (
  'black': #000,
  'white': #FFF,
  'blue': #0A3862
);
```

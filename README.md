# Basement
Ground floor CSS utility classes

# How to
Import any settings before the `src/index.scss` file and any default settings will get overwritten:
```
@import
  'overrides',
  'src/index';
```

# Settings
Spacing units for padding and margin.
```
$spacing-units: 0rem, .25rem, .5rem, .75rem, 1rem, 2rem, 3rem, 4rem, 6rem, 8rem;
```

Z indicies
```
$z-indicies: 0, 1, 2, 3;
```

Border widths
```
$border-widths: 0, 1px, 2px, 3px;
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
  'sm': 40rem,
  'md': 52rem,
  'lg': 64rem,
  'xl': 72rem
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

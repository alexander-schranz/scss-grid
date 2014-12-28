# Dynamic Grid Generator

Simple to modified with scss/sass variables. Used to add dynamic breakpoints to your grid system.

Copy src/grid.scss and src/grid-ie.scss into your project and edit the variables for your own use: 
``` scss
$grid_defaultPadding: 2%;
$grid_defaultFontSize: $defaultFontSize; // needed for inlineBlock Grid
$grid_size: 12; // 12, 18, 24, ...
$grid_type: 'float'; // float, inlineBlock
$grid_breakPoints: (
        (
                'prefix': 'tab',
                'maxWidth': '1023px',
                'padding': $grid_defaultPadding,
                'fontSize': $grid_defaultFontSize // needed for inlineBlock Grid
        ),
        (
                'prefix': 'pal',
                'maxWidth': '679px',
                'padding': $grid_defaultPadding,
                'fontSize': $grid_defaultFontSize // needed for inlineBlock Grid
        ),
        (
                'prefix': 'mob',
                'maxWidth': '479px',
                'padding': $grid_defaultPadding,
                'fontSize': $grid_defaultFontSize // needed for inlineBlock Grid
        )
);
```

Use the grid in your HTML:

``` html
<div class="grid">
    <div class="grid-3 tab-grid-6 mob-grid-12">
        Element 1
    </div>
    <div class="grid-3 tab-grid-6 mob-grid-12">
        Element 2
    </div>
    <div class="grid-2 tab-grid-4 mob-grid-12">
        Element 3
    </div>
    <div class="grid-4 tab-grid-8 mob-grid-12">
        Element 4
    </div>
</div>
```

# Changelog

## 0.1
 - Create dynamic grid system generator

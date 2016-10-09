SomeGrid
==========

SomeGrid is a very easy CSS grid framework which uses Flexbox. SomeGrid was made using SCSS, is fully responsive and has 12 columns. It's far from perfect, but it works. SomeGrid is made by [Jasper van Merle][jasper-van-merle]

Download
--------

The entire source code of SomeGrid is available on GitHub.

[View on GitHub >][github]

Media queries
------------

These media queries were taken from the Bootstrap CSS Framework (version 3). They are awesome. The only difference is that SomeGrid uses em instead of px, so all pixel values from Bootstrap were divided by 16.

|                 | Extra small devices - Phones (<46.8125em) | Small devices - Tablets (≥46.875em)              | Medium devices - Desktops (≥60.625em)            | Large devices - Desktops (≥73.125em)             |
|-----------------|-------------------------------------------|--------------------------------------------------|--------------------------------------------------|--------------------------------------------------|
| Grid behavior   | Horizontal at all times                   | Collapsed to start, horizontal above breakpoints | Collapsed to start, horizontal above breakpoints | Collapsed to start, horizontal above breakpoints |
| Container width | Auto (0.9375em on the left and the right) | 46.875em                                         | 60.625em                                         | 73.125em                                         |
| Class prefix    | `.col-xs-`                                | `.col-`                                          | `.col-`                                          | `.col-`                                          |

Grid
---------------

[Grid demo >][demo-grid]

### Default grid

The default grid layout looks like this:
``` html
<div class="grid">
    <div class="row">
        <div class="col-6">
            6/12
        </div>
        <div class="col-6">
            6/12
        </div>
    </div>
</div>
```

*In short: `.grid` is the container holding `.row`'s, which is a container holding columns.*

### Columns on extra small devices

Default columns go to 100% width on phones and other extra small devices. To keep the columns 50% width, use col-xs-6. Ofcourse, the 6 could aswell just be any number between 1 and 12.
``` html
<div class="grid">
    <div class="row">
        <div class="col-xs-6">
            6/12 - also on extra small devices like phones
        </div>
        <div class="col-xs-6">
            6/12 - also on extra small devices like phones
        </div>
    </div>
</div>
```

### Nested columns

Nested columns are also possible. To do this, put a new `.row` inside a column.
``` html
<div class="grid">
    <div class="row">
        <div class="col-6">
            <div class="row">
                <div class="col-6">
                    3/12 (nested in a 6/12)
                </div>
                <div class="col-6">
                    3/12 (nested in a 6/12)
                </div>
            </div>
        </div>
        <div class="col-6">
            6/12
        </div>
    </div>
</div>
```

### Offsets

[Grid offsets demo >][demo-grid-offsets]

To move a column to the right without needing dummy columns, you can use offsets.
``` html
<div class="grid">
    <div class="row">
        <div class="col-6 col-offset-6">
            6/12 - moved 3/12 to the right
        </div>
    </div>
</div>
```

By default, offsets aren't visible on phones and the column will just take 100% width. To have offsets on extra small devices, use `.col-xs-` and `.col-xs-offset-`
``` html
<div class="grid">
    <div class="row">
        <div class="col-xs-6 col-xs-offset-6">
            6/12 - moved 3/12 to the right - also on extra small devices like phones
        </div>
    </div
</div>
```

### Fluid grid

To make the grid fluid, simply use the `.grid-fluid` container instead of `.grid`.
``` html
<div class="grid-fluid">
    <div class="row">
        <div class="col-6">
            6/12
        </div>
        <div class="col-6">
            6/12
        </div>
    </div>
</div>
```

Visibility classes
------------

[Visibility demo >][demo-visibility]

To hide certain parts of your page on certain screen sizes, there are a few visibility classes:

* `.hide-on-phone`
* `.hide-on-small`
* `.hide-on-small-and-up`
* `.hide-on-medium`
* `.hide-on-medium-and-up`
* `.hide-on-large`

These classes should speak for themselves.

[jasper-van-merle]: https://jaspervanmerle.com/
[github]: https://github.com/JvanMerle/some-grid
[demo-grid]: https://jaspervanmerle.com/some-grid/examples/grid.html
[demo-grid-offsets]: https://jaspervanmerle.com/some-grid/examples/grid-offsets.html
[demo-visibility]: https://jaspervanmerle.com/some-grid/examples/visibility.html
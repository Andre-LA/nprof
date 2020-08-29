# NProf

Very basic profiler to Raylib-nelua.  
Inspired by [JProf](https://github.com/pfirsich/jprof)

## Compile-time options:

* `PROF`: to use nprof, you must define _PROF_ with `-D PROF` argument.
* `NPROF`:
    * `use_colors`: `true` by default; when `false`, `WHITE` color is used to draw elements, otherwise it'll use different colors.
    * `scale`: `{x=1, y=24}` by default; for _y_ axis, the element's _rectangle height_ is defined as _scale.y_; for _x_ axis, an element's _rectangle width_ is defined as the _absolute of the scale.x_ when negative, otherwise, when positive, is defined as the _screen width_ `*` _scale.x_.
* `TEST`: only useful on nprof development.

## How to use

Check the [Rotor raylib example](https://gitlab.com/Andre-LA/rotor-nelua/-/blob/master/examples/raylib.nelua)

Preview:  
![nprof-gif-preview](nprof_preview.gif)

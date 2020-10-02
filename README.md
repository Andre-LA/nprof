# NProf

Very basic profiler to Raylib-nelua.  
Inspired by [JProf](https://github.com/pfirsich/jprof)

## Dependencies

- [Raylib-nelua](https://github.com/Andre-LA/raylib-nelua) (by default, but it's' optional since you can disable drawing with the compile-time options cited below)

## Compile-time options:

* `PROF`: to use nprof, you must define `PROF` with `-D PROF` option.
* `NPROF`:
    * `use_colors`: `false` by default; when `false`, `WHITE` color is used to draw elements, otherwise it'll use different colors.
    * `scale`: `{x=1, y=24}` by default; for _y_ axis, the element's _rectangle height_ is defined as _scale.y_; for _x_ axis, an element's _rectangle width_ is defined as the _absolute of the scale.x_ when negative, otherwise, when positive, is defined as the _screen width_ `*` _scale.x_.
    * `draw_list`: `true` by default; it will draw a list on upper-left corner when `true`.
    * `draw_rects`: `true` by default; it will draw stack of rects on the bottom of screen when `true`.
* `TEST`: runs a basic test, only useful for nprof development.

**NOTE: When both `NPROF.draw_list` and `NPROF.draw_rects` are false, raylib  will not be required**

## How to use

Check the [Rotor raylib example](https://gitlab.com/Andre-LA/rotor-nelua/-/blob/master/examples/raylib.nelua)

Preview:  
![nprof-gif-preview](nprof_preview.gif)

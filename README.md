# NProf

Very basic profiler, also supports drawing using either [Raylib-nelua](https://github.com/Andre-LA/raylib-nelua) or [tico-nelua](https://github.com/Andre-LA/tico-nelua).
Inspired by [JProf](https://github.com/pfirsich/jprof)

## Dependencies
There is no external dependencies unless when drawing is enabled, which will use an _drawing implementation_ specified by
 `NPROF.draw_impl`, which must be either `"raylib"` or `"tico"`; the external dependency is the specified implementation:

- if `NPROF.draw_impl` is `"raylib"`: [Raylib-nelua](https://github.com/Andre-LA/raylib-nelua)
- if `NPROF.draw_impl` is `"tico"`: [tico-nelua](https://github.com/Andre-LA/tico-nelua)

## Compile-time options:

* `PROF`: to use nprof, you must define `PROF` with `-D PROF` option.
* `NPROF`:
    * `use_colors`: `false` by default; when `false`, `WHITE` color is used to draw elements, otherwise it'll use different colors.
    * `scale`: `{x=1, y=24}` by default; for _y_ axis, the element's _rectangle height_ is defined as _scale.y_; for _x_ axis, an element's _rectangle width_ is defined as the _absolute of the scale.x_ when negative, otherwise, when positive, is defined as the _screen width_ `*` _scale.x_.
    * `draw_list`: `true` by default; it will draw a list on upper-left corner when `true`.
    * `draw_rects`: `true` by default; it will draw stack of rects on the bottom of screen when `true`.
    * `draw_impl`: `false` by default; it must be either `"raylib"` or `"tico"`, it  specifies what drawing implementation should be used.
* `TEST`: runs a basic test, only useful for nprof development.

**NOTE: When both `NPROF.draw_list` and `NPROF.draw_rects` are false, no _drawing implementation_ is required**

## How to use

Check the [Rotor raylib example](https://gitlab.com/Andre-LA/rotor-nelua/-/blob/master/examples/raylib.nelua)

Preview:  
![nprof-gif-preview](nprof_preview.gif)

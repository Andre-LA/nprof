# NProf

Very basic profiler to Raylib-nelua.  
Inspired by [JProf](https://github.com/pfirsich/jprof)

## Compile-time options:

* `PROF`: to use nprof, you must define _PROF_ with `-DPROF` argument.
* `NPROF_COLORS`: by default, nprof use _WHITE_ color constant to draw; when _NPROF_COLORS_ is defined, it will use a color.
* `TEST`: only useful on nprof development.

## How to use

Check the [Rotor raylib example](https://gitlab.com/Andre-LA/rotor-nelua/-/blob/master/examples/raylib.nelua)

Preview:  
![nprof-gif-preview](nprof_preview.gif)

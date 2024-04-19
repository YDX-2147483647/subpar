# subpar
**NOTE: This package is not yet released and undocumented as I hash out the exact API and work out the kinks. You can help by trying it out locally and reporting issues as you encounter them.**

Subpar is a [Typst] package allowing you to create easily referencable subfigures.

```typst
#import "@preview/subpar:0.0.1": subpar-grid

#set page(height: auto)
#set par(justify: true)

#subpar-grid(
  (figure(image("/assets/andromeda.jpg"), caption: [
    An image of the andromeda galaxy.
  ]), <a>),
  (figure(image("/assets/mountains.jpg"), caption: [
    A sunset illuminating the sky above a mountain range.
  ]), <b>),
  columns: (1fr, 1fr),
  caption: [A figure composed of two subfigures.],
  label: <full>,
)


Above in @full, we see a figure which is composed of 2 other figures, namely @a and @b.
```
![ex]

## Known Issues
- [x] Relative numbering is incorrect for super-figures, see [#1]
- [ ] Supplement is always "Figure", regardless of `text.lang`, see: [#2]
- [ ] Sub figure captions are not vertically aligned, see [#3]

## TODO
The following tasks remain before the first version of subpar is released:
- [x] documentation
- [ ] manual generation
- [x] allow more control over figure layout
- [x] add convenient warppers for common types of super figures
- [x] add input validation
- [ ] add more comprehensive tests

[ex]: /examples/example.png

[Typst]: https://typst.app/

[#1]: https://github.com/tingerrr/subpar/issues/1
[#2]: https://github.com/tingerrr/subpar/issues/2
[#3]: https://github.com/tingerrr/subpar/issues/3

# CSS Questions

## What is CSS specificity?
Certain CSS rules replace (override) others by being more specific.
Three types: type, class, id (lowest to highest)

## What is z-index?
Controls the vertical stacking order of elements that overlap.
Only affects elements that have a position value which is not static.

## What's the difference between these selectors?
| selector  | description |
| --------- | ----------- |
| `*`       | Selects all elements                                                          |
| `div > p` | Selects all `<p>` elements where the parent is a `<div>` element              |
| `div + p` | Selects all `<p>` elements that are placed immediately after `<div>` elements |
| `div ~ p` | Selects every `<p>` element that are preceded by a `<div>` element            |
| `div, p`  | Selects all `<div>` elements and all `<p>` elements                           |
| `div p`   | Selects all `<p>` elements inside `<div>` elements                            |

## What's the difference between flexbox and grid?
Flexbox is made for 1D layouts (alignment) and Grid is made for 2D layouts.
Flexbox takes basis in the content while Grid takes basis in the layout.
Grid is mostly defined on the parent element. In flexbox, most of the layout happen on the children.

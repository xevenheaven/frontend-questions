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

## What are the different position values?
| position | description |
| -------- | ----------- |
| static   | (Default value) Elements render in order, as they appear in the document flow                   |
| absolute | Element is positioned relative to its first positioned (not static) ancestor element            |
| fixed    | Element is positioned relative to the browser window                                            |
| relative | Element is positioned relative to its normal position                                           |
| sticky   | Element is positioned based on the user's scroll position (toggling between relative and fixed) |
| initial  | Sets this property to its default value                                                         |
| inherit  | Inherits this property from its parent element                                                  |

## What are pseudo classes and what are they used for?
Pseudo classes are similar to pseudo elements, but instead of styling a part of an element, they apply styles when an element is in a certain state. Another common use case is to style only certain occurrences of elements in a row.

| selector       | description |
| -------------- | ----------- |
| :active        | Selects active element                     |
| :disabled      | Selects disabled element                   |
| :first-child   | Selects first child                        |
| :focus         | Selects element that has focus             |
| :hover         | Selects element on mouse over              |
| :last-child    | Selects last child                         |
| :not(selector) | Selects element that is not given selector |
| :nth-child(n)  | Selects the nth child                      |
| :required      | Selects elements with a required attribute |

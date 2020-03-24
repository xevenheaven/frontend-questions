# React Questions

## Differentiate between Real DOM and Virtual DOM.
| Real DOM                              | Virtual  DOM                        |
| ------------------------------------- | ----------------------------------- |
| It updates slow.                      | It updates faster.                  |
| Can directly update HTML.             | Can’t directly update HTML.         |
| Creates a new DOM if element updates. | Updates the JSX if element updates. |
| DOM manipulation is very expensive.   | DOM manipulation is very easy.      |
| Too much of memory wastage.           | No memory wastage.                  |

## Explain how Virtual DOM works.
A virtual DOM is a lightweight JavaScript object which originally is just the copy of the real DOM.
It is a node tree that lists the elements, their attributes and content as Objects and their properties.
React’s render function creates a node tree out of the React components.
It then updates this tree in response to the mutations in the data model.
1. Whenever any underlying data changes, the entire UI is re-rendered in Virtual DOM representation.
2. Then the difference between the previous DOM representation and the new one is calculated.
3. Once the calculations are done, the real DOM will be updated with only the things that have actually changed.

## Explain the purpose of render() in React.
Each React component must have a render() mandatorily. It returns a single React element
which is the representation of the native DOM component. If more than one HTML element needs to be rendered,
then they must be grouped together inside one enclosing tag. This function must be kept pure i.e.,
it must return the same result each time it is invoked.

## Differentiate between state and props.
Props get passed to the component similar to function parameters.
State is managed within the component similar to variables declared within a function.

| Conditions                                  | State | Props |
| ------------------------------------------- | ----- | ----- |
| Receive initial value from parent component | Yes   | Yes   |
| Parent component can change value           | No    | Yes   |
| Set default values inside component         | Yes   | Yes   |
| Changes inside component                    | Yes   | No    |
| Set initial value for child components      | Yes   | Yes   |
| Changes inside child components             | No    | Yes   |

## Explain what is a Higher Order Component (HOC) and how it is useful.
Concretely, a HOC is a function that takes a component and returns a new component.
It transforms a component into another component. It is a pure function with zero side-effects.
The goal of this pattern is to decompose the logic into simpler and smaller functions that can be reused.
(Similar to a higher order function e.g. map(), that takes in another function.)

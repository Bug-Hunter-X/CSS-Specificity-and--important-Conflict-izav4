# CSS Specificity and !important Conflict

This example demonstrates a subtle issue in CSS related to specificity and the `!important` declaration. The `!important` declaration typically overrides other styles, but in this case, a more specific selector does not override an `!important` rule.

## Bug Description

A parent element has a blue color, and a child element has a red color with `!important`.  A more specific selector targets the child within the parent and attempts to set it to green.  However, the `!important` declaration prevails, and the element remains red.

## How to Reproduce

1.  Create three HTML elements nested as parent-child relationships.
2.  Apply the provided CSS styles.
3.  Observe that the child element's color is red instead of green.

## Solution

The solution is to avoid using `!important` unless absolutely necessary and to refactor the CSS to avoid specificity conflicts.
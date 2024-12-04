# CSS `calc()` Function Calculation Errors

This repository demonstrates a common issue encountered when using the CSS `calc()` function.  The `calc()` function is powerful for dynamic calculations within CSS, but unexpected behavior can arise if not handled carefully.  This example showcases a situation where subtracting pixels from a percentage value doesn't work as intended.

## Bug Description

The `calc()` function, when used with percentage and pixel units, can produce unexpected results if the parent container's dimensions aren't clearly defined or if there are conflicting styles impacting the element's size.

## Bug Reproduction

1. Clone this repository.
2. Open `bug.html` in your web browser.
3. Observe the unexpected behavior of the inner div's width, which should be 50% of its parent's width minus 50px, but is not calculated correctly due to the missing or conflicting styles.

## Solution

The solution involves ensuring the parent element's width is explicitly defined, allowing `calc()` to accurately perform the calculation.  Removing conflicting styles also helps avoid unexpected behavior. The corrected CSS is shown in `bugSolution.css`.
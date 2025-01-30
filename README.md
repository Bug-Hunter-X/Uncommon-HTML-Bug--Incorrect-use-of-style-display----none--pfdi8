# Uncommon HTML Bug: Incorrect Use of style.display = "none"

This repository demonstrates an uncommon bug related to using `style.display = "none"` in JavaScript to hide HTML elements.  While seemingly simple, this approach can lead to unexpected layout issues, especially when combined with other layout-dependent elements or transitions.

The bug is found in `bug.html`. The solution is presented in `solution.html`.

## Bug Description:

The issue arises from the fact that setting `style.display = "none"` completely removes the element from the document's flow. This can have unexpected consequences when using it to hide an element that is later shown, as it can shift or alter the layout of other elements on the page.

## Solution:

The solution employs the `visibility: hidden;` CSS property instead.  `visibility: hidden` hides the element but preserves its layout space, making it ideal for situations where you want to maintain the visual flow of the page.

## How to reproduce the bug:
1. Open `bug.html` in a web browser.
2. Observe the initial state where the element is hidden.
3. After three seconds, the element reappears, potentially leading to layout shifts if other elements were position relative to it.
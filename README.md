# CSS Bug: :checked Pseudo-class with Radio Buttons and Labels

This repository demonstrates a subtle bug related to the CSS `:checked` pseudo-class when used with radio buttons and labels. The bug occurs when dealing with multiple radio buttons or when elements are present between a radio button and its label.

## Bug Description
The provided CSS attempts to change the color of a label when its associated radio button is selected.  However, it might fail if:

1.  Multiple radio buttons share the same `name` attribute.
2.  Elements exist between the radio button and its label.

## Solution
The solution involves using the general sibling combinator (`~`) instead of the adjacent sibling combinator (`+`). The general sibling combinator selects all following siblings, regardless of intervening elements.  The solution also ensures the labels for radio buttons include a consistent class for the styling.  

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Observe the unexpected styling behavior.
4. Open `bugSolution.html` and notice the corrected behavior.

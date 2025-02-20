# Tailwind CSS Specificity Conflict Bug

This repository demonstrates a bug where custom CSS rules unintentionally override Tailwind CSS utility classes, leading to unexpected styling issues.

## Description

The problem occurs when custom CSS rules have higher specificity than Tailwind's generated classes.  This can happen if your custom selectors are more specific (e.g., using more IDs or classes) or if you use !important declarations in your custom styles.

## Reproduction

1. Clone this repository.
2. Open `bug.css` to see the conflicting custom styles.
3. Open `index.html` (or equivalent) in a browser.  Observe that the styles aren't applied as expected due to the specificity conflict.

## Solution

The solution is shown in `bugSolution.css`.  This can involve adjusting your CSS specificity, making your selectors more general, or avoiding the use of !important.

## Additional Notes

This bug highlights the importance of understanding CSS specificity and the order in which styles are applied.  Using a CSS preprocessor (like Sass or Less) can help manage CSS complexity and avoid such conflicts.
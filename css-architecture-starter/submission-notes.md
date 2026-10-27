Kiara L. McRae · GIT 414

## Layer Order

My layer order is:

reset, base, layout, components, utilities, overrides

The reset layer creates the box sizing and removes the default body margin. Base defines custom properties and element styles. Layout is controlling the page width, spacing, and the responsive card grid. Components styles reusable navigation links, buttons, cards, and form controls. Utilities gives us small adjustments. Overrides contains focus, current-page, and print styles.

## Three Token Decisions

1. Color: --color-brand provides a consistent terracotta color for links, buttons, and the current navigation item. Updating this token changes all of those uses together at the same time.

2. Type: --font-body and --font-heading separate body and heading typography. --text-heading uses clamp() to let the main heading resize within minimum and maximum limits.

3. Shape and focus: Shared radius tokens keep cards and controls consistent. Focus tokens define a blue 3px outline with a 3px offset for keyboard focus.

## Easier Maintenance

All three session cards share the .card class, and the registration link and submit button share .button. This lets me update repeated components in one place.

The HTML also uses three utilities: .u-measure limits text width, .u-stack adds spacing between direct children, and .u-uppercase formats introductory labels.

## State and Print Styles

:focus-visible provides a visible keyboard-focus indicator. The [aria-current="page"] selector identifies Home through an underline, bold text, and a contrasting background.

Print styles hide navigation and form controls, stack the cards, simplify colors, reduce section spacing, and discourage page breaks inside cards and callouts.

## Scope

This remains the supplied practice page. Placeholder links and the demonstration form are kept. 



## AI disclosure

For this week's assignment, I used ChatGPT. The AI assistance included explain the starter structure, suggesting token names and identifying missing states. After trying to fix myself a few times, I used the AI to troubleshoot the problems in the output terminal as well with my styles.css. Most issues consisted of a missing bracket and invalid values for width properties. When I ran the issues through the checkers and kept getting errors, I asked ChatGPT to identify the errors in the code I typed.

## Documentation consulted

- MDN: https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@layer
- MDN: https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascading_variables/Using_custom_properties


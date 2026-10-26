Kiara L. McRae · GIT 414

## Layer order

`reset, base, layout, components, utilities, overrides`

Reset normalizes defaults; base defines tokens and element styles; layout handles page composition; components owns reusable patterns; utilities provides small adjustments; this overrides contains a local token exception and print exceptions. Print rules are nested in the final layer intentionally.

## Three token decisions

1. Color: `--color-brand` gives the same dark terracotta for buttons, links, and current navigation. Changing the token updates all of these uses together.
2. Type and spacing: system fonts do not use a font download; `--text-title` uses a fluid clamp, and a shared spacing scale helps control the gaps and padding.
3. Shape and focus: shared corner radius' keep the cards and controls consistent; a blue 3px outline with 3px offset gives us a reusable keyboard-focus treatment.

## Easier maintenance

The three cards use one `.card` rule, and the link and submit button share `.button`. Form inputs and the select share one control rule. Utilities `.u-stack`, `.u-measure`, and `.u-muted` are used in the HTML; `.visually-hidden` is available for accessible supporting text. A contextual token override gives the hero more spacing without making the stacking rule repeat over and over or duplicate. 

## States and print

`:focus-visible` marks keyboard focus, the skip link appears on focus, and `[aria-current="page"]` marks Home with an underline, weight, and background. Print rules remove navigation and the demonstration form, simplify colors, stack cards, and avoids splitting cards where possible.

## Scope and verification

The starter content and placeholder links are retained. The form is a demonstration and does not collect or save submissions or personal information.

I inspected the files for required layers, tokens, component classes, utility usage, focus/current states, and print rules. I tested for overflow, viewport, and navigation. I tested all CSS myself.

## AI disclosure

For this week's assignment, I used ChatGPT. The AI assistance included suggesting token names or identify missing states. After trying to fix myself a few times, I used the AI to troubleshoot the problems in the output terminal as well with my styles.css. Most issues consisted of a missing bracket and invalid values for width properties. When I ran the issues through the checkers and kept getting errors, I asked ChatGPT to identify the errors in the code I typed.

## Documentation consulted

- MDN: https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@layer
- MDN: https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascading_variables/Using_custom_properties


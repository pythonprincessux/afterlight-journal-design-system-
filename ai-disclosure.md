# Afterlight Journal - AI Disclosure and Verification Record

## Tool Used

ChatGPT (ASU Account)

## Purpose

I used ChatGPT as an AI-assisted support tool while developing the Afterlight Journal design-system specimen. I used it to compare possible publication concepts and visual directions, suggest design-token names, compare small palette and spacing alternatives, and help organize the relationship between primitive and semantic tokens.

I also used ChatGPT as a troubleshooting resource while I performed responsive, accessibility, typography, and validation tests in my own browser.

## Output Used

AI assistance contributed suggestions or explanations related to:

- selecting the Afterlight Journal concept and editorial direction
- comparing the Rich Editorial and Midnight theme directions
- naming color and design tokens
- organizing primitive and semantic color tokens
- organizing spacing, typography, radius, and elevation tokens
- understanding how semantic tokens allow themes to change without duplicating component rules
- identifying possible causes of horizontal overflow during responsive testing
- understanding how to test preferred-font failure using DevTools
- locating browser tools used to inspect contrast
- interpreting HTML and CSS validator results
- organzing lines of index and styles.css to render webpage correctly
- organizing the final testing and verification record
- structuring a polished code defense after taking my own notes and answering questions
- polishing submission.md
- organizing raw notes and unstructured notes for code defense summary

## Authority

I treated AI output as suggestions rather than authoritative evidence.

The final implementation was evaluated against the assignment requirements and verified using my own browser, Chrome DevTools, W3C HTML validation, W3C CSS validation, and the published GitHub Pages site.

AI-generated statements were not used as proof that a feature worked.

## Verification

I personally performed each of the required tests.

Responsive testing was performed at 320px, 768px, and 1280px. At 320px, the initial version produced 14px of horizontal overflow. I used DevTools to identify the elements contributing to the overflow, revised the responsive handling, and repeated the test until `scrollWidth` and `clientWidth` both measured 320px.

I also tested the page at 200% browser zoom and navigated the interactive examples using the keyboard to inspect focus visibility.

Both Rich Editorial and Midnight themes were tested. I inspected an action-text contrast pairing in each theme using DevTools. The Rich Editorial tested pair produced a contrast ratio of 8.75:1, and the Midnight tested pair produced a contrast ratio of 4.81:1.

To test typography fallback behavior, I disabled the browser cache and blocked the Google-hosted font requests in DevTools. The page continued rendering using its fallback font stacks while preserving readable hierarchy and layout.

I validated both of the HTML and CSS using the W3C validators. Initial HTML validation identified a heading-structure warning caused by an additional `h1` inside the typography specimen. I changed that example to the appropriate `h3` level and validated the document again. The final HTML result contained no errors or warnings. The CSS validator reported no errors.

Finally, I published the project through GitHub Pages and verified that the deployed specimen loaded and matched the locally tested version.

## Risk Review

The main risk of using AI during this project was accepting a suggested implementation or explanation without confirming whether it actually satisfied the assignment requirements.

To address that risk, I tested the implemented behavior independently and used browser inspection or validation tools for observable claims.

I also avoided treating suggested contrast values, responsive behavior, font behavior, or validation outcomes as verified until I observed the results myself.

## Decisions

I retained AI suggestions when they supported the design direction I selected and could be verified against the assignment requirements.

I modified suggestions when testing revealed a problem. For example, responsive testing revealed horizontal overflow at the 320px viewport, so I revised the implementation and retested it rather than assuming the original responsive rules were sufficient.

I also revised the typography specimen after the HTML validator identified a heading-structure issue.

## Explanation

I can explain the final implementation, including:

- the purpose of the selective reset
- the primitive-to-semantic token hierarchy
- why component color rules reference semantic color tokens
- how the Midnight theme overrides semantic properties without duplicating component rules
- the typography and fallback stacks
- responsive layout behavior
- keyboard focus treatment
- component states
- the 320px overflow revision
- the HTML heading revision
- how I tested and validated the final specimen
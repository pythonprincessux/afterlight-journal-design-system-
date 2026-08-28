# Afterlight Journal - Code Defense

## 1. Reset Strategy

Explain:
- why you used a selective reset instead of removing every browser default
- why `box-sizing`, body margin removal, responsive media, and inherited form fonts were included
- why you intentionally kept native focus outlines/list behavior/control affordances unless specifically styled

## 2. Token Hierarchy

Explain:
- primitive tokens store raw palette values
- semantic tokens assign roles such as background, surface, text, border, action, and focus
- components reference semantic color tokens
- spacing, typography, radius, and elevation tokens are shared system values
- this keeps components independent from a specific theme

## 3. Scoped Theme Override

Use Midnight as your example.

Explain:
- `[data-theme="midnight"]` changes semantic custom properties
- it changes background, surface, border, action, hover, text, and focus values
- component CSS does not need to be duplicated
- the same components automatically inherit the alternate theme

## 4. Evidence-Based Revision

Use the 320px overflow issue.

Explain:
- initial test: `scrollWidth = 334`, `clientWidth = 320`
- this meant there was 14px of page-level horizontal overflow
- DevTools showed the state table/code content contributing to the issue
- you revised the responsive CSS
- retest: `scrollWidth = 320`, `clientWidth = 320`
- this demonstrated why testing changed the implementation rather than simply confirming it
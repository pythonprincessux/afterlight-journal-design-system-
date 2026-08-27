# Afterlight Journal — Test Record

Fill in **Observed** and **Revision** only after actually performing each test in a browser.
Do not pre-fill these columns.

## Responsive

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| 320px viewport | No page-level horizontal overflow | | |
| 768px viewport | Card grid reflows; layout adapts appropriately | | |
| 1280px viewport | Content uses available width without stretching illegibly | | |

## Zoom

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| 200% browser zoom | Content remains readable | | |
| 200% browser zoom | Interactive elements remain operable | | |

## Keyboard

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| Tab through links | Visible gold focus outline | | |
| Tab through buttons (primary/secondary) | Visible gold focus outline | | |
| Tab to text input | Visible gold focus outline | | |
| Tab to select | Visible gold focus outline | | |
| Tab to checkbox | Visible gold focus outline | | |
| Tab to radio buttons | Visible gold focus outline | | |

## Themes

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| Default (Rich Editorial) contrast | Text/background pairs meet WCAG AA | | |
| Midnight contrast | Text/background pairs meet WCAG AA | | |
| Background changes between themes | Yes, via semantic token only | | |
| Surface changes between themes | Yes, via semantic token only | | |
| Border changes between themes | Yes, via semantic token only | | |
| Action / action-hover changes between themes | Yes, via semantic token only | | |
| Focus changes between themes | Yes, via semantic token only | | |
| No duplicated component rules for theme | Confirmed by inspecting styles.css | | |

## Typography

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| Libre Baskerville loads | Display headings render in Libre Baskerville | | |
| Inter loads | Body text renders in Inter | | |
| Preferred font blocked (DevTools → block Google Fonts request, hard reload) | Falls back to Georgia/Times New Roman/serif and Arial/Helvetica/sans-serif | | |
| Fallback readability | Hierarchy and measure remain legible in fallback stack | | |

## Validation

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| HTML validation (validator.w3.org) | No errors | | |
| CSS validation (jigsaw.w3.org/css-validator) | No errors | | |

## Publication

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| GitHub repository | Meaningful, incremental commits | | |
| GitHub Pages published | Site loads at published URL | | |
| Published site matches local specimen | No drift between local and deployed | | |
| All assets resolve | Fonts, CSS, and any images load with no 404s | | |

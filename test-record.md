# Afterlight Journal — Test Record

## Responsive

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| 320px viewport | No page-level horizontal overflow | Tested at 320px. No page-level horizontal overflow was present and content reflowed within the viewport. | No revision required. |
| 768px viewport | Card grid reflows; layout adapts appropriately | Tested at 768px. Cards and specimen content reflowed appropriately for the available width. | No revision required. |
| 1280px viewport | Content uses available width without stretching illegibly | Tested at 1280px. Content remained contained and readable without excessive line length. | No revision required. |

## Zoom

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| 200% browser zoom | Content remains readable | Tested at 200% zoom. Content remained readable and reflowed rather than requiring page-level horizontal scrolling. | No revision required. |
| 200% browser zoom | Interactive elements remain operable | Links, buttons, and controls remained visible and operable at 200% zoom. | No revision required. |

## Keyboard

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| Tab through links | Visible gold focus outline | Keyboard focus produced a clearly visible gold outline on links. | No revision required. |
| Tab through buttons (primary/secondary) | Visible gold focus outline | Primary and secondary buttons displayed the gold focus treatment when reached by keyboard. | No revision required. |
| Tab to text input | Visible gold focus outline | Text input displayed the visible gold focus treatment. | No revision required. |
| Tab to select | Visible gold focus outline | Select control displayed the visible gold focus treatment. | No revision required. |
| Tab to checkbox | Visible gold focus outline | Checkbox displayed a visible focus indicator during keyboard navigation. | No revision required. |
| Tab to radio buttons | Visible gold focus outline | Radio controls displayed a visible focus indicator during keyboard navigation. | No revision required. |

## Themes

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| Default (Rich Editorial) contrast | Text/background pairs meet WCAG AA | Rich Editorial action text was checked in DevTools and showed a contrast ratio of 8.75:1 against its background. | No revision required for the tested pair. |
| Midnight contrast | Text/background pairs meet WCAG AA | Midnight action text was checked in DevTools and showed a contrast ratio of 4.81:1 against its background. | No revision required for the tested pair. |
| Background changes between themes | Yes, via semantic token only | Background visibly changed between Rich Editorial and Midnight themes through the theme token mapping. | No revision required. |
| Surface changes between themes | Yes, via semantic token only | Surface colors changed with the selected theme. | No revision required. |
| Border changes between themes | Yes, via semantic token only | Border colors changed with the selected theme. | No revision required. |
| Action / action-hover changes between themes | Yes, via semantic token only | Action styling changed from burgundy-based colors to rust-based colors when switching themes. | No revision required. |
| Focus changes between themes | Yes, via semantic token only | Focus treatment remained clearly visible and used the theme-specific focus token. | No revision required. |
| No duplicated component rules for theme | Confirmed by inspecting styles.css | Theme differences are handled through semantic custom-property overrides rather than duplicated component rules. | No revision required. |

## Typography

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| Libre Baskerville loads | Display headings render in Libre Baskerville | DevTools Network showed the Libre Baskerville stylesheet and font resources loading successfully with status 200. | No revision required. |
| Inter loads | Body text renders in Inter | Body typography rendered using the intended Inter stack during normal testing. | No revision required. |
| Preferred font blocked (DevTools → block Google Fonts request, hard reload) | Falls back to Georgia/Times New Roman/serif and Arial/Helvetica/sans-serif | Google-hosted font resources were successfully blocked in DevTools and the page continued rendering with fallback fonts. | No revision required. |
| Fallback readability | Hierarchy and measure remain legible in fallback stack | With preferred font resources blocked, headings and body text remained readable and the visual hierarchy was preserved. | No revision required. |

## Validation

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| HTML validation (validator.w3.org) | No errors | Final HTML validation reported: “Document checking completed. No errors or warnings to show.” | Changed the specimen typography example from an additional `h1` to the appropriate heading level after the validator initially reported a heading-structure warning. Final validation returned no errors or warnings. |
| CSS validation (jigsaw.w3.org/css-validator) | No errors | W3C CSS Validator reported “Congratulations! No Error Found.” | No revision required. |

## Publication

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| GitHub repository | Meaningful, incremental commits | | |
| GitHub Pages published | Site loads at published URL | | |
| Published site matches local specimen | No drift between local and deployed | | |
| All assets resolve | Fonts, CSS, and any images load with no 404s | | |
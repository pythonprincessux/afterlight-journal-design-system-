# Afterlight Journal - Test Record

## Responsive

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| 320px viewport | No page-level horizontal overflow | Tested at 320px. After final revision, `scrollWidth` and `clientWidth` both measured 320px, confirming no page-level horizontal overflow. Content reflowed within the viewport. | Initial testing showed 14px of horizontal overflow. DevTools inspection identified the state table and code content as contributing elements. Responsive handling was revised and the test was repeated until `scrollWidth` equaled `clientWidth` at 320px. |
| 768px viewport | Card grid reflows; layout adapts appropriately | Tested at 768px. Cards and specimen content reflowed appropriately for the available width. `scrollWidth` and `clientWidth` both measured 768px. | No revision required. |
| 1280px viewport | Content uses available width without stretching illegibly | Tested at 1280px. Content remained contained and readable without excessive line length. `scrollWidth` and `clientWidth` both measured 1280px. | No revision required. |

## Zoom

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| 200% browser zoom | Content remains readable | Tested at 200% browser zoom. Content remained readable and reflowed without clipping or page-level horizontal overflow. | No revision required. |
| 200% browser zoom | Interactive elements remain operable | Links, buttons, and controls remained visible and operable at 200% zoom. | No revision required. |

## Keyboard

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| Tab through links | Visible gold focus outline | Keyboard navigation produced a clearly visible gold focus outline on links. | No revision required. |
| Tab through buttons (primary/secondary) | Visible gold focus outline | Primary and secondary buttons displayed the visible focus treatment when reached by keyboard. | No revision required. |
| Tab to text input | Visible gold focus outline | Text input displayed a visible focus treatment during keyboard navigation. | No revision required. |
| Tab to select | Visible gold focus outline | Select control displayed a visible focus treatment during keyboard navigation. | No revision required. |
| Tab to checkbox | Visible gold focus outline | Checkbox displayed a visible focus indicator during keyboard navigation. | No revision required. |
| Tab to radio buttons | Visible gold focus outline | Radio controls displayed a visible focus indicator during keyboard navigation. | No revision required. |

## Themes

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| Default (Rich Editorial) contrast | Text/background pairs meet WCAG AA | Rich Editorial action text was inspected in DevTools and showed a contrast ratio of 8.75:1 against its tested background. | No revision required for the tested pair. |
| Midnight contrast | Text/background pairs meet WCAG AA | Midnight action text was inspected in DevTools and showed a contrast ratio of 4.81:1 against its tested background. | No revision required for the tested pair. |
| Background changes between themes | Yes, via semantic token only | Background visibly changed between Rich Editorial and Midnight through the semantic theme token mapping. | No revision required. |
| Surface changes between themes | Yes, via semantic token only | Surface colors changed when switching between Rich Editorial and Midnight. | No revision required. |
| Border changes between themes | Yes, via semantic token only | Border colors changed through the semantic border token when the alternate theme was activated. | No revision required. |
| Action / action-hover changes between themes | Yes, via semantic token only | Action styling changed from burgundy-based colors in Rich Editorial to rust-based colors in Midnight. | No revision required. |
| Focus changes between themes | Yes, via semantic token only | Focus styling remained clearly visible and changed according to the theme-specific focus token. | No revision required. |
| No duplicated component rules for theme | Confirmed by inspecting styles.css | Inspection of `styles.css` confirmed that the Midnight theme overrides semantic custom properties rather than duplicating component rules. | No revision required. |

## Typography

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| Libre Baskerville loads | Display headings render in Libre Baskerville | During normal page loading, the preferred display typography loaded and headings rendered using the intended Libre Baskerville stack. | No revision required. |
| Inter loads | Body text renders in Inter | During normal page loading, body typography rendered using the intended Inter stack. | No revision required. |
| Preferred font blocked (DevTools -> block Google Fonts request, hard reload) | Falls back to Georgia/Times New Roman/serif and Arial/Helvetica/sans-serif | Google-hosted `.woff2` font requests were blocked in DevTools with the browser cache disabled. The page continued rendering using the defined fallback stacks. | No revision required. |
| Fallback readability | Hierarchy and measure remain legible in fallback stack | With the preferred web fonts unavailable, headings and body text remained readable and the visual hierarchy and text measure remained usable. | No revision required. |

## Validation

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| HTML validation (validator.w3.org) | No errors | Final HTML validation reported: "Document checking completed. No errors or warnings to show." | Initial validation produced a heading-structure warning because the typography specimen contained an additional `h1`. The specimen heading was changed to the appropriate `h3` level. The document was validated again and returned no errors or warnings. |
| CSS validation (jigsaw.w3.org/css-validator) | No errors | W3C CSS Validator reported: "Congratulations! No Error Found." | No revision required. |

## Publication

| Condition | Expected | Observed | Revision |
|---|---|---|---|
| GitHub repository | Meaningful, incremental commits | Repository history contains incremental commits documenting implementation and revisions, including design-system CSS implementation, responsive overflow correction, HTML validator correction, and test-record updates. | No revision required. |
| GitHub Pages published | Site loads at published URL | The completed specimen loaded successfully from the published GitHub Pages URL. | No revision required. |
| Published site matches local specimen | No drift between local and deployed | The deployed specimen was compared with the locally tested version. Layout, content, component styling, typography, and theme behavior matched the local implementation. | No revision required. |
| All assets resolve | Fonts, CSS, and any images load with no 404s | Final published-site verification showed the specimen loading correctly with its CSS, typography, and page assets available. No missing assets were observed. | No revision required. |
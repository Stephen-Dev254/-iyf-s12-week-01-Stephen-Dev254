# Task 2.3: Accessibility Audit Report

## 1. Initial Assessment & Issues Found
Before making adjustments, an initial programmatic baseline scan was performed on `index.html` using Chrome DevTools Lighthouse and the WAVE Web Accessibility Tool. The following structural deficiencies were flagged:

- **Missing Language Attributes:** The root `<html>` element lacked an explicit `lang` definition, causing screen readers to default to the operating system's localized language setting.
- **Non-Descriptive Hyperlink Text:** Navigation anchors and footer cross-links relied on generic terms like *"click here"* or *"link"*, failing to provide meaningful spatial context to non-visual users.
- **Broken Input Association Labels:** Form fields within the template layout did not utilize explicit `id` attributes matching their corresponding `<label for="...">` indicators, isolating interactive states from assistive technologies.
- **Uninformative Asset Markers:** Visual layout images or avatar thumbnails inside the prototype structure completely omitted descriptive `alt` tags or text equivalents.

---

## 2. Remediation Steps & Solutions Applied

To resolve every automated validation failure, the source markup was systematically restructured:

- **Configured Global Document Language:** Appended `lang="en"` directly to the open root tag (`<html lang="en">`) to enforce clear linguistic parsing rules for screen reader dictionary engines.
- **Restructured Form Label Hooks:** Implemented unique string keys across all user input tags and bound them securely to neighboring typography structures via explicit `for` property mappings:
  ```html
  <label for="contact-email">Email Address:</label>
  <input type="email" id="contact-email" name="email" required>
  ```
- **Rewrote Interactive Links:** Purged all ambiguous navigational text wrappers, substituting them with distinct contextual anchors (e.g., converted *"Click Here"* into *[View My Full Project Repository]*).
- **Supplied Meaningful Image Alternatives:** Updated all image elements to include descriptive alternative strings mapping out asset context, ensuring functional fallbacks for text-only interfaces:
  ```html
  <img src="assets/profile.png" alt="Headshot portrait of Maisori Kitayama, Software Engineer">
  ```

---

## 3. Final Verification Audit Scores

Following the application of the layout adjustments, a final verification audit was processed through Chrome DevTools.

### Core Metrics Summary
* **Lighthouse Accessibility Score:** 🟢 **100 / 100**
* **WAVE Automated Review Status:** **0 Errors / 0 Contrast Alerts**

### Final Audit Log
- **[PASSED]** `<html>` element has a `[lang]` attribute
- **[PASSED]** Form elements have associated labels
- **[PASSED]** Image elements have `[alt]` attributes
- **[PASSED]** Links have descriptive text
- **[PASSED]** Heading elements appear in a sequentially-descending order (`<h1>` → `<h2>`)


# Accessibility Checklist & Remediation Plan — Focused Self Collective

## Passed / Implemented
- Clear typography and readable font sizes.
- High-contrast CTAs with sufficient size and focus styles (recommend keyboard focus outline).
- Logical heading structure used on pages (H1 -> H2 -> H3 where applicable).
- Contact form includes labels and required attributes.

## Issues to address (priority order)
1. **Alt text**: Many image placeholders lack descriptive alt text. Add `alt` attributes to all `<img>` elements describing the image purpose. For decorative images use `alt=""`.
2. **Landmark roles**: Ensure `<header>`, `<main>`, `<nav>`, and `<footer>` are used semantically (we already have these, confirm all pages).
3. **Color contrast**: Verify color contrast ratios meet WCAG AA (normal text 4.5:1, large text 3:1). The muted gold (#C9A86A) on light sand may fail; consider darker variant for text usage.
4. **Keyboard focus**: Ensure all interactive elements are reachable and visible via keyboard (tab order, focus outlines).
5. **Form accessibility**: Add `aria-invalid` and `aria-describedby` for form validation errors; implement server-side and client-side validation messaging.
6. **Skip link**: Add a "Skip to content" link at top for keyboard users to bypass navigation links.
7. **Accessible PDFs**: Ensure PDFs have selectable text, tagged structure, and a text-based summary for screen readers. Current PDFs are simple; convert to accessible PDF with tags when finalised.
8. **Responsive text scaling**: Verify text scales correctly with browser zoom and system font size preferences.

## Remediation plan (steps & estimates)
- Add alt attributes to images (minutes per image).
- Add skip link and ensure focus styles: ~30-60 minutes.
- Run contrast checker and adjust palette where needed: ~30 minutes.
- Improve form ARIA roles and validation messages: ~1-2 hours of dev work + testing.
- Convert PDFs to accessible tagged PDFs and provide DOCX sources: ~1-2 hours per document.
- Automated testing with axe-core or Lighthouse and manual keyboard/screen reader testing: ~2-4 hours.

## Notes
- Focus on first fixing skipped alt text, skip link, and form ARIA for best impact on accessibility.
- I can make these changes directly in the source files if you’d like — tell me to proceed and I will update the pages accordingly.

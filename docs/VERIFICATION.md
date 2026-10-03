# Verification record

[Overview](../README.md) · [Machine-readable evidence](verification.json)

Local reference checks ran on 2026-10-03 with **Node v22.16.0**. The machine-readable record contains the captured output rather than an invented transcript.

## Executable checks

Command: `node tools/check-site.mjs`. Exit code: **0**. Local asset references passed existence checks; this is not a behavioral unit-test suite.

Re-run from this repository with `npm test`. There are no external npm dependencies. The local preview can be started with npm start.

## Browser evidence

- No document horizontal overflow at 1200, 800, 500 and 320 CSS pixels
- First Tab exposes skip link; Enter transfers focus to main
- Flex layout handles long station name, uneven text and one remaining card

These checks ran in installed Microsoft Edge through a browser automation harness. No JavaScript page errors were observed. A representative screenshot is saved in images/preview.png. The harness was run from the parent workspace; the reproduction checklist below can be performed without installing that harness.

## Reproduce the important observation yourself

Inspect three cards, one card and a long unbroken heading at wide and narrow widths. Identify which computed properties belong to the parent and which to each card.

Record viewport, input, expected result and actual result. For interaction failures, verify that correcting the input produces a normal result and does not leave stale error styling or stale output. For a layout failure, distinguish document overflow from an intentionally scrollable table region.

## Limits

These observations cover the listed fixtures and one installed browser. They are not a full cross-browser, accessibility, production-security or performance audit. There is no real external service to validate. Static pages use a lightweight link check in CI; the manual/browser observations remain essential. New stories require new evidence after your changes.

The GitHub Actions workflow runs `npm test` on push and pull request. Its configuration is included; an actual remote success must be verified on GitHub separately. Do not infer it merely from this local report.

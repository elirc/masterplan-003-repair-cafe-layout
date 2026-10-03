# Rebuild Repair Cafe Layout through small verified slices

[Expanded workshop map](WORKBOOK-INDEX.md) · [Repository overview](../README.md)

This is a hypothetical reconstruction exercise using the existing reference as a comparison point. Work on a practice branch or a separate scratch copy. Do not erase the working reference. Your goal is to recover the important decisions from requirements, not reproduce every character or configuration file from memory.

## Session zero: write a contract you can challenge

Three repair stations wrap using Flexbox, cope with uneven descriptions and remain usable when only one station exists. The container owns distribution; individual cards own their internal vertical arrangement.

Your target skill is flexbox and content-driven layout. Write three examples before implementation: one ordinary success, one boundary distinction and one recovery or repeat sequence. Reuse the fixed reference fixtures only after making a prediction. If your new example is outside the documented scope, decide whether to reject it or explicitly expand the contract; do not let an incidental implementation choice decide silently.

Write a short non-goal list tied to this exercise. Non-goals keep an assistant from adding a database, a UI framework or a broad refactor before you understand the central rule. For static layout work, a meaningful non-goal may be scripting interactions that native HTML already handles. For stateful work, it may be remote persistence or a global state container.

## Slice 1: Identify the repeated unit

**Reference context:** Each station is an article with an opening time, heading, explanation and preparation note. Keep one understandable card working before copying the structure twice. Repetition is useful here because it exposes differences in content length. It is not a reason to introduce a component framework before you understand what repeats.

### Your implementation route

1. Inspect `public/style.css` and the related adapter `public/index.html and public/style.css`. Write which responsibility belongs to each for this slice. A path is a place to inspect, not automatic permission to edit every file.
2. State the example independently: **Three short cards at desktop width → Cards share available space**. Explain which requirement supplies the expected answer.
3. Build the smallest version that can express the example. Start with explicit data and direct control flow. Introduce a helper only when you can name its input, output and reason to change.
4. Observe the result through the real boundary: a command, a browser control, or a layout condition. A function returning the right value does not prove a button passes it the right input.
5. Add a neighboring example that would fail if you special-cased the first one. Review your diff before comparing with the reference.

### Pause at the first uncertainty

Write the smallest question you cannot answer. It might concern ownership, a comparison operator, the effect of deleting a property, or when a callback actually runs. Include the exact expression and an example. Ask a mentor for one clue, then return to the source; avoid requesting a complete replacement implementation.

### Inspect an alternative

Choose one plausible different design for this slice. Describe the extra state, dependency or maintenance rule it introduces. If it satisfies the same contract, it is not automatically wrong. Compare the cost of making the next small change. If it violates the contract, provide the smallest concrete example that demonstrates that violation.

### Capture a reviewable stopping point

Record your actual check: npm test (local asset references), plus the relevant browser/content observation. State what it established and what remains untested. Use a commit message about the resulting behavior rather than a list of file names. If the slice does not work yet, keep the uncertainty visible in the journal instead of writing a success narrative.

**Left for you:** the code, fixture values beyond the supplied example, exact naming and the acceptance evidence. The reference is available for comparison after an attempt; it is not evidence that your branch has passed.

## Slice 2: Give the parent a job

**Reference context:** The stations rule controls wrapping, gap and alignment. Its children express a preferred basis and permission to grow or shrink. Draw a row with three hypothetical 260px cards, then account for gaps and container width. This simple sketch predicts when wrapping should occur more reliably than guessing a device-specific breakpoint.

### Your implementation route

1. Inspect `public/style.css` and the related adapter `public/index.html and public/style.css`. Write which responsibility belongs to each for this slice. A path is a place to inspect, not automatic permission to edit every file.
2. State the example independently: **One very long heading at 320px → Text wraps inside the card**. Explain which requirement supplies the expected answer.
3. Build the smallest version that can express the example. Start with explicit data and direct control flow. Introduce a helper only when you can name its input, output and reason to change.
4. Observe the result through the real boundary: a command, a browser control, or a layout condition. A function returning the right value does not prove a button passes it the right input.
5. Add a neighboring example that would fail if you special-cased the first one. Review your diff before comparing with the reference.

### Pause at the first uncertainty

Write the smallest question you cannot answer. It might concern ownership, a comparison operator, the effect of deleting a property, or when a callback actually runs. Include the exact expression and an example. Ask a mentor for one clue, then return to the source; avoid requesting a complete replacement implementation.

### Inspect an alternative

Choose one plausible different design for this slice. Describe the extra state, dependency or maintenance rule it introduces. If it satisfies the same contract, it is not automatically wrong. Compare the cost of making the next small change. If it violates the contract, provide the smallest concrete example that demonstrates that violation.

### Capture a reviewable stopping point

Record your actual check: npm test (local asset references), plus the relevant browser/content observation. State what it established and what remains untested. Use a commit message about the resulting behavior rather than a list of file names. If the slice does not work yet, keep the uncertainty visible in the journal instead of writing a success narrative.

**Left for you:** the code, fixture values beyond the supplied example, exact naming and the acceptance evidence. The reference is available for comparison after an attempt; it is not evidence that your branch has passed.

## Slice 3: Give the child a separate job

**Reference context:** Each card is a column. The station note uses automatic top margin to consume spare vertical space after the description. Compare this with adding a fixed top margin: fixed spacing does not adapt when one description becomes much longer. If there is no spare room, auto margin does not manufacture it.

### Your implementation route

1. Inspect `public/style.css` and the related adapter `public/index.html and public/style.css`. Write which responsibility belongs to each for this slice. A path is a place to inspect, not automatic permission to edit every file.
2. State the example independently: **Only one card remains → It grows within the container instead of retaining an arbitrary fixed width**. Explain which requirement supplies the expected answer.
3. Build the smallest version that can express the example. Start with explicit data and direct control flow. Introduce a helper only when you can name its input, output and reason to change.
4. Observe the result through the real boundary: a command, a browser control, or a layout condition. A function returning the right value does not prove a button passes it the right input.
5. Add a neighboring example that would fail if you special-cased the first one. Review your diff before comparing with the reference.

### Pause at the first uncertainty

Write the smallest question you cannot answer. It might concern ownership, a comparison operator, the effect of deleting a property, or when a callback actually runs. Include the exact expression and an example. Ask a mentor for one clue, then return to the source; avoid requesting a complete replacement implementation.

### Inspect an alternative

Choose one plausible different design for this slice. Describe the extra state, dependency or maintenance rule it introduces. If it satisfies the same contract, it is not automatically wrong. Compare the cost of making the next small change. If it violates the contract, provide the smallest concrete example that demonstrates that violation.

### Capture a reviewable stopping point

Record your actual check: npm test (local asset references), plus the relevant browser/content observation. State what it established and what remains untested. Use a commit message about the resulting behavior rather than a list of file names. If the slice does not work yet, keep the uncertainty visible in the journal instead of writing a success narrative.

**Left for you:** the code, fixture values beyond the supplied example, exact naming and the acceptance evidence. The reference is available for comparison after an attempt; it is not evidence that your branch has passed.

## Slice 4: Disturb the ideal example

**Reference context:** Remove two cards in browser developer tools, make one heading an unbroken string, and increase one description. The learning target is resilience under changing content, not matching a single screenshot. The saved reference remains unchanged by these temporary probes. Use the evidence notes to distinguish those runtime probes from source changes you commit yourself.

### Your implementation route

1. Inspect `public/style.css` and the related adapter `public/index.html and public/style.css`. Write which responsibility belongs to each for this slice. A path is a place to inspect, not automatic permission to edit every file.
2. State the example independently: **Uneven descriptions → Notes remain separated from descriptions**. Explain which requirement supplies the expected answer.
3. Build the smallest version that can express the example. Start with explicit data and direct control flow. Introduce a helper only when you can name its input, output and reason to change.
4. Observe the result through the real boundary: a command, a browser control, or a layout condition. A function returning the right value does not prove a button passes it the right input.
5. Add a neighboring example that would fail if you special-cased the first one. Review your diff before comparing with the reference.

### Pause at the first uncertainty

Write the smallest question you cannot answer. It might concern ownership, a comparison operator, the effect of deleting a property, or when a callback actually runs. Include the exact expression and an example. Ask a mentor for one clue, then return to the source; avoid requesting a complete replacement implementation.

### Inspect an alternative

Choose one plausible different design for this slice. Describe the extra state, dependency or maintenance rule it introduces. If it satisfies the same contract, it is not automatically wrong. Compare the cost of making the next small change. If it violates the contract, provide the smallest concrete example that demonstrates that violation.

### Capture a reviewable stopping point

Record your actual check: npm test (local asset references), plus the relevant browser/content observation. State what it established and what remains untested. Use a commit message about the resulting behavior rather than a list of file names. If the slice does not work yet, keep the uncertainty visible in the journal instead of writing a success narrative.

**Left for you:** the code, fixture values beyond the supplied example, exact naming and the acceptance evidence. The reference is available for comparison after an attempt; it is not evidence that your branch has passed.

## Reconstruct the whole path without the guide

The stations container becomes a wrapping flex row → each card starts with a 260px basis → available room controls growth and wrapping → each card is also a column → margin-top:auto pushes its station note toward the bottom.

Close this page and redraw that route from memory using your own labels. Open the code only to resolve a specific uncertainty. Then trace a different valid input and one boundary. If your picture requires a hidden value that you cannot locate in the source, investigate it; diagrams can invent state just as easily as prose can.

## Compare your implementation fairly

First compare behavior and evidence. Only then compare style and abstractions. A shorter implementation may be harder for you to explain; a longer implementation may duplicate a rule that later drifts. State the concrete tradeoff. Do not treat matching the reference line for line as the only successful outcome.

## Finish with a teach-back

Explain why `.stations and .station-note` is enough for its present responsibility, which work remains in `public/index.html and public/style.css`, and which future requirement would justify changing that boundary. Answer the original transfer question: Which property belongs on the container and which belongs on a card? Keep the answer short enough that another junior can challenge it with an example.

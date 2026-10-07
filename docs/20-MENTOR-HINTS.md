# M003: mentor hints and answer directions

[Expanded workshop map](WORKBOOK-INDEX.md) · [Repository overview](../README.md)

Use this chapter after making an attempt. It provides reasoning directions and evaluation criteria, not finished feature patches. A learner can choose a different design when the revised contract is explicit and the evidence supports it.

## Retrieval card 01: answer direction

**Question:** Explain flex basis through this project

The preferred starting size used by flex layout.

Look for a concrete connection to `public/style.css` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 02: answer direction

**Question:** Explain free space through this project

Room available after content and sizing constraints.

Look for a concrete connection to `public/style.css` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 03: answer direction

**Question:** Explain intrinsic minimum through this project

Content-driven sizing that can resist shrinking.

Look for a concrete connection to `public/style.css` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 04: answer direction

**Question:** Explain container responsibility through this project

A rule governing relationships among children.

Look for a concrete connection to `public/style.css` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 05: answer direction

**Question:** Predict: Three short cards at desktop width

Cards share available space

Look for a concrete connection to `public/style.css` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 06: answer direction

**Question:** Predict: One very long heading at 320px

Text wraps inside the card

Look for a concrete connection to `public/style.css` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 07: answer direction

**Question:** Predict: Only one card remains

It grows within the container instead of retaining an arbitrary fixed width

Look for a concrete connection to `public/style.css` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 08: answer direction

**Question:** Explain why the container owns wrapping instead of each individual card.

flex-wrap lets the browser move a card when the available space no longer supports the preferred basis. A separate breakpoint for every possible card count would be harder to maintain.

Look for a concrete connection to `public/style.css` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 09: answer direction

**Question:** Find the difference between a preferred flex basis and a rigid width.

min-width:0 and overflow-wrap:anywhere protect the layout from a long unbroken label. The content should remain visible, rather than force the whole page wider.

Look for a concrete connection to `public/style.css` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 10: answer direction

**Question:** Explain why margin-top:auto works only when there is free space to absorb.

The outer row distributes cards. Each card’s own column layout separates its description and bottom note. These are two different layout problems, even though both use Flexbox.

Look for a concrete connection to `public/style.css` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 11: answer direction

**Question:** What does your strongest check not prove?

Use the scope recorded in VERIFICATION.md; do not infer production readiness from a small local fixture.

Look for a concrete connection to `public/style.css` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 12: answer direction

**Question:** Which property belongs on the container and which belongs on a card?

There are two layout owners. The station container decides how cards share and wrap across a row; each card decides how its own description and preparation note stack. A change to one owner should not be disguised as a magic margin on the other. Stressing card count and text length exposes whether those responsibilities are really separate.

Look for a concrete connection to `public/style.css` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Story 07: Add a tools-available line

**First hint:** The desired improvement is “Show shared equipment per station.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Add a short semantic list inside a card; allow wrapping; compare cards with one and many tools. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: Equipment text never forces fixed heights or hides the preparation note. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose the list presentation. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 08: Add a beginner-friendly label

**First hint:** The desired improvement is “Help visitors choose a station.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Add a textual skill label; style it consistently; inspect layout without color and with long text. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: Every label stays readable and card wrapping is unchanged. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose the allowed label vocabulary. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 09: Support a missing preparation note

**First hint:** The desired improvement is “Handle incomplete optional content honestly.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Create a fixture without a note; inspect the column layout; choose an explicit absent-note policy. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: No empty decorative block is mistaken for missing required instructions. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose omission or a short fallback. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 10: Add a station contact link

**First hint:** The desired improvement is “Provide a descriptive route to ask about one station.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Place the link in the card's reading order; keep purpose specific; inspect focus when cards wrap. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: Links remain reachable in source order at wide and narrow widths. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose where contact belongs within each card. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 11: Compare gap with margins

**First hint:** The desired improvement is “Learn which element owns inter-card spacing.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Build a scratch margin-based variant; calculate outer-edge effects; compare it with container gap. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: The worksheet explains both internal spacing and the container edges. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose a fixture width that reveals the difference. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 12: Add a text-only status key

**First hint:** The desired improvement is “Explain labels such as open or full.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Create a small key before the cards; reuse exact status words; keep meanings independent of color. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: A reader can interpret a card without seeing its badge color. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose two useful fictional statuses. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 13: Create a five-card fixture

**First hint:** The desired improvement is “Probe wrapping beyond a single neat row.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Add two uneven cards in a practice page; inspect the final row; compare grow behavior with earlier rows. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: The last row is readable and no card depends on its numerical position. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose the final-row growth policy. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 14: Add print-specific spacing

**First hint:** The desired improvement is “Make the station list readable on paper.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Inspect print preview first; reduce unnecessary decorative space; preserve every station and time. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: Printing does not crop a note or require background colors to explain state. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose acceptable page breaks. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 15: Document layout ownership

**First hint:** The desired improvement is “Help a reviewer change one layout concern at a time.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Annotate outer and inner flex rules in a worksheet; propose one change per owner; predict interactions. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: Each explanation names a concrete property and the box it affects. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose an example where both owners matter. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Mentor feedback rubric

| Dimension | Beginning | Developing | Independent evidence |
|---|---|---|---|
| Trace | Names files only | Follows one ordinary case | Predicts a new boundary and explains its owner |
| Test design | Copies output | Uses a stated expectation | Rejects a plausible wrong candidate |
| Design | Repeats a slogan | Names an alternative | Compares costs using a concrete change |
| Agent use | Accepts a generated answer | Checks suggested edits | Supplies own proposal and adjudicates critiques |
| Handoff | Claims it works | Lists actual checks | Explains behavior, evidence and limits coherently |

Use the rubric to choose the next practice action, not to label yourself permanently. A learner may be independent at source tracing and still need help designing a failure case. Target the missing skill with one smaller exercise.

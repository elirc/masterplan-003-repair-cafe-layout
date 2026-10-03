# Hints and answer directions

[Return to the stories](05-PRACTICE-STORIES.md)

There are intentionally no complete feature patches here. Use one hint, return to your code and produce evidence. Your design can differ from the reference when you state and verify the new contract.

## Story 01: Add a fourth station

**Hint 1 — ownership:** Begin from `.stations and .station-note`. Add one station using the same semantic structure and no special width.

**Hint 2 — reasoning:** Revisit the decision “Use a wrapping container”. Ask yourself: Explain why the container owns wrapping instead of each individual card.

**Answer direction:** A defensible solution demonstrates this observable result: It wraps naturally at all inspected widths. The exact code is not prescribed. If your change achieves that result by changing an unrelated original rule, revise either the implementation or the story contract explicitly.

**Self-review:** Could the UI or helper appear correct while the underlying rule remains wrong? Could the underlying calculation be correct while stale presentation misleads the user? Choose the question that applies and write one distinguishing example.

## Story 02: Add a closed-state label

**Hint 1 — ownership:** Begin from `.stations and .station-note`. Represent a closed station with text as well as a visual style.

**Hint 2 — reasoning:** Revisit the decision “Allow cards to shrink”. Ask yourself: Find the difference between a preferred flex basis and a rigid width.

**Answer direction:** A defensible solution demonstrates this observable result: Its state is understandable without color and its card still participates in layout. The exact code is not prescribed. If your change achieves that result by changing an unrelated original rule, revise either the implementation or the story contract explicitly.

**Self-review:** Could the UI or helper appear correct while the underlying rule remains wrong? Could the underlying calculation be correct while stale presentation misleads the user? Choose the question that applies and write one distinguishing example.

## Story 03: Test the single-station day

**Hint 1 — ownership:** Begin from `.stations and .station-note`. Create a separate fixture page or documented developer-tools procedure containing one station.

**Hint 2 — reasoning:** Revisit the decision “Use nested layout for a different responsibility”. Ask yourself: Explain why margin-top:auto works only when there is free space to absorb.

**Answer direction:** A defensible solution demonstrates this observable result: The remaining card is readable and does not cause overflow. The exact code is not prescribed. If your change achieves that result by changing an unrelated original rule, revise either the implementation or the story contract explicitly.

**Self-review:** Could the UI or helper appear correct while the underlying rule remains wrong? Could the underlying calculation be correct while stale presentation misleads the user? Choose the question that applies and write one distinguishing example.

## Story 04: Improve time semantics

**Hint 1 — ownership:** Begin from `.stations and .station-note`. Wrap opening and closing times in appropriate time elements.

**Hint 2 — reasoning:** Revisit the decision “Use a wrapping container”. Ask yourself: Explain why the container owns wrapping instead of each individual card.

**Answer direction:** A defensible solution demonstrates this observable result: The visible time is clear and machine-readable values match it. The exact code is not prescribed. If your change achieves that result by changing an unrelated original rule, revise either the implementation or the story contract explicitly.

**Self-review:** Could the UI or helper appear correct while the underlying rule remains wrong? Could the underlying calculation be correct while stale presentation misleads the user? Choose the question that applies and write one distinguishing example.

## Story 05: Tune spacing without changing behavior

**Hint 1 — ownership:** Begin from `.stations and .station-note`. Change the gap and card padding, then compare the wrapping point.

**Hint 2 — reasoning:** Revisit the decision “Allow cards to shrink”. Ask yourself: Find the difference between a preferred flex basis and a rigid width.

**Answer direction:** A defensible solution demonstrates this observable result: Your explanation accounts for both card widths and inter-card space. The exact code is not prescribed. If your change achieves that result by changing an unrelated original rule, revise either the implementation or the story contract explicitly.

**Self-review:** Could the UI or helper appear correct while the underlying rule remains wrong? Could the underlying calculation be correct while stale presentation misleads the user? Choose the question that applies and write one distinguishing example.

## Story 06: Create a content stress fixture

**Hint 1 — ownership:** Begin from `.stations and .station-note`. Add one intentionally long but readable description in a practice branch.

**Hint 2 — reasoning:** Revisit the decision “Use nested layout for a different responsibility”. Ask yourself: Explain why margin-top:auto works only when there is free space to absorb.

**Answer direction:** A defensible solution demonstrates this observable result: The page handles uneven content without fixed card heights or clipped text. The exact code is not prescribed. If your change achieves that result by changing an unrelated original rule, revise either the implementation or the story contract explicitly.

**Self-review:** Could the UI or helper appear correct while the underlying rule remains wrong? Could the underlying calculation be correct while stale presentation misleads the user? Choose the question that applies and write one distinguishing example.

## Answers to the trace questions

The stations container becomes a wrapping flex row → each card starts with a 260px basis → available room controls growth and wrapping → each card is also a column → margin-top:auto pushes its station note toward the bottom.

The expected examples are in the concepts table. Use them to check your reasoning, then supply a new example of your own. A copied sentence is not evidence that you can trace a changed input.

## When to ask for more help

Ask after you can show a concrete attempt, a specific uncertainty and an observation. Request a smaller hint before a full patch. If you do accept generated code, explain each changed line and run a counterexample you chose independently.

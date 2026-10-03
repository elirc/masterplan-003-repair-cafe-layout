# M003: practice stories 07–15

[Expanded workshop map](WORKBOOK-INDEX.md) · [Repository overview](../README.md)

These nine proposals extend the original six stories. They are intentionally not implemented in the reference. Each plan gives you boundaries and a route, while leaving the actual patch, exact fixtures and a product decision to you. Start with one story; do not bundle all nine into a single difficult-to-review change.

## Story 07: Add a tools-available line

**User story:** As a user or learner of Repair Cafe Layout, I want to show shared equipment per station so I can use or explain the behavior with less uncertainty.

**Acceptance contract:** Equipment text never forces fixed heights or hides the preparation note.

**Decision you own:** Choose the list presentation. Write your answer before implementation. Different answers can be valid when they produce a clear, verified contract.

### 1. Define the smallest complete change

Read `public/style.css` and trace `.stations and .station-note` once. Then inspect `public/index.html and public/style.css` to determine where this feature enters and becomes visible. Write a two-sentence scope: the new outcome and one adjacent feature you are deliberately leaving for later. Avoid inventing an endpoint, framework or storage mechanism unless this story explicitly needs it.

### 2. Write examples before editing

Create three rows in your journal: ordinary use, a boundary or missing input, and a repeat/recovery sequence. The required observation is: **Equipment text never forces fixed heights or hides the preparation note.** Give each row exact starting data, the user action and expected retained state. If this is a documentation or layout task, use observable content and keyboard/viewport conditions rather than a meaningless unit test of a sentence.

### 3. Implement in this order

1. **Add a short semantic list inside a card.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
2. **Allow wrapping.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
3. **Compare cards with one and many tools.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.

After those steps, remove any experimental code that no longer serves the contract. Do not remove a guard merely because the first happy-path example passes. Explain every new stored value: what event changes it, who owns it and whether it could instead be derived from existing information.

### 4. Challenge the first implementation

Propose a plausible incorrect version that would look successful in an easy demo but violate “Equipment text never forces fixed heights or hides the preparation note.” Choose one input or interaction that distinguishes it from your intended result. This counterexample is the basis for a useful regression or manual acceptance check. A second ordinary screenshot is less useful if it cannot reject the wrong version.

### 5. Review and hand off

Use npm test (local asset references), plus the relevant browser/content observation. Inspect the exact changed files and verify that the original contract still holds for one neighboring case. Record the actual commands or browser steps and their output. The reference verification document belongs to the supplied implementation; it cannot certify your new story before you run fresh checks.

Write the handoff in four lines: trigger, resulting behavior, evidence and remaining limitation. Include the design decision you made and the reason. If an assistant suggested the patch, identify which part you independently explained and checked. Keep your personal journal in the ignored my-journal folder.

### Saved prompt: request a challenge, not a solution

```text
I am implementing story 07: Add a tools-available line in Repair Cafe Layout.
Acceptance requirement: Equipment text never forces fixed heights or hides the preparation note.
My unresolved choice: Choose the list presentation.
My proposed decision, example and smallest diff: [fill these in].
Challenge one assumption and propose one discriminating example.
Do not implement the feature or claim any tests were run.
```

**Completion gate:** you can explain the changed behavior without reading the patch, reproduce the acceptance example, show one boundary check and name a limitation. The story remains unfinished until you supply that evidence.

## Story 08: Add a beginner-friendly label

**User story:** As a user or learner of Repair Cafe Layout, I want to help visitors choose a station so I can use or explain the behavior with less uncertainty.

**Acceptance contract:** Every label stays readable and card wrapping is unchanged.

**Decision you own:** Choose the allowed label vocabulary. Write your answer before implementation. Different answers can be valid when they produce a clear, verified contract.

### 1. Define the smallest complete change

Read `public/style.css` and trace `.stations and .station-note` once. Then inspect `public/index.html and public/style.css` to determine where this feature enters and becomes visible. Write a two-sentence scope: the new outcome and one adjacent feature you are deliberately leaving for later. Avoid inventing an endpoint, framework or storage mechanism unless this story explicitly needs it.

### 2. Write examples before editing

Create three rows in your journal: ordinary use, a boundary or missing input, and a repeat/recovery sequence. The required observation is: **Every label stays readable and card wrapping is unchanged.** Give each row exact starting data, the user action and expected retained state. If this is a documentation or layout task, use observable content and keyboard/viewport conditions rather than a meaningless unit test of a sentence.

### 3. Implement in this order

1. **Add a textual skill label.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
2. **Style it consistently.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
3. **Inspect layout without color and with long text.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.

After those steps, remove any experimental code that no longer serves the contract. Do not remove a guard merely because the first happy-path example passes. Explain every new stored value: what event changes it, who owns it and whether it could instead be derived from existing information.

### 4. Challenge the first implementation

Propose a plausible incorrect version that would look successful in an easy demo but violate “Every label stays readable and card wrapping is unchanged.” Choose one input or interaction that distinguishes it from your intended result. This counterexample is the basis for a useful regression or manual acceptance check. A second ordinary screenshot is less useful if it cannot reject the wrong version.

### 5. Review and hand off

Use npm test (local asset references), plus the relevant browser/content observation. Inspect the exact changed files and verify that the original contract still holds for one neighboring case. Record the actual commands or browser steps and their output. The reference verification document belongs to the supplied implementation; it cannot certify your new story before you run fresh checks.

Write the handoff in four lines: trigger, resulting behavior, evidence and remaining limitation. Include the design decision you made and the reason. If an assistant suggested the patch, identify which part you independently explained and checked. Keep your personal journal in the ignored my-journal folder.

### Saved prompt: request a challenge, not a solution

```text
I am implementing story 08: Add a beginner-friendly label in Repair Cafe Layout.
Acceptance requirement: Every label stays readable and card wrapping is unchanged.
My unresolved choice: Choose the allowed label vocabulary.
My proposed decision, example and smallest diff: [fill these in].
Challenge one assumption and propose one discriminating example.
Do not implement the feature or claim any tests were run.
```

**Completion gate:** you can explain the changed behavior without reading the patch, reproduce the acceptance example, show one boundary check and name a limitation. The story remains unfinished until you supply that evidence.

## Story 09: Support a missing preparation note

**User story:** As a user or learner of Repair Cafe Layout, I want to handle incomplete optional content honestly so I can use or explain the behavior with less uncertainty.

**Acceptance contract:** No empty decorative block is mistaken for missing required instructions.

**Decision you own:** Choose omission or a short fallback. Write your answer before implementation. Different answers can be valid when they produce a clear, verified contract.

### 1. Define the smallest complete change

Read `public/style.css` and trace `.stations and .station-note` once. Then inspect `public/index.html and public/style.css` to determine where this feature enters and becomes visible. Write a two-sentence scope: the new outcome and one adjacent feature you are deliberately leaving for later. Avoid inventing an endpoint, framework or storage mechanism unless this story explicitly needs it.

### 2. Write examples before editing

Create three rows in your journal: ordinary use, a boundary or missing input, and a repeat/recovery sequence. The required observation is: **No empty decorative block is mistaken for missing required instructions.** Give each row exact starting data, the user action and expected retained state. If this is a documentation or layout task, use observable content and keyboard/viewport conditions rather than a meaningless unit test of a sentence.

### 3. Implement in this order

1. **Create a fixture without a note.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
2. **Inspect the column layout.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
3. **Choose an explicit absent-note policy.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.

After those steps, remove any experimental code that no longer serves the contract. Do not remove a guard merely because the first happy-path example passes. Explain every new stored value: what event changes it, who owns it and whether it could instead be derived from existing information.

### 4. Challenge the first implementation

Propose a plausible incorrect version that would look successful in an easy demo but violate “No empty decorative block is mistaken for missing required instructions.” Choose one input or interaction that distinguishes it from your intended result. This counterexample is the basis for a useful regression or manual acceptance check. A second ordinary screenshot is less useful if it cannot reject the wrong version.

### 5. Review and hand off

Use npm test (local asset references), plus the relevant browser/content observation. Inspect the exact changed files and verify that the original contract still holds for one neighboring case. Record the actual commands or browser steps and their output. The reference verification document belongs to the supplied implementation; it cannot certify your new story before you run fresh checks.

Write the handoff in four lines: trigger, resulting behavior, evidence and remaining limitation. Include the design decision you made and the reason. If an assistant suggested the patch, identify which part you independently explained and checked. Keep your personal journal in the ignored my-journal folder.

### Saved prompt: request a challenge, not a solution

```text
I am implementing story 09: Support a missing preparation note in Repair Cafe Layout.
Acceptance requirement: No empty decorative block is mistaken for missing required instructions.
My unresolved choice: Choose omission or a short fallback.
My proposed decision, example and smallest diff: [fill these in].
Challenge one assumption and propose one discriminating example.
Do not implement the feature or claim any tests were run.
```

**Completion gate:** you can explain the changed behavior without reading the patch, reproduce the acceptance example, show one boundary check and name a limitation. The story remains unfinished until you supply that evidence.

## Story 10: Add a station contact link

**User story:** As a user or learner of Repair Cafe Layout, I want to provide a descriptive route to ask about one station so I can use or explain the behavior with less uncertainty.

**Acceptance contract:** Links remain reachable in source order at wide and narrow widths.

**Decision you own:** Choose where contact belongs within each card. Write your answer before implementation. Different answers can be valid when they produce a clear, verified contract.

### 1. Define the smallest complete change

Read `public/style.css` and trace `.stations and .station-note` once. Then inspect `public/index.html and public/style.css` to determine where this feature enters and becomes visible. Write a two-sentence scope: the new outcome and one adjacent feature you are deliberately leaving for later. Avoid inventing an endpoint, framework or storage mechanism unless this story explicitly needs it.

### 2. Write examples before editing

Create three rows in your journal: ordinary use, a boundary or missing input, and a repeat/recovery sequence. The required observation is: **Links remain reachable in source order at wide and narrow widths.** Give each row exact starting data, the user action and expected retained state. If this is a documentation or layout task, use observable content and keyboard/viewport conditions rather than a meaningless unit test of a sentence.

### 3. Implement in this order

1. **Place the link in the card's reading order.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
2. **Keep purpose specific.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
3. **Inspect focus when cards wrap.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.

After those steps, remove any experimental code that no longer serves the contract. Do not remove a guard merely because the first happy-path example passes. Explain every new stored value: what event changes it, who owns it and whether it could instead be derived from existing information.

### 4. Challenge the first implementation

Propose a plausible incorrect version that would look successful in an easy demo but violate “Links remain reachable in source order at wide and narrow widths.” Choose one input or interaction that distinguishes it from your intended result. This counterexample is the basis for a useful regression or manual acceptance check. A second ordinary screenshot is less useful if it cannot reject the wrong version.

### 5. Review and hand off

Use npm test (local asset references), plus the relevant browser/content observation. Inspect the exact changed files and verify that the original contract still holds for one neighboring case. Record the actual commands or browser steps and their output. The reference verification document belongs to the supplied implementation; it cannot certify your new story before you run fresh checks.

Write the handoff in four lines: trigger, resulting behavior, evidence and remaining limitation. Include the design decision you made and the reason. If an assistant suggested the patch, identify which part you independently explained and checked. Keep your personal journal in the ignored my-journal folder.

### Saved prompt: request a challenge, not a solution

```text
I am implementing story 10: Add a station contact link in Repair Cafe Layout.
Acceptance requirement: Links remain reachable in source order at wide and narrow widths.
My unresolved choice: Choose where contact belongs within each card.
My proposed decision, example and smallest diff: [fill these in].
Challenge one assumption and propose one discriminating example.
Do not implement the feature or claim any tests were run.
```

**Completion gate:** you can explain the changed behavior without reading the patch, reproduce the acceptance example, show one boundary check and name a limitation. The story remains unfinished until you supply that evidence.

## Story 11: Compare gap with margins

**User story:** As a user or learner of Repair Cafe Layout, I want to learn which element owns inter-card spacing so I can use or explain the behavior with less uncertainty.

**Acceptance contract:** The worksheet explains both internal spacing and the container edges.

**Decision you own:** Choose a fixture width that reveals the difference. Write your answer before implementation. Different answers can be valid when they produce a clear, verified contract.

### 1. Define the smallest complete change

Read `public/style.css` and trace `.stations and .station-note` once. Then inspect `public/index.html and public/style.css` to determine where this feature enters and becomes visible. Write a two-sentence scope: the new outcome and one adjacent feature you are deliberately leaving for later. Avoid inventing an endpoint, framework or storage mechanism unless this story explicitly needs it.

### 2. Write examples before editing

Create three rows in your journal: ordinary use, a boundary or missing input, and a repeat/recovery sequence. The required observation is: **The worksheet explains both internal spacing and the container edges.** Give each row exact starting data, the user action and expected retained state. If this is a documentation or layout task, use observable content and keyboard/viewport conditions rather than a meaningless unit test of a sentence.

### 3. Implement in this order

1. **Build a scratch margin-based variant.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
2. **Calculate outer-edge effects.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
3. **Compare it with container gap.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.

After those steps, remove any experimental code that no longer serves the contract. Do not remove a guard merely because the first happy-path example passes. Explain every new stored value: what event changes it, who owns it and whether it could instead be derived from existing information.

### 4. Challenge the first implementation

Propose a plausible incorrect version that would look successful in an easy demo but violate “The worksheet explains both internal spacing and the container edges.” Choose one input or interaction that distinguishes it from your intended result. This counterexample is the basis for a useful regression or manual acceptance check. A second ordinary screenshot is less useful if it cannot reject the wrong version.

### 5. Review and hand off

Use npm test (local asset references), plus the relevant browser/content observation. Inspect the exact changed files and verify that the original contract still holds for one neighboring case. Record the actual commands or browser steps and their output. The reference verification document belongs to the supplied implementation; it cannot certify your new story before you run fresh checks.

Write the handoff in four lines: trigger, resulting behavior, evidence and remaining limitation. Include the design decision you made and the reason. If an assistant suggested the patch, identify which part you independently explained and checked. Keep your personal journal in the ignored my-journal folder.

### Saved prompt: request a challenge, not a solution

```text
I am implementing story 11: Compare gap with margins in Repair Cafe Layout.
Acceptance requirement: The worksheet explains both internal spacing and the container edges.
My unresolved choice: Choose a fixture width that reveals the difference.
My proposed decision, example and smallest diff: [fill these in].
Challenge one assumption and propose one discriminating example.
Do not implement the feature or claim any tests were run.
```

**Completion gate:** you can explain the changed behavior without reading the patch, reproduce the acceptance example, show one boundary check and name a limitation. The story remains unfinished until you supply that evidence.

## Story 12: Add a text-only status key

**User story:** As a user or learner of Repair Cafe Layout, I want to explain labels such as open or full so I can use or explain the behavior with less uncertainty.

**Acceptance contract:** A reader can interpret a card without seeing its badge color.

**Decision you own:** Choose two useful fictional statuses. Write your answer before implementation. Different answers can be valid when they produce a clear, verified contract.

### 1. Define the smallest complete change

Read `public/style.css` and trace `.stations and .station-note` once. Then inspect `public/index.html and public/style.css` to determine where this feature enters and becomes visible. Write a two-sentence scope: the new outcome and one adjacent feature you are deliberately leaving for later. Avoid inventing an endpoint, framework or storage mechanism unless this story explicitly needs it.

### 2. Write examples before editing

Create three rows in your journal: ordinary use, a boundary or missing input, and a repeat/recovery sequence. The required observation is: **A reader can interpret a card without seeing its badge color.** Give each row exact starting data, the user action and expected retained state. If this is a documentation or layout task, use observable content and keyboard/viewport conditions rather than a meaningless unit test of a sentence.

### 3. Implement in this order

1. **Create a small key before the cards.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
2. **Reuse exact status words.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
3. **Keep meanings independent of color.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.

After those steps, remove any experimental code that no longer serves the contract. Do not remove a guard merely because the first happy-path example passes. Explain every new stored value: what event changes it, who owns it and whether it could instead be derived from existing information.

### 4. Challenge the first implementation

Propose a plausible incorrect version that would look successful in an easy demo but violate “A reader can interpret a card without seeing its badge color.” Choose one input or interaction that distinguishes it from your intended result. This counterexample is the basis for a useful regression or manual acceptance check. A second ordinary screenshot is less useful if it cannot reject the wrong version.

### 5. Review and hand off

Use npm test (local asset references), plus the relevant browser/content observation. Inspect the exact changed files and verify that the original contract still holds for one neighboring case. Record the actual commands or browser steps and their output. The reference verification document belongs to the supplied implementation; it cannot certify your new story before you run fresh checks.

Write the handoff in four lines: trigger, resulting behavior, evidence and remaining limitation. Include the design decision you made and the reason. If an assistant suggested the patch, identify which part you independently explained and checked. Keep your personal journal in the ignored my-journal folder.

### Saved prompt: request a challenge, not a solution

```text
I am implementing story 12: Add a text-only status key in Repair Cafe Layout.
Acceptance requirement: A reader can interpret a card without seeing its badge color.
My unresolved choice: Choose two useful fictional statuses.
My proposed decision, example and smallest diff: [fill these in].
Challenge one assumption and propose one discriminating example.
Do not implement the feature or claim any tests were run.
```

**Completion gate:** you can explain the changed behavior without reading the patch, reproduce the acceptance example, show one boundary check and name a limitation. The story remains unfinished until you supply that evidence.

## Story 13: Create a five-card fixture

**User story:** As a user or learner of Repair Cafe Layout, I want to probe wrapping beyond a single neat row so I can use or explain the behavior with less uncertainty.

**Acceptance contract:** The last row is readable and no card depends on its numerical position.

**Decision you own:** Choose the final-row growth policy. Write your answer before implementation. Different answers can be valid when they produce a clear, verified contract.

### 1. Define the smallest complete change

Read `public/style.css` and trace `.stations and .station-note` once. Then inspect `public/index.html and public/style.css` to determine where this feature enters and becomes visible. Write a two-sentence scope: the new outcome and one adjacent feature you are deliberately leaving for later. Avoid inventing an endpoint, framework or storage mechanism unless this story explicitly needs it.

### 2. Write examples before editing

Create three rows in your journal: ordinary use, a boundary or missing input, and a repeat/recovery sequence. The required observation is: **The last row is readable and no card depends on its numerical position.** Give each row exact starting data, the user action and expected retained state. If this is a documentation or layout task, use observable content and keyboard/viewport conditions rather than a meaningless unit test of a sentence.

### 3. Implement in this order

1. **Add two uneven cards in a practice page.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
2. **Inspect the final row.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
3. **Compare grow behavior with earlier rows.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.

After those steps, remove any experimental code that no longer serves the contract. Do not remove a guard merely because the first happy-path example passes. Explain every new stored value: what event changes it, who owns it and whether it could instead be derived from existing information.

### 4. Challenge the first implementation

Propose a plausible incorrect version that would look successful in an easy demo but violate “The last row is readable and no card depends on its numerical position.” Choose one input or interaction that distinguishes it from your intended result. This counterexample is the basis for a useful regression or manual acceptance check. A second ordinary screenshot is less useful if it cannot reject the wrong version.

### 5. Review and hand off

Use npm test (local asset references), plus the relevant browser/content observation. Inspect the exact changed files and verify that the original contract still holds for one neighboring case. Record the actual commands or browser steps and their output. The reference verification document belongs to the supplied implementation; it cannot certify your new story before you run fresh checks.

Write the handoff in four lines: trigger, resulting behavior, evidence and remaining limitation. Include the design decision you made and the reason. If an assistant suggested the patch, identify which part you independently explained and checked. Keep your personal journal in the ignored my-journal folder.

### Saved prompt: request a challenge, not a solution

```text
I am implementing story 13: Create a five-card fixture in Repair Cafe Layout.
Acceptance requirement: The last row is readable and no card depends on its numerical position.
My unresolved choice: Choose the final-row growth policy.
My proposed decision, example and smallest diff: [fill these in].
Challenge one assumption and propose one discriminating example.
Do not implement the feature or claim any tests were run.
```

**Completion gate:** you can explain the changed behavior without reading the patch, reproduce the acceptance example, show one boundary check and name a limitation. The story remains unfinished until you supply that evidence.

## Story 14: Add print-specific spacing

**User story:** As a user or learner of Repair Cafe Layout, I want to make the station list readable on paper so I can use or explain the behavior with less uncertainty.

**Acceptance contract:** Printing does not crop a note or require background colors to explain state.

**Decision you own:** Choose acceptable page breaks. Write your answer before implementation. Different answers can be valid when they produce a clear, verified contract.

### 1. Define the smallest complete change

Read `public/style.css` and trace `.stations and .station-note` once. Then inspect `public/index.html and public/style.css` to determine where this feature enters and becomes visible. Write a two-sentence scope: the new outcome and one adjacent feature you are deliberately leaving for later. Avoid inventing an endpoint, framework or storage mechanism unless this story explicitly needs it.

### 2. Write examples before editing

Create three rows in your journal: ordinary use, a boundary or missing input, and a repeat/recovery sequence. The required observation is: **Printing does not crop a note or require background colors to explain state.** Give each row exact starting data, the user action and expected retained state. If this is a documentation or layout task, use observable content and keyboard/viewport conditions rather than a meaningless unit test of a sentence.

### 3. Implement in this order

1. **Inspect print preview first.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
2. **Reduce unnecessary decorative space.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
3. **Preserve every station and time.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.

After those steps, remove any experimental code that no longer serves the contract. Do not remove a guard merely because the first happy-path example passes. Explain every new stored value: what event changes it, who owns it and whether it could instead be derived from existing information.

### 4. Challenge the first implementation

Propose a plausible incorrect version that would look successful in an easy demo but violate “Printing does not crop a note or require background colors to explain state.” Choose one input or interaction that distinguishes it from your intended result. This counterexample is the basis for a useful regression or manual acceptance check. A second ordinary screenshot is less useful if it cannot reject the wrong version.

### 5. Review and hand off

Use npm test (local asset references), plus the relevant browser/content observation. Inspect the exact changed files and verify that the original contract still holds for one neighboring case. Record the actual commands or browser steps and their output. The reference verification document belongs to the supplied implementation; it cannot certify your new story before you run fresh checks.

Write the handoff in four lines: trigger, resulting behavior, evidence and remaining limitation. Include the design decision you made and the reason. If an assistant suggested the patch, identify which part you independently explained and checked. Keep your personal journal in the ignored my-journal folder.

### Saved prompt: request a challenge, not a solution

```text
I am implementing story 14: Add print-specific spacing in Repair Cafe Layout.
Acceptance requirement: Printing does not crop a note or require background colors to explain state.
My unresolved choice: Choose acceptable page breaks.
My proposed decision, example and smallest diff: [fill these in].
Challenge one assumption and propose one discriminating example.
Do not implement the feature or claim any tests were run.
```

**Completion gate:** you can explain the changed behavior without reading the patch, reproduce the acceptance example, show one boundary check and name a limitation. The story remains unfinished until you supply that evidence.

## Story 15: Document layout ownership

**User story:** As a user or learner of Repair Cafe Layout, I want to help a reviewer change one layout concern at a time so I can use or explain the behavior with less uncertainty.

**Acceptance contract:** Each explanation names a concrete property and the box it affects.

**Decision you own:** Choose an example where both owners matter. Write your answer before implementation. Different answers can be valid when they produce a clear, verified contract.

### 1. Define the smallest complete change

Read `public/style.css` and trace `.stations and .station-note` once. Then inspect `public/index.html and public/style.css` to determine where this feature enters and becomes visible. Write a two-sentence scope: the new outcome and one adjacent feature you are deliberately leaving for later. Avoid inventing an endpoint, framework or storage mechanism unless this story explicitly needs it.

### 2. Write examples before editing

Create three rows in your journal: ordinary use, a boundary or missing input, and a repeat/recovery sequence. The required observation is: **Each explanation names a concrete property and the box it affects.** Give each row exact starting data, the user action and expected retained state. If this is a documentation or layout task, use observable content and keyboard/viewport conditions rather than a meaningless unit test of a sentence.

### 3. Implement in this order

1. **Annotate outer and inner flex rules in a worksheet.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
2. **Propose one change per owner.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.
3. **Predict interactions.** Before proceeding, name the value or element this step owns and predict one visible consequence. Keep the step small enough to inspect in a diff.

After those steps, remove any experimental code that no longer serves the contract. Do not remove a guard merely because the first happy-path example passes. Explain every new stored value: what event changes it, who owns it and whether it could instead be derived from existing information.

### 4. Challenge the first implementation

Propose a plausible incorrect version that would look successful in an easy demo but violate “Each explanation names a concrete property and the box it affects.” Choose one input or interaction that distinguishes it from your intended result. This counterexample is the basis for a useful regression or manual acceptance check. A second ordinary screenshot is less useful if it cannot reject the wrong version.

### 5. Review and hand off

Use npm test (local asset references), plus the relevant browser/content observation. Inspect the exact changed files and verify that the original contract still holds for one neighboring case. Record the actual commands or browser steps and their output. The reference verification document belongs to the supplied implementation; it cannot certify your new story before you run fresh checks.

Write the handoff in four lines: trigger, resulting behavior, evidence and remaining limitation. Include the design decision you made and the reason. If an assistant suggested the patch, identify which part you independently explained and checked. Keep your personal journal in the ignored my-journal folder.

### Saved prompt: request a challenge, not a solution

```text
I am implementing story 15: Document layout ownership in Repair Cafe Layout.
Acceptance requirement: Each explanation names a concrete property and the box it affects.
My unresolved choice: Choose an example where both owners matter.
My proposed decision, example and smallest diff: [fill these in].
Challenge one assumption and propose one discriminating example.
Do not implement the feature or claim any tests were run.
```

**Completion gate:** you can explain the changed behavior without reading the patch, reproduce the acceptance example, show one boundary check and name a limitation. The story remains unfinished until you supply that evidence.

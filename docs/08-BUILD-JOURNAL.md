# Build journal: Repair Cafe Layout

[Code tour](03-CODE-TOUR.md) · [Actual verification](VERIFICATION.md)

This is a retrospective teaching narrative about the implementation in this repository. It is not a verbatim conversation, fabricated team debate or hidden chain-of-thought transcript. The design explanations below are reviewable rationales tied to the source. Dates and check results belong to the verification record.

## The starting problem

A volunteer needs to scan three repair stations and find each opening time.

The main temptation was to make the project larger than its learning target. The useful boundary is **flexbox and content-driven layout**. A finished small example lets you inspect the whole path and ask what each part contributes. Extra infrastructure would add more things to configure before the central idea became clear.

## The first contract

Three repair stations wrap using Flexbox, cope with uneven descriptions and remain usable when only one station exists. The container owns distribution; individual cards own their internal vertical arrangement.

The contract turned broad intent into examples that can disagree with an implementation. That matters because a plausible-looking result can hide a wrong boundary rule. The examples in the concepts guide were chosen to expose those distinctions, not to make the demo look flawless.

## Decision note 1: Use a wrapping container

flex-wrap lets the browser move a card when the available space no longer supports the preferred basis. A separate breakpoint for every possible card count would be harder to maintain.

**What a learner should challenge:** Explain why the container owns wrapping instead of each individual card.

**Evidence to consult:** inspect the owning source file, the contract examples and the verification scope. If your alternative satisfies the same behavior with a different structure, compare the maintenance cost instead of assuming one syntax is automatically correct.

## Decision note 2: Allow cards to shrink

min-width:0 and overflow-wrap:anywhere protect the layout from a long unbroken label. The content should remain visible, rather than force the whole page wider.

**What a learner should challenge:** Find the difference between a preferred flex basis and a rigid width.

**Evidence to consult:** inspect the owning source file, the contract examples and the verification scope. If your alternative satisfies the same behavior with a different structure, compare the maintenance cost instead of assuming one syntax is automatically correct.

## Decision note 3: Use nested layout for a different responsibility

The outer row distributes cards. Each card’s own column layout separates its description and bottom note. These are two different layout problems, even though both use Flexbox.

**What a learner should challenge:** Explain why margin-top:auto works only when there is free space to absorb.

**Evidence to consult:** inspect the owning source file, the contract examples and the verification scope. If your alternative satisfies the same behavior with a different structure, compare the maintenance cost instead of assuming one syntax is automatically correct.

## What the checks contributed

The static asset check caught missing local resources, while the browser checks exercised layout, keyboard entry and project-specific content changes. Neither check alone would justify a blanket accessibility claim.

The record in VERIFICATION.md reports actual local observations. A GitHub Actions workflow is provided, but its remote result must be inspected separately after a push. A screenshot documents one rendered state; it is not a substitute for the interaction and boundary checks.

## What you should do differently on your own build

Start from the same user need but write your own examples first. Choose a small variation from the story list. Predict behavior, implement a slice and compare the result with your prediction. The reference helps you judge a finished result; your journal should record your own uncertainties and discoveries rather than adopting this narrative as if you experienced it.

## The handoff

The next learner can start from README, locate `.stations and .station-note`, reproduce the example table and attempt one bounded story. That is the intended handoff quality: a working result plus enough evidence and explanation to continue safely. The six practice stories remain unfinished for the learner.

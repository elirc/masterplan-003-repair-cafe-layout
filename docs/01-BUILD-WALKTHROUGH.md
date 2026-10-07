# Building Repair Cafe Layout, one decision at a time

[Learning route](00-START-HERE.md) · [Code tour](03-CODE-TOUR.md)

This is a reconstruction of how to approach the finished reference. It explains visible design choices; it is not a transcript of hidden reasoning or a claim that a fictional team performed these steps.

## Start from the contract

Three repair stations wrap using Flexbox, cope with uneven descriptions and remain usable when only one station exists. The container owns distribution; individual cards own their internal vertical arrangement.

The smallest useful result answers this user need: A volunteer needs to scan three repair stations and find each opening time. Write the examples before choosing file names. Keep the scope small enough that the decisive behavior fits in one trace.

## Step 1: Identify the repeated unit

Each station is an article with an opening time, heading, explanation and preparation note. Keep one understandable card working before copying the structure twice. Repetition is useful here because it exposes differences in content length. It is not a reason to introduce a component framework before you understand what repeats.

**Pause and produce evidence:** Only one card remains. Predict the outcome, then compare it with the reference. In your notes, distinguish what the code says should happen from what you actually observed.

## Step 2: Give the parent a job

The stations rule controls wrapping, gap and alignment. Its children express a preferred basis and permission to grow or shrink. Draw a row with three hypothetical 260px cards, then account for gaps and container width. This simple sketch predicts when wrapping should occur more reliably than guessing a device-specific breakpoint.

**Pause and produce evidence:** Three short cards at desktop width. Predict the outcome, then compare it with the reference. In your notes, distinguish what the code says should happen from what you actually observed.

## Step 3: Give the child a separate job

Each card is a column. The station note uses automatic top margin to consume spare vertical space after the description. Compare this with adding a fixed top margin: fixed spacing does not adapt when one description becomes much longer. If there is no spare room, auto margin does not manufacture it.

**Pause and produce evidence:** Uneven descriptions. Predict the outcome, then compare it with the reference. In your notes, distinguish what the code says should happen from what you actually observed.

## Step 4: Disturb the ideal example

Remove two cards in browser developer tools, make one heading an unbroken string, and increase one description. The learning target is resilience under changing content, not matching a single screenshot. The saved reference remains unchanged by these temporary probes. Use the evidence notes to distinguish those runtime probes from source changes you commit yourself.

**Pause and produce evidence:** One very long heading at 320px. Predict the outcome, then compare it with the reference. In your notes, distinguish what the code says should happen from what you actually observed.

## Keep the implementation reviewable

A useful commit has one understandable reason to exist. Separate the initial working slice, the checks that expose its important boundaries, and the teaching material that explains it. The published commits in this repository were assembled from verified working files; they are real commits, not fabricated evidence of a long historical development process.

For your own variation, commit at a point where the behavior and evidence agree. Describe the trigger, the resulting behavior and the check in the commit message or review note. Avoid mixing a rule change with unrelated formatting because it makes the learning decision harder to see.

## Stop before adding a platform

The next useful improvement is a sharper example or clearer explanation, not a database, account system or framework migration. Add an abstraction only when it names a real repeated responsibility. You should be able to describe what becomes easier to change after the abstraction and what new complexity it introduces.

**Independent design choice from the original brief:** Decide where wrapping should occur and explain why.

The reference made one choice, documented in the code tour. You may choose differently in a branch if you first revise the contract and acceptance examples. A deliberate alternative is a stronger learning artifact than an unexplained copy.

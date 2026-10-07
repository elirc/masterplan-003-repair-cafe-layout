# Six junior practice stories

[Debugging lab](04-DEBUGGING-LAB.md) · [Hints — use after an attempt](06-HINTS-AND-ANSWERS.md)

These are new exercises beyond the finished reference. No story is marked complete for you. Start a branch such as practice/story-01 and write acceptance examples before editing. Each plan leaves the actual code, wording and one design choice to you.

## Story 01: Add a fourth station

**Feature boundary:** Add one station using the same semantic structure and no special width.

**Implementation plan:**

1. Trace `.stations and .station-note` and locate the smallest owning file from the code tour. Write how this story touches that responsibility.
2. Write a before/after example that demonstrates this acceptance requirement: It wraps naturally at all inspected widths.
3. Choose the input shape, wording or layout policy yourself. Record one alternative and the reason you did not choose it.
4. Implement only the bounded change. If it crosses files, explain what each file owns rather than copying the same decision into several places.
5. Reproduce the acceptance example and one existing boundary case. Add an automated regression for executable logic, or an explicit browser/keyboard/content observation for a static change.
6. Review the diff, explain the change without reading the solution, and record remaining limits.

**Acceptance evidence:** It wraps naturally at all inspected widths.

**Left for you:** exact fixture values, names, wording, the implementation and the tradeoff decision. Do not open the hints until you have an example and a first attempt.

**Stretch only after completion:** add one adversarial example that a plausible but incorrect solution would fail. Explain why that example is more informative than adding three ordinary examples.

## Story 02: Add a closed-state label

**Feature boundary:** Represent a closed station with text as well as a visual style.

**Implementation plan:**

1. Trace `.stations and .station-note` and locate the smallest owning file from the code tour. Write how this story touches that responsibility.
2. Write a before/after example that demonstrates this acceptance requirement: Its state is understandable without color and its card still participates in layout.
3. Choose the input shape, wording or layout policy yourself. Record one alternative and the reason you did not choose it.
4. Implement only the bounded change. If it crosses files, explain what each file owns rather than copying the same decision into several places.
5. Reproduce the acceptance example and one existing boundary case. Add an automated regression for executable logic, or an explicit browser/keyboard/content observation for a static change.
6. Review the diff, explain the change without reading the solution, and record remaining limits.

**Acceptance evidence:** Its state is understandable without color and its card still participates in layout.

**Left for you:** exact fixture values, names, wording, the implementation and the tradeoff decision. Do not open the hints until you have an example and a first attempt.

**Stretch only after completion:** add one adversarial example that a plausible but incorrect solution would fail. Explain why that example is more informative than adding three ordinary examples.

## Story 03: Test the single-station day

**Feature boundary:** Create a separate fixture page or documented developer-tools procedure containing one station.

**Implementation plan:**

1. Trace `.stations and .station-note` and locate the smallest owning file from the code tour. Write how this story touches that responsibility.
2. Write a before/after example that demonstrates this acceptance requirement: The remaining card is readable and does not cause overflow.
3. Choose the input shape, wording or layout policy yourself. Record one alternative and the reason you did not choose it.
4. Implement only the bounded change. If it crosses files, explain what each file owns rather than copying the same decision into several places.
5. Reproduce the acceptance example and one existing boundary case. Add an automated regression for executable logic, or an explicit browser/keyboard/content observation for a static change.
6. Review the diff, explain the change without reading the solution, and record remaining limits.

**Acceptance evidence:** The remaining card is readable and does not cause overflow.

**Left for you:** exact fixture values, names, wording, the implementation and the tradeoff decision. Do not open the hints until you have an example and a first attempt.

**Stretch only after completion:** add one adversarial example that a plausible but incorrect solution would fail. Explain why that example is more informative than adding three ordinary examples.

## Story 04: Improve time semantics

**Feature boundary:** Wrap opening and closing times in appropriate time elements.

**Implementation plan:**

1. Trace `.stations and .station-note` and locate the smallest owning file from the code tour. Write how this story touches that responsibility.
2. Write a before/after example that demonstrates this acceptance requirement: The visible time is clear and machine-readable values match it.
3. Choose the input shape, wording or layout policy yourself. Record one alternative and the reason you did not choose it.
4. Implement only the bounded change. If it crosses files, explain what each file owns rather than copying the same decision into several places.
5. Reproduce the acceptance example and one existing boundary case. Add an automated regression for executable logic, or an explicit browser/keyboard/content observation for a static change.
6. Review the diff, explain the change without reading the solution, and record remaining limits.

**Acceptance evidence:** The visible time is clear and machine-readable values match it.

**Left for you:** exact fixture values, names, wording, the implementation and the tradeoff decision. Do not open the hints until you have an example and a first attempt.

**Stretch only after completion:** add one adversarial example that a plausible but incorrect solution would fail. Explain why that example is more informative than adding three ordinary examples.

## Story 05: Tune spacing without changing behavior

**Feature boundary:** Change the gap and card padding, then compare the wrapping point.

**Implementation plan:**

1. Trace `.stations and .station-note` and locate the smallest owning file from the code tour. Write how this story touches that responsibility.
2. Write a before/after example that demonstrates this acceptance requirement: Your explanation accounts for both card widths and inter-card space.
3. Choose the input shape, wording or layout policy yourself. Record one alternative and the reason you did not choose it.
4. Implement only the bounded change. If it crosses files, explain what each file owns rather than copying the same decision into several places.
5. Reproduce the acceptance example and one existing boundary case. Add an automated regression for executable logic, or an explicit browser/keyboard/content observation for a static change.
6. Review the diff, explain the change without reading the solution, and record remaining limits.

**Acceptance evidence:** Your explanation accounts for both card widths and inter-card space.

**Left for you:** exact fixture values, names, wording, the implementation and the tradeoff decision. Do not open the hints until you have an example and a first attempt.

**Stretch only after completion:** add one adversarial example that a plausible but incorrect solution would fail. Explain why that example is more informative than adding three ordinary examples.

## Story 06: Create a content stress fixture

**Feature boundary:** Add one intentionally long but readable description in a practice branch.

**Implementation plan:**

1. Trace `.stations and .station-note` and locate the smallest owning file from the code tour. Write how this story touches that responsibility.
2. Write a before/after example that demonstrates this acceptance requirement: The page handles uneven content without fixed card heights or clipped text.
3. Choose the input shape, wording or layout policy yourself. Record one alternative and the reason you did not choose it.
4. Implement only the bounded change. If it crosses files, explain what each file owns rather than copying the same decision into several places.
5. Reproduce the acceptance example and one existing boundary case. Add an automated regression for executable logic, or an explicit browser/keyboard/content observation for a static change.
6. Review the diff, explain the change without reading the solution, and record remaining limits.

**Acceptance evidence:** The page handles uneven content without fixed card heights or clipped text.

**Left for you:** exact fixture values, names, wording, the implementation and the tradeoff decision. Do not open the hints until you have an example and a first attempt.

**Stretch only after completion:** add one adversarial example that a plausible but incorrect solution would fail. Explain why that example is more informative than adding three ordinary examples.

<!-- expanded-story-clinics -->

## Additional planning checkpoints for stories 01–06

[Nine more stories, 07–15](11-NINE-MORE-STORIES.md) · [Expanded workshop map](WORKBOOK-INDEX.md)

Keep the original plans above. The following checkpoints add implementation and review depth without completing the exercise for you.

### Story 01 planning clinic: Add a fourth station

**Before editing:** restate the boundary in your own words: Add one station using the same semantic structure and no special width. Identify the part of `public/style.css` or `public/index.html and public/style.css` that owns it. If your proposed design changes another owner, explain the dependency instead of opening every file for a broad rewrite.

**Acceptance matrix:** write ordinary, boundary and repeat/recovery rows that establish “It wraps naturally at all inspected widths.” Include exact starting data or content and the expected retained information. Calculate expected values or inspect meaningful source order independently of the proposed implementation.

**First implementation slice:** make only enough of the change to demonstrate one acceptance row. Inspect the diff and predict the next row before running it. If your first slice is mostly setup or abstraction with no observable result, consider a smaller direct route.

**Review challenge:** sketch a plausible wrong solution that would pass a casual demonstration. Choose a counterexample that exposes its specific weakness. Ask an assistant to critique that example rather than immediately asking it to finish the entire feature.

**Evidence and explanation:** use npm test (local asset references), plus the relevant browser/content observation. Record the actual observation and the limit of the check. Finish by naming a design decision you made yourself and explaining why the neighboring original behavior still holds.

### Story 02 planning clinic: Add a closed-state label

**Before editing:** restate the boundary in your own words: Represent a closed station with text as well as a visual style. Identify the part of `public/style.css` or `public/index.html and public/style.css` that owns it. If your proposed design changes another owner, explain the dependency instead of opening every file for a broad rewrite.

**Acceptance matrix:** write ordinary, boundary and repeat/recovery rows that establish “Its state is understandable without color and its card still participates in layout.” Include exact starting data or content and the expected retained information. Calculate expected values or inspect meaningful source order independently of the proposed implementation.

**First implementation slice:** make only enough of the change to demonstrate one acceptance row. Inspect the diff and predict the next row before running it. If your first slice is mostly setup or abstraction with no observable result, consider a smaller direct route.

**Review challenge:** sketch a plausible wrong solution that would pass a casual demonstration. Choose a counterexample that exposes its specific weakness. Ask an assistant to critique that example rather than immediately asking it to finish the entire feature.

**Evidence and explanation:** use npm test (local asset references), plus the relevant browser/content observation. Record the actual observation and the limit of the check. Finish by naming a design decision you made yourself and explaining why the neighboring original behavior still holds.

### Story 03 planning clinic: Test the single-station day

**Before editing:** restate the boundary in your own words: Create a separate fixture page or documented developer-tools procedure containing one station. Identify the part of `public/style.css` or `public/index.html and public/style.css` that owns it. If your proposed design changes another owner, explain the dependency instead of opening every file for a broad rewrite.

**Acceptance matrix:** write ordinary, boundary and repeat/recovery rows that establish “The remaining card is readable and does not cause overflow.” Include exact starting data or content and the expected retained information. Calculate expected values or inspect meaningful source order independently of the proposed implementation.

**First implementation slice:** make only enough of the change to demonstrate one acceptance row. Inspect the diff and predict the next row before running it. If your first slice is mostly setup or abstraction with no observable result, consider a smaller direct route.

**Review challenge:** sketch a plausible wrong solution that would pass a casual demonstration. Choose a counterexample that exposes its specific weakness. Ask an assistant to critique that example rather than immediately asking it to finish the entire feature.

**Evidence and explanation:** use npm test (local asset references), plus the relevant browser/content observation. Record the actual observation and the limit of the check. Finish by naming a design decision you made yourself and explaining why the neighboring original behavior still holds.

### Story 04 planning clinic: Improve time semantics

**Before editing:** restate the boundary in your own words: Wrap opening and closing times in appropriate time elements. Identify the part of `public/style.css` or `public/index.html and public/style.css` that owns it. If your proposed design changes another owner, explain the dependency instead of opening every file for a broad rewrite.

**Acceptance matrix:** write ordinary, boundary and repeat/recovery rows that establish “The visible time is clear and machine-readable values match it.” Include exact starting data or content and the expected retained information. Calculate expected values or inspect meaningful source order independently of the proposed implementation.

**First implementation slice:** make only enough of the change to demonstrate one acceptance row. Inspect the diff and predict the next row before running it. If your first slice is mostly setup or abstraction with no observable result, consider a smaller direct route.

**Review challenge:** sketch a plausible wrong solution that would pass a casual demonstration. Choose a counterexample that exposes its specific weakness. Ask an assistant to critique that example rather than immediately asking it to finish the entire feature.

**Evidence and explanation:** use npm test (local asset references), plus the relevant browser/content observation. Record the actual observation and the limit of the check. Finish by naming a design decision you made yourself and explaining why the neighboring original behavior still holds.

### Story 05 planning clinic: Tune spacing without changing behavior

**Before editing:** restate the boundary in your own words: Change the gap and card padding, then compare the wrapping point. Identify the part of `public/style.css` or `public/index.html and public/style.css` that owns it. If your proposed design changes another owner, explain the dependency instead of opening every file for a broad rewrite.

**Acceptance matrix:** write ordinary, boundary and repeat/recovery rows that establish “Your explanation accounts for both card widths and inter-card space.” Include exact starting data or content and the expected retained information. Calculate expected values or inspect meaningful source order independently of the proposed implementation.

**First implementation slice:** make only enough of the change to demonstrate one acceptance row. Inspect the diff and predict the next row before running it. If your first slice is mostly setup or abstraction with no observable result, consider a smaller direct route.

**Review challenge:** sketch a plausible wrong solution that would pass a casual demonstration. Choose a counterexample that exposes its specific weakness. Ask an assistant to critique that example rather than immediately asking it to finish the entire feature.

**Evidence and explanation:** use npm test (local asset references), plus the relevant browser/content observation. Record the actual observation and the limit of the check. Finish by naming a design decision you made yourself and explaining why the neighboring original behavior still holds.

### Story 06 planning clinic: Create a content stress fixture

**Before editing:** restate the boundary in your own words: Add one intentionally long but readable description in a practice branch. Identify the part of `public/style.css` or `public/index.html and public/style.css` that owns it. If your proposed design changes another owner, explain the dependency instead of opening every file for a broad rewrite.

**Acceptance matrix:** write ordinary, boundary and repeat/recovery rows that establish “The page handles uneven content without fixed card heights or clipped text.” Include exact starting data or content and the expected retained information. Calculate expected values or inspect meaningful source order independently of the proposed implementation.

**First implementation slice:** make only enough of the change to demonstrate one acceptance row. Inspect the diff and predict the next row before running it. If your first slice is mostly setup or abstraction with no observable result, consider a smaller direct route.

**Review challenge:** sketch a plausible wrong solution that would pass a casual demonstration. Choose a counterexample that exposes its specific weakness. Ask an assistant to critique that example rather than immediately asking it to finish the entire feature.

**Evidence and explanation:** use npm test (local asset references), plus the relevant browser/content observation. Record the actual observation and the limit of the check. Finish by naming a design decision you made yourself and explaining why the neighboring original behavior still holds.

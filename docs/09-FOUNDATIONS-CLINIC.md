# M003: foundations clinic

[Expanded workshop map](WORKBOOK-INDEX.md) · [Repository overview](../README.md)

There are two layout owners. The station container decides how cards share and wrap across a row; each card decides how its own description and preparation note stack. A change to one owner should not be disguised as a magic margin on the other. Stressing card count and text length exposes whether those responsibilities are really separate.

## Start from one visible behavior

Read this contract slowly: Three repair stations wrap using Flexbox, cope with uneven descriptions and remain usable when only one station exists. The container owns distribution; individual cards own their internal vertical arrangement.

Underline the promised result, circle the input boundary and mark the stated limitation. A junior developer often starts by naming a framework or file. Start instead with an observation that a user could confirm or reject. File names become useful after you know which responsibility you are looking for.

## Clinic 1: Flex basis

The preferred starting size used by flex layout.

**Small experiment:** Compare a preference with a rigid width using one remaining card.

Find the part of `.stations and .station-note` or its surrounding adapter that makes this idea observable. Read no more than one small responsibility at a time. Write the value or structure before the operation, the operation itself and the value or structure afterward. If this is a layout observation, use the containing box, matching rule and resulting arrangement instead of inventing a JavaScript variable.

### Predict before inspecting

Write one ordinary example and one example that makes the distinction matter. Give an expected result for each. The second example should separate two plausible implementations; simply changing a name or color may leave both candidates behaving identically. Explain why your chosen variation is informative.

### Build a tiny explanation

Explain **flex basis** in three sentences: what problem it names, where you can see it in this repository, and what would go wrong if you ignored it. Avoid replacing the explanation with a slogan such as “best practice.” A concrete input, property or event should appear in at least one sentence.

### Repeat with less support

Close this paragraph, revisit the source and reconstruct the explanation without copying. Then deliberately change one assumption and predict which part of the explanation must change. Record the first point where you become uncertain. That point is a better question for a mentor than asking for another complete tour of the entire project.

**Checkpoint question:** How would you teach this distinction using only the experiment “Compare a preference with a rigid width using one remaining card.”? Leave your answer in the session journal before reading the mentor hints.

## Clinic 2: Free space

Room available after content and sizing constraints.

**Small experiment:** Explain what margin-top:auto can absorb in a card column.

Find the part of `.stations and .station-note` or its surrounding adapter that makes this idea observable. Read no more than one small responsibility at a time. Write the value or structure before the operation, the operation itself and the value or structure afterward. If this is a layout observation, use the containing box, matching rule and resulting arrangement instead of inventing a JavaScript variable.

### Predict before inspecting

Write one ordinary example and one example that makes the distinction matter. Give an expected result for each. The second example should separate two plausible implementations; simply changing a name or color may leave both candidates behaving identically. Explain why your chosen variation is informative.

### Build a tiny explanation

Explain **free space** in three sentences: what problem it names, where you can see it in this repository, and what would go wrong if you ignored it. Avoid replacing the explanation with a slogan such as “best practice.” A concrete input, property or event should appear in at least one sentence.

### Repeat with less support

Close this paragraph, revisit the source and reconstruct the explanation without copying. Then deliberately change one assumption and predict which part of the explanation must change. Record the first point where you become uncertain. That point is a better question for a mentor than asking for another complete tour of the entire project.

**Checkpoint question:** How would you teach this distinction using only the experiment “Explain what margin-top:auto can absorb in a card column.”? Leave your answer in the session journal before reading the mentor hints.

## Clinic 3: Intrinsic minimum

Content-driven sizing that can resist shrinking.

**Small experiment:** Use one unbroken station name to expose the constraint.

Find the part of `.stations and .station-note` or its surrounding adapter that makes this idea observable. Read no more than one small responsibility at a time. Write the value or structure before the operation, the operation itself and the value or structure afterward. If this is a layout observation, use the containing box, matching rule and resulting arrangement instead of inventing a JavaScript variable.

### Predict before inspecting

Write one ordinary example and one example that makes the distinction matter. Give an expected result for each. The second example should separate two plausible implementations; simply changing a name or color may leave both candidates behaving identically. Explain why your chosen variation is informative.

### Build a tiny explanation

Explain **intrinsic minimum** in three sentences: what problem it names, where you can see it in this repository, and what would go wrong if you ignored it. Avoid replacing the explanation with a slogan such as “best practice.” A concrete input, property or event should appear in at least one sentence.

### Repeat with less support

Close this paragraph, revisit the source and reconstruct the explanation without copying. Then deliberately change one assumption and predict which part of the explanation must change. Record the first point where you become uncertain. That point is a better question for a mentor than asking for another complete tour of the entire project.

**Checkpoint question:** How would you teach this distinction using only the experiment “Use one unbroken station name to expose the constraint.”? Leave your answer in the session journal before reading the mentor hints.

## Clinic 4: Container responsibility

A rule governing relationships among children.

**Small experiment:** Locate wrapping and gap separately from card padding.

Find the part of `.stations and .station-note` or its surrounding adapter that makes this idea observable. Read no more than one small responsibility at a time. Write the value or structure before the operation, the operation itself and the value or structure afterward. If this is a layout observation, use the containing box, matching rule and resulting arrangement instead of inventing a JavaScript variable.

### Predict before inspecting

Write one ordinary example and one example that makes the distinction matter. Give an expected result for each. The second example should separate two plausible implementations; simply changing a name or color may leave both candidates behaving identically. Explain why your chosen variation is informative.

### Build a tiny explanation

Explain **container responsibility** in three sentences: what problem it names, where you can see it in this repository, and what would go wrong if you ignored it. Avoid replacing the explanation with a slogan such as “best practice.” A concrete input, property or event should appear in at least one sentence.

### Repeat with less support

Close this paragraph, revisit the source and reconstruct the explanation without copying. Then deliberately change one assumption and predict which part of the explanation must change. Record the first point where you become uncertain. That point is a better question for a mentor than asking for another complete tour of the entire project.

**Checkpoint question:** How would you teach this distinction using only the experiment “Locate wrapping and gap separately from card padding.”? Leave your answer in the session journal before reading the mentor hints.

## Read a real source window

The following is an excerpt from [public/style.css](../public/style.css), beginning at source line 175. It is a reading window, not a standalone runnable exercise. Open the linked file for surrounding declarations and context.

```css
}
@media(max-width:500px) {
  header,main,footer {
    width:calc(100% - 28px)
  }
  .panel,.card {
    padding:18px
  }
  h1 {
    font-size:2.3rem
  }
  th,td {
    padding:8px 5px
  }
}
/* Project-specific layout rules. */
.stations {
  display:flex;
  flex-wrap:wrap;
  gap:20px;
  align-items:stretch
}
.stations .card {
  flex:1 1 260px;
```

For each meaningful line, label its job as input interpretation, validation, state ownership, transformation, output or presentation. Some files contain only a subset of those jobs. Do not force the categories onto code that does not perform them. A closing brace is structure, not a separate business rule.

Choose one expression and restate it as a question the program answers. Then choose one expression that merely carries out a consequence of that answer. This separates a product decision from mechanical plumbing. If you cannot explain an operator, isolate a tiny example rather than rewriting the whole function.

## A three-column scratch sheet

| Before | Rule or operation | After |
|---|---|---|
| Write an actual supported input or layout situation | Name the owning function, property or event | Predict the concrete result |
| Change one assumption | State which rule now matters | Predict what changes and what remains stable |
| Use an invalid, missing or unsupported case | Identify the boundary that rejects or handles it | Predict feedback and retained state |

Do not fill the After column by running the reference first. That turns prediction practice into transcription. After predicting, observe the program and put discrepancies in a fourth note below the table. A wrong prediction is useful when you can name the mistaken assumption.

## What understanding looks like

You can locate `.stations and .station-note`, explain why the adapter has a separate job, and produce a new counterexample without borrowing one from the tests. You can also say what the reference deliberately does not support. If one of those is missing, choose the smallest clinic above that addresses it and repeat that clinic with different data.

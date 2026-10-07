# Code tour and architecture decisions

[Overview](../README.md) · [Concepts](02-CONCEPTS-AND-TRACES.md)

| File | Responsibility |
|---|---|
| [package.json](../package.json) | Names the module format, Node requirement and local commands; private prevents npm publication. |
| [.github/workflows/check.yml](../.github/workflows/check.yml) | Runs the committed checks on GitHub. A workflow file is not evidence that a remote run succeeded. |
| [public/index.html](../public/index.html) | Semantic station content: three `article.card` stations with time tags, descriptions and notes. |
| [public/style.css](../public/style.css) | Presentation, focus indication and project-specific layout. |
| [tools/serve.mjs](../tools/serve.mjs) | Local preview infrastructure; only public/ is served. |
| [tools/check-site.mjs](../tools/check-site.mjs) | Checks referenced local assets exist, without pretending to judge usability. |

## Follow one path, not every file

Start at [public/style.css](../public/style.css) and locate `.stations and .station-note`. Use this trace as a map: The stations container becomes a wrapping flex row → each card starts with a 260px basis → available room controls growth and wrapping → each card is also a column → margin-top:auto pushes its station note toward the bottom.

The tooling is intentionally separate from the product concept. You can study the local server or CI after the main rule is clear. Neither an HTTP preview server nor a workflow configuration should become a prerequisite for understanding a layout rule.

## Decision: Use a wrapping container

flex-wrap lets the browser move a card when the available space no longer supports the preferred basis. A separate breakpoint for every possible card count would be harder to maintain.

**Review question:** Explain why the container owns wrapping instead of each individual card.

**Your alternative:** Write a plausible different choice, then give a concrete example that reveals its cost. “More scalable” or “cleaner” is not enough; identify a changed dependency, a new state to manage, or a user-visible failure mode.

## Decision: Allow cards to shrink

min-width:0 and overflow-wrap:anywhere protect the layout from a long unbroken label. The content should remain visible, rather than force the whole page wider.

**Review question:** Find the difference between a preferred flex basis and a rigid width.

**Your alternative:** Write a plausible different choice, then give a concrete example that reveals its cost. “More scalable” or “cleaner” is not enough; identify a changed dependency, a new state to manage, or a user-visible failure mode.

## Decision: Use nested layout for a different responsibility

The outer row distributes cards. Each card’s own column layout separates its description and bottom note. These are two different layout problems, even though both use Flexbox.

**Review question:** Explain why margin-top:auto works only when there is free space to absorb.

**Your alternative:** Write a plausible different choice, then give a concrete example that reveals its cost. “More scalable” or “cleaner” is not enough; identify a changed dependency, a new state to manage, or a user-visible failure mode.

## Change boundaries

A small change should begin in the file that owns its meaning. Semantic information belongs in HTML before styling; layout belongs in the relevant CSS rule.

If a story crosses two files, say why. A new section may require markup, a navigation link or a layout rule to change together. That is a coherent feature boundary, not permission to rewrite unrelated parts of the project.

## Deliberate limits

No persistence, external integration or general framework is hidden behind these files. The preview server is a local development aid, not a production hosting system. A browser screenshot is one observation, not proof of every device or assistive technology. Keep these limits visible when describing your own work.

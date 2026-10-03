# Code tour and architecture decisions

[Overview](../README.md) · [Concepts](02-CONCEPTS-AND-TRACES.md)

| File | Responsibility |
|---|---|
| [package.json](../package.json) | Names the module format, Node requirement and local commands; private prevents npm publication. |
| [.github/workflows/check.yml](../.github/workflows/check.yml) | Runs the committed checks on GitHub. A workflow file is not evidence that a remote run succeeded. |
| [public/index.html](../public/index.html) | Semantic content, controls and explicit IDs. |
| [public/style.css](../public/style.css) | Presentation, focus indication and project-specific layout. |
| [tools/serve.mjs](../tools/serve.mjs) | Local preview infrastructure; only public/ is served. |
| [tools/check-site.mjs](../tools/check-site.mjs) | Checks referenced local assets exist, without pretending to judge usability. |

## Follow one path, not every file

Start at [public/index.html](../public/index.html) and locate `the skip link and main#main`. Use this trace as a map: Tab reaches .skip → Enter follows #main → tabindex=-1 makes main a valid programmatic focus target without inserting it into ordinary Tab order → the next Tab reaches the next useful link in main.

The tooling is intentionally separate from the product concept. You can study the local server or CI after the main rule is clear. Neither an HTTP preview server nor a workflow configuration should become a prerequisite for understanding an inline-block box or a small pure function.

## Decision: Use native anchors

A link already supports keyboard activation, browser navigation and a meaningful accessible role. Clickable generic divs would require recreating behavior that HTML provides.

**Review question:** Explain the difference between navigating somewhere and performing an action.

**Your alternative:** Write a plausible different choice, then give a concrete example that reveals its cost. “More scalable” or “cleaner” is not enough; identify a changed dependency, a new state to manage, or a user-visible failure mode.

## Decision: Avoid positive tabindex values

Source order describes the intended reading and focus sequence. Positive tabindex can create a second order that becomes difficult to maintain as links are added.

**Review question:** Predict the sequence after inserting a new link in the source.

**Your alternative:** Write a plausible different choice, then give a concrete example that reveals its cost. “More scalable” or “cleaner” is not enough; identify a changed dependency, a new state to manage, or a user-visible failure mode.

## Decision: Make focus visible and understandable

The focus outline shows where the next keyboard action will occur. Descriptive link text explains the destination independently of surrounding prose. These are separate requirements.

**Review question:** Explain why a visible outline does not rescue a link labeled only “here”.

**Your alternative:** Write a plausible different choice, then give a concrete example that reveals its cost. “More scalable” or “cleaner” is not enough; identify a changed dependency, a new state to manage, or a user-visible failure mode.

## Change boundaries

A small change should begin in the file that owns its meaning. Change domain rules in the core, wording and interaction in the browser adapter, and layout in the relevant CSS rule. For the static references, semantic information belongs in HTML before styling. For the Git reference, the staged snapshot boundary belongs in the helper rather than being guessed from editor state.

If a story crosses two files, say why. A new unit, weather option or UI station may require a contract, a control and tests to change together. That is a coherent feature boundary, not permission to rewrite unrelated parts of the project.

## Deliberate limits

No persistence, external integration or general framework is hidden behind these files. The preview server is a local development aid, not a production hosting system. A browser screenshot is one observation, not proof of every device or assistive technology. Keep these limits visible when describing your own work.

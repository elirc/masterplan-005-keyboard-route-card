# Hints and answer directions

[Return to the stories](05-PRACTICE-STORIES.md)

There are intentionally no complete feature patches here. Use one hint, return to your code and produce evidence. Your design can differ from the reference when you state and verify the new contract.

## Story 01: Add a venue section

**Hint 1 — ownership:** Begin from the `nav` links and section order in `public/index.html`. Add a venue section and a descriptive navigation link in reading order.

**Hint 2 — reasoning:** Revisit the decision “Avoid positive tabindex values”. Ask yourself: Predict the sequence after inserting a new link in the source.

**Answer direction:** A defensible solution demonstrates this observable result: The keyboard route remains predictable forward and backward. The exact code is not prescribed. If your change achieves that result by changing an unrelated original rule, revise either the implementation or the story contract explicitly.

**Self-review:** Could the UI or helper appear correct while the underlying rule remains wrong? Could the underlying calculation be correct while stale presentation misleads the user? Choose the question that applies and write one distinguishing example.

## Story 02: Improve ambiguous link text

**Hint 1 — ownership:** Begin from the in-section links such as “Read the event's access information”. Introduce a deliberately vague link in a scratch branch, then replace it.

**Hint 2 — reasoning:** Revisit the decision “Make focus visible and understandable”. Ask yourself: Explain why a visible outline does not rescue a link labeled only “here”.

**Answer direction:** A defensible solution demonstrates this observable result: The final link makes sense when read on its own. The exact code is not prescribed. If your change achieves that result by changing an unrelated original rule, revise either the implementation or the story contract explicitly.

**Self-review:** Could the UI or helper appear correct while the underlying rule remains wrong? Could the underlying calculation be correct while stale presentation misleads the user? Choose the question that applies and write one distinguishing example.

## Story 03: Add a focus-route record

**Hint 1 — ownership:** Begin from `the skip link and main#main`. Document each tab stop and what activation does.

**Hint 2 — reasoning:** Revisit the decision “Avoid positive tabindex values”. Ask yourself: Predict the sequence after inserting a new link in the source.

**Answer direction:** A defensible solution demonstrates this observable result: The recorded order matches the browser rather than the visual position alone. The exact code is not prescribed. If your change achieves that result by changing an unrelated original rule, revise either the implementation or the story contract explicitly.

**Self-review:** Could the UI or helper appear correct while the underlying rule remains wrong? Could the underlying calculation be correct while stale presentation misleads the user? Choose the question that applies and write one distinguishing example.

## Story 04: Support larger text

**Hint 1 — ownership:** Begin from the focus and `section:target` rules in `public/style.css`. Inspect the page with increased text size and repair actual crowding.

**Hint 2 — reasoning:** Revisit the decision “Make focus visible and understandable”. Ask yourself: Explain why a visible outline does not rescue a link labeled only “here”.

**Answer direction:** A defensible solution demonstrates this observable result: No focused link or essential sentence becomes hidden. The exact code is not prescribed. If your change achieves that result by changing an unrelated original rule, revise either the implementation or the story contract explicitly.

**Self-review:** Could the UI or helper appear correct while the underlying rule remains wrong? Could the underlying calculation be correct while stale presentation misleads the user? Choose the question that applies and write one distinguishing example.

## Story 05: Add a downloadable preparation note

**Hint 1 — ownership:** Begin from the contact section in `public/index.html`. Create a local text file and a clearly labeled download link.

**Hint 2 — reasoning:** Revisit the decision “Use native anchors”. Ask yourself: Explain the difference between navigating somewhere and performing an action.

**Answer direction:** A defensible solution demonstrates this observable result: The asset exists and the label explains both content and action. The exact code is not prescribed. If your change achieves that result by changing an unrelated original rule, revise either the implementation or the story contract explicitly.

**Self-review:** Could the UI or helper appear correct while the underlying rule remains wrong? Could the underlying calculation be correct while stale presentation misleads the user? Choose the question that applies and write one distinguishing example.

## Story 06: Review an accidental focus trap

**Hint 1 — ownership:** Begin from `the skip link and main#main`. Describe how a future dialog could trap or lose focus and write acceptance examples before implementation.

**Hint 2 — reasoning:** Revisit the decision “Avoid positive tabindex values”. Ask yourself: Predict the sequence after inserting a new link in the source.

**Answer direction:** A defensible solution demonstrates this observable result: The examples include opening, closing, Escape and return to the triggering control. The exact code is not prescribed. If your change achieves that result by changing an unrelated original rule, revise either the implementation or the story contract explicitly.

**Self-review:** Could the UI or helper appear correct while the underlying rule remains wrong? Could the underlying calculation be correct while stale presentation misleads the user? Choose the question that applies and write one distinguishing example.

## Answers to the trace questions

Tab reaches .skip → Enter follows #main → tabindex=-1 makes main a valid programmatic focus target without inserting it into ordinary Tab order → the next Tab reaches the next useful link in main.

The expected examples are in the concepts table. Use them to check your reasoning, then supply a new example of your own. A copied sentence is not evidence that you can trace a changed input.

## When to ask for more help

Ask after you can show a concrete attempt, a specific uncertainty and an observation. Request a smaller hint before a full patch. If you do accept generated code, explain each changed line and run a counterexample you chose independently.

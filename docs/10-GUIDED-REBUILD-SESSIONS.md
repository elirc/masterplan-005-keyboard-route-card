# Rebuild Keyboard Route Card through small verified slices

[Expanded workshop map](WORKBOOK-INDEX.md) · [Repository overview](../README.md)

This is a hypothetical reconstruction exercise using the existing reference as a comparison point. Work on a practice branch or a separate scratch copy. Do not erase the working reference. Your goal is to recover the important decisions from requirements, not reproduce every character or configuration file from memory.

## Session zero: write a contract you can challenge

The first Tab reveals a skip link. Activating it focuses main. Navigation, schedule, access and contact links follow meaningful source order, have visible focus, and can be traversed in reverse.

Your target skill is focus order and usable page structure. Write three examples before implementation: one ordinary success, one boundary distinction and one recovery or repeat sequence. Reuse the fixed reference fixtures only after making a prediction. If your new example is outside the documented scope, decide whether to reject it or explicitly expand the contract; do not let an incidental implementation choice decide silently.

Write a short non-goal list tied to this exercise. Non-goals keep an assistant from adding a database, a UI framework or a broad refactor before you understand the central rule. For static layout work, a meaningful non-goal may be scripting interactions that native HTML already handles. For stateful work, it may be remote persistence or a global state container.

## Slice 1: Write the route as a user journey

**Reference context:** Before styling, list the useful destinations: schedule, access details and organizer contact. Put them in the source in that order. Then add supporting links within the sections. A keyboard route should feel like a coherent reading path rather than a puzzle determined by where elements happen to be positioned visually.

### Your implementation route

1. Inspect `public/index.html` and the related adapter `public/index.html and public/style.css`. Write which responsibility belongs to each for this slice. A path is a place to inspect, not automatic permission to edit every file.
2. State the example independently: **First Tab → Visible Skip to main content link**. Explain which requirement supplies the expected answer.
3. Build the smallest version that can express the example. Start with explicit data and direct control flow. Introduce a helper only when you can name its input, output and reason to change.
4. Observe the result through the real boundary: a command, a browser control, or a layout condition. A function returning the right value does not prove a button passes it the right input.
5. Add a neighboring example that would fail if you special-cased the first one. Review your diff before comparing with the reference.

### Pause at the first uncertainty

Write the smallest question you cannot answer. It might concern ownership, a comparison operator, the effect of deleting a property, or when a callback actually runs. Include the exact expression and an example. Ask a mentor for one clue, then return to the source; avoid requesting a complete replacement implementation.

### Inspect an alternative

Choose one plausible different design for this slice. Describe the extra state, dependency or maintenance rule it introduces. If it satisfies the same contract, it is not automatically wrong. Compare the cost of making the next small change. If it violates the contract, provide the smallest concrete example that demonstrates that violation.

### Capture a reviewable stopping point

Record your actual check: npm test (local asset references), plus the relevant browser/content observation. State what it established and what remains untested. Use a commit message about the resulting behavior rather than a list of file names. If the slice does not work yet, keep the uncertainty visible in the journal instead of writing a success narrative.

**Left for you:** the code, fixture values beyond the supplied example, exact naming and the acceptance evidence. The reference is available for comparison after an attempt; it is not evidence that your branch has passed.

## Slice 2: Give the skip link a real destination

**Reference context:** The link targets main#main. The negative tabindex allows focus to land there when the fragment is activated but does not make the entire main container an extra ordinary tab stop. Observe focus with document.activeElement in developer tools. Looking only at scroll position would miss a skip link that scrolls without transferring interaction focus.

### Your implementation route

1. Inspect `public/index.html` and the related adapter `public/index.html and public/style.css`. Write which responsibility belongs to each for this slice. A path is a place to inspect, not automatic permission to edit every file.
2. State the example independently: **Enter on skip → Focus moves to main**. Explain which requirement supplies the expected answer.
3. Build the smallest version that can express the example. Start with explicit data and direct control flow. Introduce a helper only when you can name its input, output and reason to change.
4. Observe the result through the real boundary: a command, a browser control, or a layout condition. A function returning the right value does not prove a button passes it the right input.
5. Add a neighboring example that would fail if you special-cased the first one. Review your diff before comparing with the reference.

### Pause at the first uncertainty

Write the smallest question you cannot answer. It might concern ownership, a comparison operator, the effect of deleting a property, or when a callback actually runs. Include the exact expression and an example. Ask a mentor for one clue, then return to the source; avoid requesting a complete replacement implementation.

### Inspect an alternative

Choose one plausible different design for this slice. Describe the extra state, dependency or maintenance rule it introduces. If it satisfies the same contract, it is not automatically wrong. Compare the cost of making the next small change. If it violates the contract, provide the smallest concrete example that demonstrates that violation.

### Capture a reviewable stopping point

Record your actual check: npm test (local asset references), plus the relevant browser/content observation. State what it established and what remains untested. Use a commit message about the resulting behavior rather than a list of file names. If the slice does not work yet, keep the uncertainty visible in the journal instead of writing a success narrative.

**Left for you:** the code, fixture values beyond the supplied example, exact naming and the acceptance evidence. The reference is available for comparison after an attempt; it is not evidence that your branch has passed.

## Slice 3: Keep the focused link visible

**Reference context:** The skip link is positioned off-screen until focused, then shown at the top. Other links receive a clear focus outline. Test that indication against the page background and with larger text. Do not remove outline merely because a default style looks untidy; replace it with something equally discoverable.

### Your implementation route

1. Inspect `public/index.html` and the related adapter `public/index.html and public/style.css`. Write which responsibility belongs to each for this slice. A path is a place to inspect, not automatic permission to edit every file.
2. State the example independently: **Tab through header → Schedule → Access information → Contact**. Explain which requirement supplies the expected answer.
3. Build the smallest version that can express the example. Start with explicit data and direct control flow. Introduce a helper only when you can name its input, output and reason to change.
4. Observe the result through the real boundary: a command, a browser control, or a layout condition. A function returning the right value does not prove a button passes it the right input.
5. Add a neighboring example that would fail if you special-cased the first one. Review your diff before comparing with the reference.

### Pause at the first uncertainty

Write the smallest question you cannot answer. It might concern ownership, a comparison operator, the effect of deleting a property, or when a callback actually runs. Include the exact expression and an example. Ask a mentor for one clue, then return to the source; avoid requesting a complete replacement implementation.

### Inspect an alternative

Choose one plausible different design for this slice. Describe the extra state, dependency or maintenance rule it introduces. If it satisfies the same contract, it is not automatically wrong. Compare the cost of making the next small change. If it violates the contract, provide the smallest concrete example that demonstrates that violation.

### Capture a reviewable stopping point

Record your actual check: npm test (local asset references), plus the relevant browser/content observation. State what it established and what remains untested. Use a commit message about the resulting behavior rather than a list of file names. If the slice does not work yet, keep the uncertainty visible in the journal instead of writing a success narrative.

**Left for you:** the code, fixture values beyond the supplied example, exact naming and the acceptance evidence. The reference is available for comparison after an attempt; it is not evidence that your branch has passed.

## Slice 4: Check both directions and state changes

**Reference context:** Use Tab to move forward and Shift+Tab to return. Activate an internal anchor and inspect where the page moves. The reference contains no modal or dynamic focus trap, so the user should not become stuck. Automated keyboard checks cover the expected route, but a complete accessibility review would require more than these checks and one browser.

### Your implementation route

1. Inspect `public/index.html` and the related adapter `public/index.html and public/style.css`. Write which responsibility belongs to each for this slice. A path is a place to inspect, not automatic permission to edit every file.
2. State the example independently: **Shift+Tab from Schedule → Returns to the skip link**. Explain which requirement supplies the expected answer.
3. Build the smallest version that can express the example. Start with explicit data and direct control flow. Introduce a helper only when you can name its input, output and reason to change.
4. Observe the result through the real boundary: a command, a browser control, or a layout condition. A function returning the right value does not prove a button passes it the right input.
5. Add a neighboring example that would fail if you special-cased the first one. Review your diff before comparing with the reference.

### Pause at the first uncertainty

Write the smallest question you cannot answer. It might concern ownership, a comparison operator, the effect of deleting a property, or when a callback actually runs. Include the exact expression and an example. Ask a mentor for one clue, then return to the source; avoid requesting a complete replacement implementation.

### Inspect an alternative

Choose one plausible different design for this slice. Describe the extra state, dependency or maintenance rule it introduces. If it satisfies the same contract, it is not automatically wrong. Compare the cost of making the next small change. If it violates the contract, provide the smallest concrete example that demonstrates that violation.

### Capture a reviewable stopping point

Record your actual check: npm test (local asset references), plus the relevant browser/content observation. State what it established and what remains untested. Use a commit message about the resulting behavior rather than a list of file names. If the slice does not work yet, keep the uncertainty visible in the journal instead of writing a success narrative.

**Left for you:** the code, fixture values beyond the supplied example, exact naming and the acceptance evidence. The reference is available for comparison after an attempt; it is not evidence that your branch has passed.

## Reconstruct the whole path without the guide

Tab reaches .skip → Enter follows #main → tabindex=-1 makes main a valid programmatic focus target without inserting it into ordinary Tab order → the next Tab reaches the next useful link in main.

Close this page and redraw that route from memory using your own labels. Open the code only to resolve a specific uncertainty. Then trace a different valid input and one boundary. If your picture requires a hidden value that you cannot locate in the source, investigate it; diagrams can invent state just as easily as prose can.

## Compare your implementation fairly

First compare behavior and evidence. Only then compare style and abstractions. A shorter implementation may be harder for you to explain; a longer implementation may duplicate a rule that later drifts. State the concrete tradeoff. Do not treat matching the reference line for line as the only successful outcome.

## Finish with a teach-back

Explain why `the skip link and main#main` is enough for its present responsibility, which work remains in `public/index.html and public/style.css`, and which future requirement would justify changing that boundary. Answer the original transfer question: Can someone predict what each focused link will do without using a mouse? Keep the answer short enough that another junior can challenge it with an example.

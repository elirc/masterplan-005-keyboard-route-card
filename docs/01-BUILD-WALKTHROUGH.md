# Building Keyboard Route Card, one decision at a time

[Learning route](00-START-HERE.md) · [Code tour](03-CODE-TOUR.md)

This is a reconstruction of how to approach the finished reference. It explains visible design choices; it is not a transcript of hidden reasoning or a claim that a fictional team performed these steps.

## Start from the contract

The first Tab reveals a skip link. Activating it focuses main. Navigation, schedule, access and contact links follow meaningful source order, have visible focus, and can be traversed in reverse.

The smallest useful result answers this user need: A keyboard user needs to reach the useful links on a small event page in a predictable order. Write the examples before choosing file names. Keep the scope small enough that the decisive behavior fits in one trace.

## Step 1: Write the route as a user journey

Before styling, list the useful destinations: schedule, access details and organizer contact. Put them in the source in that order. Then add supporting links within the sections. A keyboard route should feel like a coherent reading path rather than a puzzle determined by where elements happen to be positioned visually.

**Pause and produce evidence:** First Tab. Predict the outcome, then compare it with the reference. In your notes, distinguish what the code says should happen from what you actually observed.

## Step 2: Give the skip link a real destination

The link targets main#main. The negative tabindex allows focus to land there when the fragment is activated but does not make the entire main container an extra ordinary tab stop. Observe focus with document.activeElement in developer tools. Looking only at scroll position would miss a skip link that scrolls without transferring interaction focus.

**Pause and produce evidence:** Enter on skip. Predict the outcome, then compare it with the reference. In your notes, distinguish what the code says should happen from what you actually observed.

## Step 3: Keep the focused link visible

The skip link is positioned off-screen until focused, then shown at the top. Other links receive a clear focus outline. Test that indication against the page background and with larger text. Do not remove outline merely because a default style looks untidy; replace it with something equally discoverable.

**Pause and produce evidence:** Tab through header. Predict the outcome, then compare it with the reference. In your notes, distinguish what the code says should happen from what you actually observed.

## Step 4: Check both directions and state changes

Use Tab to move forward and Shift+Tab to return. Activate an internal anchor and inspect where the page moves. The reference contains no modal or dynamic focus trap, so the user should not become stuck. Automated keyboard checks cover the expected route, but a complete accessibility review would require more than these checks and one browser.

**Pause and produce evidence:** Shift+Tab from Schedule. Predict the outcome, then compare it with the reference. In your notes, distinguish what the code says should happen from what you actually observed.

## Keep the implementation reviewable

A useful commit has one understandable reason to exist. Separate the initial working slice, the checks that expose its important boundaries, and the teaching material that explains it. The published commits in this repository were assembled from verified working files; they are real commits, not fabricated evidence of a long historical development process. M001 additionally contains the actual two-file baseline and a separate opening-time correction.

For your own variation, commit at a point where the behavior and evidence agree. Describe the trigger, the resulting behavior and the check in the commit message or review note. Avoid mixing a rule change with unrelated formatting because it makes the learning decision harder to see.

## Stop before adding a platform

The next useful improvement is a sharper example or clearer explanation, not a database, account system or framework migration. Add an abstraction only when it names a real repeated responsibility. You should be able to describe what becomes easier to change after the abstraction and what new complexity it introduces.

**Independent design choice from the original brief:** Choose descriptive link text and demonstrate the keyboard route yourself.

The reference made one choice, documented in the code tour. You may choose differently in a branch if you first revise the contract and acceptance examples. A deliberate alternative is a stronger learning artifact than an unexplained copy.

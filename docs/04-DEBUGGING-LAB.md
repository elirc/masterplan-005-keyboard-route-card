# Debugging laboratory

[Concepts](02-CONCEPTS-AND-TRACES.md) · [Practice stories](05-PRACTICE-STORIES.md)

These are deliberately proposed defects for a scratch branch. They are not claims that the shipped reference still contains these bugs. Keep main working and introduce only one change at a time.

## Case 1: The skip link is never visible

**Introduce or discuss this mistake:** Hide the link with display:none in a scratch edit.

**Discriminating experiment:** Press Tab from a fresh page load.

### Worked diagnosis

First state the expected contract: The first Tab reveals a skip link. Activating it focuses main. Navigation, schedule, access and contact links follow meaningful source order, have visible focus, and can be traversed in reverse. Then create the smallest example from the experiment above. Compare the observed result with the contract before changing more code. The likely cause is at this boundary: **Use off-screen positioning with a visible focused state instead.** Repair that boundary, rerun the example, and check one neighboring valid case so the repair does not merely special-case the chosen input.

The completed reasoning record is: symptom → contract violated → input that distinguishes hypotheses → owning line or rule → minimal repair → regression evidence. This is a worked diagnostic route; fill in your actual outputs when you run it. No invented console transcript is supplied.

## Case 2: The skip link targets nothing

**Introduce or discuss this mistake:** Rename main’s ID without updating the href.

**Discriminating experiment:** Activate skip and inspect document.activeElement.

### Your investigation

1. Write two possible explanations before looking at the hints.
2. Predict what the experiment would show if each explanation were true.
3. Run or inspect the smallest discriminating case and record the result.
4. Identify the owning file and make one bounded repair.
5. Verify the original case and a neighboring case; explain why both matter.

**Location hint, only after your attempt:** Keep the target ID and link aligned.

## Case 3: Tab order surprises the reader

**Introduce or discuss this mistake:** Add tabindex=4 to an ordinary navigation link.

**Discriminating experiment:** Write and compare the resulting focus sequence.

### Your investigation

1. Write two possible explanations before looking at the hints.
2. Predict what the experiment would show if each explanation were true.
3. Run or inspect the smallest discriminating case and record the result.
4. Identify the owning file and make one bounded repair.
5. Verify the original case and a neighboring case; explain why both matter.

**Location hint, only after your attempt:** Remove positive ordering and repair source order instead.

## If the first repair does not work

Do not pile on another unrelated edit. Read the diff and check whether the observed failure changed. If the hypothesis was wrong, write that down and restore only your own experimental change before testing the next hypothesis. A rejected hypothesis is useful progress when its evidence is clear.

When asking an assistant for help, provide the exact input, expected and observed result, the current diff and the file you believe owns the rule. Ask for one counterexample or diagnostic question first. Keep proposed causes separate from demonstrated causes.

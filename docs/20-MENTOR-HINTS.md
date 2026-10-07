# M005: mentor hints and answer directions

[Expanded workshop map](WORKBOOK-INDEX.md) · [Repository overview](../README.md)

Use this chapter after making an attempt. It provides reasoning directions and evaluation criteria, not finished feature patches. A learner can choose a different design when the revised contract is explicit and the evidence supports it.

## Retrieval card 01: answer direction

**Question:** Explain focus target through this project

The element that receives the next keyboard action.

Look for a concrete connection to `public/index.html` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 02: answer direction

**Question:** Explain negative tabindex through this project

Programmatic focusability without another ordinary Tab stop.

Look for a concrete connection to `public/index.html` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 03: answer direction

**Question:** Explain link purpose through this project

The destination or action a label communicates.

Look for a concrete connection to `public/index.html` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 04: answer direction

**Question:** Explain reverse traversal through this project

Returning through the route with Shift+Tab.

Look for a concrete connection to `public/index.html` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 05: answer direction

**Question:** Predict: First Tab

Visible Skip to main content link

Look for a concrete connection to `public/index.html` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 06: answer direction

**Question:** Predict: Enter on skip

Focus moves to main

Look for a concrete connection to `public/index.html` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 07: answer direction

**Question:** Predict: Tab through header

Schedule → Access information → Contact

Look for a concrete connection to `public/index.html` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 08: answer direction

**Question:** Explain the difference between navigating somewhere and performing an action.

A link already supports keyboard activation, browser navigation and a meaningful accessible role. Clickable generic divs would require recreating behavior that HTML provides.

Look for a concrete connection to `public/index.html` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 09: answer direction

**Question:** Predict the sequence after inserting a new link in the source.

Source order describes the intended reading and focus sequence. Positive tabindex can create a second order that becomes difficult to maintain as links are added.

Look for a concrete connection to `public/index.html` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 10: answer direction

**Question:** Explain why a visible outline does not rescue a link labeled only “here”.

The focus outline shows where the next keyboard action will occur. Descriptive link text explains the destination independently of surrounding prose. These are separate requirements.

Look for a concrete connection to `public/index.html` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 11: answer direction

**Question:** What does your strongest check not prove?

Use the scope recorded in VERIFICATION.md; do not infer production readiness from a small local fixture.

Look for a concrete connection to `public/index.html` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Retrieval card 12: answer direction

**Question:** Can someone predict what each focused link will do without using a mouse?

A keyboard route is a sequence of meaningful destinations and visible focus states. Scrolling to a section and transferring focus are related but different observations. Native links give the browser useful behavior; source order makes that behavior predictable. The worksheet should record actual active elements, not infer focus from a screenshot.

Look for a concrete connection to `public/index.html` or `public/index.html and public/style.css`. A strong answer names an input or condition, the responsible operation and the resulting behavior. Merely repeating the vocabulary word is insufficient. If your example differs from the reference, check whether it is supported by the contract before treating a different outcome as a defect.

## Story 07: Add a native disclosure

**First hint:** The desired improvement is “Offer optional preparation details without custom keyboard code.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Use details and summary; write a meaningful summary; inspect open and closed keyboard behavior. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: The disclosure can be operated with the keyboard and does not trap focus. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose which information is truly optional. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 08: Add a phone contact example

**First hint:** The desired improvement is “Compare two native contact destinations.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Add a clearly fictional phone link; label the contact purpose; inspect its position in the route. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: A reader can distinguish phone from email without surrounding prose. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose the fictional number and label. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 09: Show a focused section context

**First hint:** The desired improvement is “Help readers locate an in-page destination.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Add a restrained :target treatment; keep the focus outline distinct; compare scrolling and activeElement. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: Target styling never substitutes for actual focus evidence. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose the target cue. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 10: Add footer navigation

**First hint:** The desired improvement is “Offer a short return path at the end of the page.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Add native links to existing sections; use descriptive labels; verify forward and reverse order. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: Footer navigation does not introduce positive tabindex or dead fragments. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose which destinations belong in the footer. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 11: Explain an unavailable action

**First hint:** The desired improvement is “Avoid a misleading active-looking dead link.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Identify a fictional unavailable destination; replace a fake href with explicit text; document the interaction policy. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: Keyboard users are not offered a link that pretends to work. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose the unavailable-state wording. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 12: Add a link-purpose audit

**First hint:** The desired improvement is “Review every link as an isolated phrase.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Extract labels into a worksheet; mark ambiguous phrases; propose specific replacements without changing destinations. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: Another learner can predict each destination from its label. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose a simple review rubric. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 13: Compare native link and button roles

**First hint:** The desired improvement is “Teach navigation versus local action in a separate fixture.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Describe one destination and one action; select appropriate native elements; avoid shipping a nonfunctional pretend action. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: The worksheet explains why roles differ before adding JavaScript. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose a harmless illustrative action. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 14: Inspect focus against every background

**First hint:** The desired improvement is “Catch a visible outline that disappears in one section.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Traverse the route; record focused element and surrounding colors; adjust only the owning focus rule. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: Focus remains visually identifiable on all inspected backgrounds. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose a replacement outline treatment. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Story 15: Add a no-mouse onboarding card

**First hint:** The desired improvement is “Help a novice reproduce the route.” Start by identifying which existing boundary already knows the necessary information. Do not copy that information into new state until you can explain why derivation is insufficient.

**Second hint:** Follow this source-specific route: Write exact keys and expected destinations; include reverse traversal; separate observed results from blank learner fields. Keep each stage independently inspectable. If a step requires a policy choice, write the choice before implementing it.

**Third hint:** Your strongest completion evidence should establish: A second person can repeat the route without needing a mouse. Invent a plausible wrong implementation and make your example disagree with it.

**Decision still left to you:** Choose the smallest complete route. The guide intentionally does not settle this. Evaluate your answer by clarity of the contract, consistency of the implementation and quality of verification, not by guessing the author's preferred wording.

## Mentor feedback rubric

| Dimension | Beginning | Developing | Independent evidence |
|---|---|---|---|
| Trace | Names files only | Follows one ordinary case | Predicts a new boundary and explains its owner |
| Test design | Copies output | Uses a stated expectation | Rejects a plausible wrong candidate |
| Design | Repeats a slogan | Names an alternative | Compares costs using a concrete change |
| Agent use | Accepts a generated answer | Checks suggested edits | Supplies own proposal and adjudicates critiques |
| Handoff | Claims it works | Lists actual checks | Explains behavior, evidence and limits coherently |

Use the rubric to choose the next practice action, not to label yourself permanently. A learner may be independent at source tracing and still need help designing a failure case. Target the missing skill with one smaller exercise.

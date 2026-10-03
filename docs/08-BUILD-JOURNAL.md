# Build journal: Keyboard Route Card

[Code tour](03-CODE-TOUR.md) · [Actual verification](VERIFICATION.md)

This is a retrospective teaching narrative about the implementation in this repository. It is not a verbatim conversation, fabricated team debate or hidden chain-of-thought transcript. The design explanations below are reviewable rationales tied to the source. Dates and check results belong to the verification record.

## The starting problem

A keyboard user needs to reach the useful links on a small event page in a predictable order.

The main temptation was to make the project larger than its learning target. The useful boundary is **focus order and usable page structure**. A finished small example lets you inspect the whole path and ask what each part contributes. Extra infrastructure would add more things to configure before the central idea became clear.

## The first contract

The first Tab reveals a skip link. Activating it focuses main. Navigation, schedule, access and contact links follow meaningful source order, have visible focus, and can be traversed in reverse.

The contract turned broad intent into examples that can disagree with an implementation. That matters because a plausible-looking result can hide a wrong boundary rule. The examples in the concepts guide were chosen to expose those distinctions, not to make the demo look flawless.

## Decision note 1: Use native anchors

A link already supports keyboard activation, browser navigation and a meaningful accessible role. Clickable generic divs would require recreating behavior that HTML provides.

**What a learner should challenge:** Explain the difference between navigating somewhere and performing an action.

**Evidence to consult:** inspect the owning source file, the contract examples and the verification scope. If your alternative satisfies the same behavior with a different structure, compare the maintenance cost instead of assuming one syntax is automatically correct.

## Decision note 2: Avoid positive tabindex values

Source order describes the intended reading and focus sequence. Positive tabindex can create a second order that becomes difficult to maintain as links are added.

**What a learner should challenge:** Predict the sequence after inserting a new link in the source.

**Evidence to consult:** inspect the owning source file, the contract examples and the verification scope. If your alternative satisfies the same behavior with a different structure, compare the maintenance cost instead of assuming one syntax is automatically correct.

## Decision note 3: Make focus visible and understandable

The focus outline shows where the next keyboard action will occur. Descriptive link text explains the destination independently of surrounding prose. These are separate requirements.

**What a learner should challenge:** Explain why a visible outline does not rescue a link labeled only “here”.

**Evidence to consult:** inspect the owning source file, the contract examples and the verification scope. If your alternative satisfies the same behavior with a different structure, compare the maintenance cost instead of assuming one syntax is automatically correct.

## What the checks contributed

The static asset check caught missing local resources, while the browser checks exercised layout, keyboard entry and project-specific content changes. Neither check alone would justify a blanket accessibility claim.

The record in VERIFICATION.md reports actual local observations. A GitHub Actions workflow is provided, but its remote result must be inspected separately after a push. A screenshot documents one rendered state; it is not a substitute for the interaction and boundary checks.

## What you should do differently on your own build

Start from the same user need but write your own examples first. Choose a small variation from the story list. Predict behavior, implement a slice and compare the result with your prediction. The reference helps you judge a finished result; your journal should record your own uncertainties and discoveries rather than adopting this narrative as if you experienced it.

## The handoff

The next learner can start from README, locate `the skip link and main#main`, reproduce the example table and attempt one bounded story. That is the intended handoff quality: a working result plus enough evidence and explanation to continue safely. The six practice stories remain unfinished for the learner.

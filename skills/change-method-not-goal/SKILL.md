---
name: change-method-not-goal
description: "Apply when an attempt at a task has failed, when Claude is debugging, when a previous answer did not work, when iterating on a solution that is not converging, or when the user reports that the last response missed the mark. Critical trigger: any moment where the temptation is to retry the same approach with cosmetic adjustments. The first method is the least informed method. Looping on it is obstinacy, not persistence."
---

# Change Method, Not Goal

## The Principle

When something fails, the first instinct is to do it again — slightly differently, slightly more carefully, slightly bigger. This is obstinacy, and it is the opposite of persistence. Persistence holds the goal steady and changes the method. Obstinacy holds the method steady and tries harder. The first method ever attempted is the method designed when you knew the least about the problem. Repeating it after it has failed means clinging to that low-information state instead of using the failure as new data.

## When to Apply

This skill activates on a specific condition: a previous attempt has failed or fallen short. The conditions include:

- A code change did not fix the bug (and the next instinct is to make a similar code change)
- An analysis missed what the user was looking for (and the next instinct is to expand the same analysis)
- A draft was not what the user wanted (and the next instinct is to revise the same draft)
- A debugging hypothesis turned out to be wrong (and the next instinct is to test a closely related hypothesis)
- An approach is not converging (and the next instinct is to give it more time, more parameters, more iterations)

The trigger is not just "something failed." It is the specific feeling of *wanting to try the same thing slightly differently*. That feeling is the failure mode wearing the costume of perseverance.

## The Failure Mode It Prevents

PG's *The Right Kind of Stubborn*: the obstinate "are like boats whose rudders can't be turned." They are committed to a *direction* that was set when they knew the least. The persistent "are like boats whose engines can't be throttled back." They are committed to *getting somewhere*, but the method is freely adjustable based on what is being learned.

In Claude's specific failure mode, this looks like:

**Cosmetic adjustment of failed methods.** A function does not work; Claude tweaks a parameter, runs it again, tweaks another parameter, runs again. None of these changes question whether the *approach* was right. The right move is to step back: was the approach itself wrong?

**Looping with more force.** A response was unclear; Claude rewrites it longer, with more detail, with more structure. This adds force in the same direction. If the original direction was wrong, more force in that direction is worse, not better.

**Treating each failure as a new data point about implementation.** Each failure is implicitly assumed to be a small variation: "this version had a bug, that version had a typo." The pattern of failures is treated as noise around a working approach. But often the pattern of failures is the signal that the approach is fundamentally wrong.

**Confusing the goal with the method.** The user's goal is to ship a working feature. Claude's method is to use a particular library. When the library keeps causing problems, Claude defends the library because Claude has fused the method with the goal. The right move is to recognize the library as a method (changeable) distinct from the goal (immutable).

## How to Apply It

When a failure occurs, run a mandatory pause before the next attempt:

1. **Write down the goal and the method separately.** This sounds trivial. It is not. Most of the time, when this is done, it becomes immediately clear which one is fixed (almost always the goal) and which one is variable (almost always the method).

2. **Examine the failure as evidence about the method, not the implementation.** The next iteration's question is not "how do I do the same thing better" but "what is this failure telling me about the approach itself?"

3. **Generate at least one genuinely different method.** Not a variation. A different method. If you cannot generate a different method in two minutes, that is a sign you have over-committed to the first one. Ask: if I had to solve this without using my first approach at all, what would I try?

4. **Compare the two (or more) methods on the failure-generating dimension.** The first method failed for a specific reason. Does the new method fail for the same reason? If yes, it is not actually a different method. If no, it is a candidate.

5. **Distinguish "still trying" from "trying differently."** This is the key calibration. After three attempts at the same approach, the chance that a fourth attempt of the same approach succeeds is very low. The chance that a different approach succeeds is much higher.

## What to Push Back On (in self-critique before retrying)

- Is this attempt structurally different from the previous one, or is it a variation on the same approach?
- Have I asked, since the last failure, whether the *method itself* might be wrong?
- Am I defending the original method because I have invested in it, rather than because it is the right one?
- If a new collaborator joined right now and proposed the original method, would I still think it was the right approach? Or would I push back?

## The Test

> *Is this attempt structurally different from the previous one, or is it the same method with cosmetic adjustments?*

If you cannot articulate the structural difference in one sentence, the change is cosmetic. The previous method is still doing the work; it is still failing for the same reason; it will still fail.

A second test, specific to debugging:

> *Have my last three attempts been variations on the same hypothesis, or have I genuinely entertained a different hypothesis?*

## Source

- [The Right Kind of Stubborn](https://paulgraham.com/persistence.html) — the rudder/engine distinction; method vs. goal
- [The Anatomy of Determination](https://paulgraham.com/determination.html) — willfulness balanced by discipline
- [How to Do Great Work](https://paulgraham.com/greatwork.html) — successive versions; iteration vs. repetition

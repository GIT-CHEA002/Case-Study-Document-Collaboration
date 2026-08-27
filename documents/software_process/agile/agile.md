### Author by Sedtha

## What the model actually is (per Sommerville Ch. 2):

The chapter defines three basic generic process models — waterfall, incremental development, and reuse/integration-and-configuration. Incremental development is distinguished from waterfall specifically by when the core activities happen: in the waterfall model these activities are organized in sequence, whereas in incremental development specification, development, and validation are interleaved, and the model may be either plan-driven or agile. This same point is repeated across multiple course renderings of the chapter: real software processes are interleaved sequences of technical, collaborative, and managerial activities, and the four basic activities — specification, development, validation, and evolution — are organized differently depending on the process, with waterfall sequencing them and incremental development interleaving them.

## Mechanically, how the increments work:

Older Sommerville slide decks (6th edition, same underlying model) describe the operational logic: rather than deliver the system as a single delivery, development and delivery are broken down into increments, with each increment delivering part of the required functionality. Crucially, user requirements are prioritized, and the highest-priority requirements are included in the early increments, and once development of an increment has started, the requirements for that increment are frozen, though requirements for later increments can continue to evolve.

This is the mechanism that matters for your Mentcare argument: incremental/agile doesn't require the full specification to be correct before building starts. It only requires the current increment's scope to be frozen, while later increments stay open to revision based on what's learned from earlier ones.

## Why this fits the "search" ambiguity case (applying the theory by reasoning, not from the book):

The book's own justification for why waterfall struggles with certain requirements is the same logic your document is applying: waterfall assumes specification can be finished before development starts, whereas incremental development assumes specification and validation happen together, in a loop, resolved through built increments rather than upfront analysis. Where a requirement like "what should search return" is inherently a matter of end-user judgment rather than a fixed, derivable rule, the plan-driven waterfall approach has no natural mechanism for testing that judgment against real usage before code exists — it can only be resolved by writing it down and hoping it's right. Incremental development's interleaving of specification and validation gives you a build-test-refine loop instead, which is the general property Sommerville attributes to this model.

## The broader framing point your document made is also textbook-accurate:

The chapter's summary line — that in practice, most large systems are developed using a process that incorporates elements from all of these models — is exactly the caveat your Stage 3 write-up already leans on: Mentcare as a whole is not "pure" incremental/agile, it's a hybrid, and the incremental/agile element is invoked specifically for the ambiguous, user-facing part (search behavior), not the entire system.

## Reference

- [S5] SlideShare, "Ch 2 Software Engineering"(Sommerville Ch. 2 slides) — https://www.slideshare.net/slideshow/ch-2-software-engineering/91393431
- Scribd, "SoftwareProcesses" (CNG350, based on Sommerville Ch. 2) — https://www.scribd.com/presentation/449486496/SoftwareProcesses
- SlideShare, "Software Process Models in Software Engineering" (Sommerville, 6th ed. slides) — https://www.slideshare.net/slideshow/software-process-models-in-software-engineering-8974/272700812
- SlideShare, "Lecture 16 — Software Process (Software Engineering and Development)" — https://www.slideshare.net/slideshow/lecture-16-software-process-software-engineering-and-development-pptx/279937215

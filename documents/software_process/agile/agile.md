### Author by Sedtha

## What "agile" means ?

Agile (incremental) development is a process where specification, development, and validation are interleaved rather than kept as separate, sequential phases — the system is developed as a series of versions (increments), with each version adding functionality to the previous version, and customer feedback shapes each next increment. Sommerville explicitly contrasts this with the waterfall model, where specification and development are kept as separate, distinct phases done once, in order. [S5]

Incremental development itself may be either plan-driven or agile — but agile specifically means planning is done incrementally, and it is easier to change the process to reflect changing customer requirements, rather than committing to a full plan up front the way plan-driven development does. [S7]

## Why agile fits this kind of requirement ?

Sommerville lists concrete benefits of incremental/agile development, and each one applies directly to Mentcare's user-facing behavior: [S5]

Lower cost of changes: the cost of accommodating changing customer requirements is reduced, and the amount of analysis and documentation that has to be redone is much less than with the waterfall model — relevant because exactly what "search" should mean, or how a report should be formatted, wasn't fully knowable up front the way a legal rule is.

Frequent feedback: it is easier to get customer feedback on the development work that has been done — customers can comment on demonstrations of the software and see how much has been implemented — relevant because clinic staff are the real judge of whether a search feature or report layout is actually usable.

Faster delivery: more rapid delivery and deployment of useful software to the customer is possible, so customers gain value from the software earlier than with a waterfall process — relevant because a working, if imperfect, search or reporting feature can go live and improve with real clinic use, rather than waiting for a single, fully-specified version.

Unlike the plan-driven items (fixed by external law) or the reuse-oriented items (solved by existing technology), these requirements involve genuine ambiguity in what the *right* behavior is — the kind of ambiguity that can only be resolved by building something, watching real staff use it, and adjusting.

## Which of our SRS requirements were built this way?

| ID | Requirement | Why Agile |
|---|---|---|
| SR-F01 | Monthly Drug Cost Report, generated at 17:30 on the last working day | The exact timing is an implementation decision beyond what the URD stated — the kind of detail typically settled by testing with real clinic managers |
| SR-F02 | Cross-clinic appointment search | The book's own ambiguity example — "search" had to be clarified through iteration, the clearest possible proof of agile refinement |
| SR-F03 | Daily attendance list per clinic | Direct from the book in principle, but its exact format/fields are the kind of detail usually tuned with real clinic staff feedback |
| SR-NF07 | 2-hour training target, 2 errors/hour usability goal | A usability target normally achieved by testing the UI with real users and adjusting, not fixed correctly on the first attempt |

### Reference

- [S5] SlideShare, "Ch 2 Software Engineering" (Sommerville Ch. 2 slides) — https://www.slideshare.net/slideshow/ch-2-software-engineering/91393431
- [S7] Studocu — https://www.studocu.com/row/document/the-university-of-faisalabad/human-computer-interaction/2nd-chp-se-none/19031193

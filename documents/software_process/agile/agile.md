### Author by Sedtha

## What the model is, per the source

Sommerville defines three basic process models — waterfall, incremental development, and integration/configuration (reuse-oriented). Incremental development is described as follows: specification, development and validation are interleaved, and it may be plan-driven or agile. This is explicitly contrasted with waterfall, where specification and development are separate and distinct phases. 

The interleaving point is repeated more precisely in the "process activities" section: the four basic process activities of specification, development, validation and evolution are organized differently in different development processes — in the waterfall model they are organized in sequence, whereas in incremental development they are interleaved.

A companion source paraphrasing the same chapter adds the detail that matters most for your case: the system is developed as a series of versions (increments), with each version adding functionality to the previous version. 

## Why the source says this model helps with ambiguity

Sommerville lists concrete benefits of incremental development, and two of them are exactly what resolving "search" behavior in 5.4 requires:

* Lower cost of changes: the cost of accommodating changing customer requirements is reduced, and the amount of analysis and documentation that has to be redone is much less than with the waterfall model. 

* Frequent feedback: it is easier to get customer feedback on the development work that has been done — customers can comment on demonstrations of the software and see how much has been implemented. 

* Faster delivery: more rapid delivery and deployment of useful software to the customer is possible, so customers gain value from the software earlier than with a waterfall process.

## Applied to Section 5.4
The requirement "a user shall be able to search the appointments lists for all clinics" specifies that search must exist but not how it should behave — by name, by date range, by clinic, by status, etc. Under waterfall, that ambiguity would have to be fully resolved on paper before any code is written, because the waterfall model's main drawback is the difficulty of accommodating change once the process is underway. Under incremental development, a first version of the search feature can be built with a reasonable guess at behavior, shown to clinic staff, and revised — because specification and validation are not locked in sequence but interleaved, each round of user feedback can directly reshape the next increment's specification. 

## Stage 3 — Incremental / Agile

*Behavior that needed real usage/feedback to pin down — this is where refinement happens.*

| ID | Why agile |
|---|---|
| SR-F01 | The exact timing (17:30, last working day) is an implementation decision beyond what the URD stated — the kind of detail typically settled by testing with actual clinic managers. |
| SR-F02 | The textbook ambiguity example itself — "search" had to be resolved through clarification, the clearest possible proof of iterative refinement. |
| SR-F03 | Daily attendance list — fairly direct from the book, but its exact format/fields are the kind of thing usually tuned with real clinic staff feedback. |
| SR-NF07 | The 2-hour training / 2-error target is a usability goal — usually achieved by testing the UI with real users and adjusting, not fixed on paper on day one. |

## References

- [S5] SlideShare, "Ch 2 Software Engineering"(Sommerville Ch. 2 slides) — https://www.slideshare.net/slideshow/ch-2-software-engineering/91393431
- SlideShare, "Ch2 sw processes" (Sommerville Ch. 2 slides) — https://slideshare.net/software-engineeringbook/ch2-sw-processes
- ian sommerville software engineering (tenth edition) pearson education limited 2016 | PDF - https://www.slideshare.net/slideshow/ian-sommerville-software-engineering-tenth-edition-pearson-education-limited-2016/287925972
- CS 410/510 - Software Engineering class notes - https://cs.ccsu.edu/~stan/classes/CS410/Notes16/02-SoftwareProcesses.html

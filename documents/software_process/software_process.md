### Author PutKakada Seng
### Development Process Model

Important distinction: the book does not state which process model was used to build Mentcare specifically — Mentcare is a requirements case study, not a project-management case study. What follows is the general process-model theory from Sommerville's Chapter 2, applied by reasoning to Mentcare's own characteristics (safety-critical, legally regulated, multi-clinic).

The book states as a general principle: "In practice, most large systems are developed using a process that incorporates elements from all of these [process] models." [S5] It also notes: "The waterfall model is mostly used for large systems engineering projects where a system is developed at several sites. In those circumstances, the plan-driven nature of the waterfall model helps coordinate the work." [S6]

### Stage 1 — Plan-Driven (Waterfall)

Used first, for the core legal, safety, and privacy requirements. These are fixed, externally regulated, and well understood before implementation — exactly the condition under which the book says the waterfall model is appropriate. [S6]

### Stage 2 — Reuse-Oriented

Used for infrastructure — encryption, authentication hardware, server infrastructure — where "the system is assembled from existing components" rather than built from scratch. [S5]

### Stage 3 — Incremental / Agile

Used to refine ambiguous, user-facing behavior — such as resolving what "search" should actually mean — through building a version, testing it with real users, and refining it, which the book describes as the core idea of incremental development: "specification, development and validation are interleaved." [S5]

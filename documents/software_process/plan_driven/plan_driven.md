### Author by Sedtha

## What "plan-driven" means ?

A plan-driven process is one where all activities are planned out in advance, and progress is tracked against that fixed plan, meaning all of the process activities are planned in advance and progress is measured against this plan. This is explicitly contrasted with agile processes, where planning is incremental and it is easier to change the process to reflect changing customer requirements.[S7]

The waterfall model is the classic example of a plan-driven model: it is a plan-driven model with separate and distinct phases of specification and development. Those phases are laid out sequentially: requirements analysis and definition, system and software design, implementation and unit testing, integration and system testing, and operation and maintenance. In principle, each phase must be finished before the next one starts — which is precisely what makes it "plan-driven": you commit to a full plan/specification up front rather than discovering requirements as you go.[S0]

## Why waterfall fits this kind of requirement ?
Sommerville's slides give a specific list of situations where waterfall is the better fit: embedded systems where the software has to interface with hardware systems, critical systems where there is a need for extensive safety and security analysis, and large software systems that are part of broader engineering systems.

UR-F07 (suicide/danger warnings, availability for safe prescribing, patient confidentiality, and the two legal regimes — data protection law and mental health law) map directly onto that "critical systems" category:

They are safety-critical (a failure can mean a missed warning about a dangerous patient, or the wrong medication being prescribed).
They are externally regulated by two established bodies of law that exist independently of the project and don't change based on developer preference or sprint feedback.
They require extensive up-front safety and security analysis — you have to reason about confidentiality, availability, and legal compliance before writing code, not discover the right behavior through iteration, because getting it wrong has legal/clinical consequences, not just a bad user experience.
The tradeoff itself (Section 9: privacy vs. availability) is a design conflict that must be resolved analytically at the specification stage — it's not something you can "iterate toward" safely, since a half-built compromise could leave either patient data exposed or the system unavailable in an emergency.

## Which of our SRS requirements were built this way?
| ID | Requirement | Why Plan-Driven |
|---|---|---|
| SR-F04 | Access control + audit log on every patient data access | Directly required by mental health law (judicial review for sectioning) — a fixed legal obligation |
| SR-F05 | Record consultation notes, diagnoses, and treatments (drug + therapy) | Core clinical record-keeping, specified directly from the book's "individual care management" feature |
| SR-F06 | Record prescribed drug/dose/cost; dosage safety-check | Tied directly to the book's safety requirement — must be correct from day one |
| SR-F08 | Flag suicidal/dangerous patient warning | Same safety-critical reasoning — a book-mandated, non-negotiable requirement |
| SR-NF04 | Clinic availability Mon–Fri, 08:30–17:30 | Operational rule stated directly in the book, fixed from the start |
| SR-NF05 | Patient privacy standard compliance (HStan-03-2006-priv) | External law — non-negotiable, exists independently of the project |
| SR-NF06 | Hospital managers barred from individual patient data | Privacy law, fixed before any design decision was made |

### Reference

-[S0] Sommerville, I. (2016) Software Engineering, 10th Edition, Pearson Education Limited, Bosto

-[S5] SlideShare, "Ch 2 Software Engineering"(Sommerville Ch. 2 slides) — https://www.slideshare.n-et/slideshow/ch-2-software-engineering/91393431

-[S6] SlideShare, “Ch2 sw processes” (Sommerville Ch. 2 slides) — https://slideshare.net/software-engineering-book/ch2-sw-processes

-[S7] Studocu - https://www.studocu.com/row/document/the-university-of-faisalabad/human-computer-interaction/2nd-chp-se-none/19031193

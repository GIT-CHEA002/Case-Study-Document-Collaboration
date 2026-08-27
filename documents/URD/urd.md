### Author: PutKakada Seng

Mentcare System — Requirements Document

A Mental Health Clinic Patient Information System Based on the Mentcare case study — Ian Sommerville, Software Engineering, 10th Edition

0. Gathered Requirements (Combined, Undivided)

This paragraph combines every requirement from the sources below into one raw block, in the order gathered, before any division into categories. Nothing is added beyond what the sources state; wording is paraphrased rather than quoted directly, per copyright limits on reproducing published text.

Mentcare's stakeholders are the patients themselves along with doctors, nurses, medical receptionists, IT staff, medical ethics managers, healthcare managers, and medical records staff. Users need to be able to search the appointment lists across all clinics, not just one, and the system should generate a daily list for each clinic showing which patients are expected to attend that day; every staff member using the system is identified by a unique 8-digit employee number. The system also produces monthly management reports covering how many patients were treated at each clinic, how many entered or left care, how many were legally detained ("sectioned"), and what drugs were prescribed along with their costs — and where a patient is sectioned, the system must ensure the required legal procedures are followed and properly documented. On the non-functional side, the system must be available to all clinics during normal working hours (Monday to Friday, 08:30 to 17:30), with no more than five seconds of downtime in a working day; staff must authenticate themselves using their health authority identity card; and the system must follow the patient privacy provisions set out in the relevant privacy standard. Because some mental illnesses can make a patient suicidal or a danger to others, the system should warn staff wherever it can about potentially dangerous or suicidal patients, and it must also check drug dosage and appropriate medication, since unavailability at the wrong moment could mean the wrong medication gets prescribed. Patient information must stay confidential, disclosed only to authorized medical staff and the patient themselves, with hospital managers explicitly barred from seeing individual patient information; and the system itself runs on Linux servers housed in the health authority's own data centre. [S1, S2, S3, S4]

1. Stakeholders

Patients, doctors, nurses, medical receptionists, IT staff, medical ethics managers, healthcare managers, and medical records staff. [S1]

2. User / Functional Requirements
1. "A user shall be able to search the appointments lists for all clinics." [S2]
2. "The system shall generate each day, for each clinic, a list of patients who are expected to attend appointments that day." [S2]
3. "Each staff member using the system shall be uniquely identified by his or her 8-digit employee number." [S2]
4. The system generates monthly management reports showing the number of patients treated at each clinic, patients entered/left the care system, patients sectioned (legally detained), and drugs prescribed and their costs. [S4]
5. Where patients are dangerous, they may need to be "sectioned" (confined to a secure hospital); the system must support managing detained patients and ensure required legal processes are followed and documented. [S4]
Note on Requirements Ambiguity (a key teaching point in the book)

The word "search" in requirement 1 is deliberately ambiguous: the user's intended meaning was to search across all clinics, while a developer might interpret it as searching within one individual clinic first. This is used in the book to illustrate why user requirements need refining into precise system requirements. [S2]

3. Non-Functional Requirements

Product requirement: "The Mentcare system shall be available to all clinics during normal working hours (Mon–Fri, 0830–17.30). Downtime within normal working hours shall not exceed five seconds in any one day." [S3]

Organizational requirement: "Users of the Mentcare system shall authenticate themselves using their health authority identity card." [S3]

External requirement: "The system shall implement patient privacy provisions as set out in HStan-03-2006-priv." [S2, S3]

Infrastructure: "The Mentcare system shall run on hardware (Linux servers) that is available in the authority's data centre." [S4]

4. Safety Requirements

"The safety implications stem from the fact that some mental illnesses cause patients to become suicidal or a danger to other people. Wherever possible, the system should warn medical staff about potentially suicidal or dangerous patients. Other safety issues concern checking of drug dosage and appropriate medication. The system must be available when needed otherwise safety may be compromised and it may be impossible to prescribe the correct medication to patients." [S4]

5. Privacy Requirements

"As in all medical systems, privacy is a critical system requirement. It is essential that patient information is confidential and is never disclosed to anyone apart from authorized medical staff and the patient themselves. Hospital managers should not have access to individual patient information." [S4]

References
-[S1] Slideserve, "Comprehensive Overview of Software Requirements Engineering" (Sommerville Ch. 4 content) — https://www.slideserve.com/simeone/practical-software-engineering-session-4-powerpoint-ppt-presentation

-[S2] SlidePlayer, "Chapter 4 – Requirements Engineering," CS 425, Oct 2015 (Sommerville Ch. 4 slides) — https://slideplayer.com/slide/8714092/

-[S3] SlidePlayer, "Chapter 4 – Requirements Engineering," CS709, Sep 2017 (Sommerville Ch. 4 slides) — https://slideplayer.com/slide/13561421/

-[S4] GitHub, opendesigncasestudies/Mentcare-IanSommerville — case study text retrieved from Ian Sommerville's Software Engineering, 10th Edition — https://github.com/opendesigncasestudies/Mentcare-IanSommerville (original: Sommerville, I. (2016) Software Engineering, 10th Edition, Pearson Education Limited, Boston)


### Author: PutKakada Seng

MHC-PMS System — Requirements Document

A Mental Health Clinic Patient Information System Based on the Mentcare case study — Ian Sommerville, Software Engineering, 10th Edition

0. Gathered Requirements (Combined, Undivided)

This paragraph combines every requirement from the sources below into one raw block, in the order gathered, before any division into categories. Nothing is added beyond what the sources state; wording is paraphrased rather than quoted directly, per copyright limits on reproducing published text.

Mentcare's stakeholders are the patients themselves along with doctors, nurses, medical receptionists, IT staff, medical ethics managers, healthcare managers, and medical records staff. Users need to be able to search the appointment lists across all clinics, not just one, and the system should generate a daily list for each clinic showing which patients are expected to attend that day; every staff member using the system is identified by a unique 8-digit employee number. The system also produces monthly management reports covering how many patients were treated at each clinic, how many entered or left care, how many were legally detained ("sectioned"), and what drugs were prescribed along with their costs — and where a patient is sectioned, the system must ensure the required legal procedures are followed and properly documented. On the non-functional side, the system must be available to all clinics during normal working hours (Monday to Friday, 08:30 to 17:30), with no more than five seconds of downtime in a working day; staff must authenticate themselves using their health authority identity card; and the system must follow the patient privacy provisions set out in the relevant privacy standard. Because some mental illnesses can make a patient suicidal or a danger to others, the system should warn staff wherever it can about potentially dangerous or suicidal patients, and it must also check drug dosage and appropriate medication, since unavailability at the wrong moment could mean the wrong medication gets prescribed. Patient information must stay confidential, disclosed only to authorized medical staff and the patient themselves, with hospital managers explicitly barred from seeing individual patient information; and the system itself runs on Linux servers housed in the health authority's own data centre. [S1, S2, S3, S4]

1. Stakeholders

Patients, doctors, nurses, medical receptionists, IT staff, medical ethics managers, healthcare managers, and medical records staff. [S1]

2. User / Functional Requirements

UR-F01: The system generates monthly management reports showing the number of patients treated at each clinic, patients entered/left the care system, patients sectioned (legally detained), and drugs prescribed and their costs. [S4]

UR-F02: "A user shall be able to search the appointments lists for all clinics." [S2]

UR-F03: "The system shall generate each day, for each clinic, a list of patients who are expected to attend appointments that day. A user shall be able to search the appointments lists for all clinics." [S2]

UR-F04: Only authorized medical staff shall be able to access a patient's records, and each staff member's actions within the system shall be identifiable and recorded, so that access and decisions can be reviewed later if required by law (e.g. for judicial review in sectioning cases). [S0]

UR-F05: Clinicians can create records for patients, edit information, view
patient history, and so on. The system supports data summaries so that a doctor who has not previously met a patient can quickly learn about key problems and prescribed treatments. [S0]

UR-F06: The system uses a centralized database but is also designed to run on a laptop so it can be accessed from sites without secure network connectivity. When connected, it uses the central database; when disconnected, it downloads and uses local copies of patient records. It is not a complete medical records system — it does not maintain information about other medical conditions — but it may interact and exchange data with other clinical information systems. [S0]

UR-F07: "The safety implications stem from the fact that some mental illnesses cause patients to become suicidal or a danger to other people. Wherever possible, the system should warn medical staff about potentially suicidal or dangerous patients. " [S4]

The word "search" in requirement 1 is deliberately ambiguous: the user's intended meaning was to search across all clinics, while a developer might interpret it as searching within one individual clinic first. This is used in the book to illustrate why user requirements need refining into precise system requirements. [S2]

3. Non-Functional Requirements

UR-NF01: Product requirement: "The Mentcare system shall be available to all clinics during normal working hours (Mon–Fri, 0830–17.30). Downtime within normal working hours shall not exceed five seconds in any one day." [S3]

UR-NF02: Organizational requirement: "Users of the Mentcare system shall authenticate themselves using their health authority identity card." [S3]

UR-NF03: External requirement: "The system shall implement patient privacy provisions as set out in HStan-03-2006-priv." [S2, S3]

UR-NF04: Infrastructure: "The Mentcare system shall run on hardware (Linux servers) that is available in the authority's data centre." [S4]

UR-NF05: Medical staff shall be able to use all the system functions after two hours of training. After this training, the average number of errors made by experienced users shall not exceed two per hour of system use.[S0]

UR-NF06: "As in all medical systems, privacy is a critical system requirement. It is essential that patient information is confidential and is never disclosed to anyone apart from authorized medical staff and the patient themselves. Hospital managers should not have access to individual patient information." [S4]

References
-[S1] Slideserve, "Comprehensive Overview of Software Requirements Engineering" (Sommerville Ch. 4 content) — https://www.slideserve.com/simeone/practical-software-engineering-session-4-powerpoint-ppt-presentation

-[S2] SlidePlayer, "Chapter 4 – Requirements Engineering," CS 425, Oct 2015 (Sommerville Ch. 4 slides) — https://slideplayer.com/slide/8714092/

-[S3] SlidePlayer, "Chapter 4 – Requirements Engineering," CS709, Sep 2017 (Sommerville Ch. 4 slides) — https://slideplayer.com/slide/13561421/

-[S4] GitHub, opendesigncasestudies/Mentcare-IanSommerville — case study text retrieved from Ian Sommerville's Software Engineering, 10th Edition — https://github.com/opendesigncasestudies/Mentcare-IanSommerville (original: Sommerville, I. (2016) Software Engineering, 10th Edition, Pearson Education Limited, Boston)


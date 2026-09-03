### Author: PutKakada Seng

## MHC-PMS System — Requirements Document

A Mental Health Clinic Patient Information System Based on the Mentcare case study — Ian Sommerville, Software Engineering, 10th Edition

## 0. Gathered Requirements (Combined, Undivided)

This paragraph combines every requirement from the sources below into one raw block, in the order gathered, before any division into categories. Nothing is added beyond what the sources state; wording is paraphrased rather than quoted directly, per copyright limits on reproducing published text.

Mentcare is a medical information system that maintains records for patients suffering from mental health problems and the treatments they've received, used in clinics that may be based in hospitals, local medical practices, or community centers rather than only hospitals. [S0] It exists for two purposes: generating management information so health service managers can assess performance against targets, and giving medical staff timely information to support patient treatment. [S0] It uses a centralized database but is also designed to run on a laptop, so it can be used at sites without secure network connectivity — downloading and using local copies of records when disconnected, and syncing when connectivity returns; it is not a complete medical records system, so it doesn't hold information about other medical conditions, though it may exchange data with other clinical systems. [S0] Stakeholders include patients, doctors, nurses, health visitors (nurses who visit patients at home), medical receptionists, medical records staff, administrative staff who generate reports, IT staff, medical ethics managers, and healthcare managers. [S0, S1] Recorded data includes patient details (name, address, age, next of kin) and consultation details (date, doctor seen, subjective impressions), along with conditions and treatments. [S0] Users need to be able to search the appointment lists across all clinics, not just one, and the system generates a daily list for each clinic showing which patients are expected that day; each staff member is identified by a unique 8-digit employee number. [S2] The system has three key features: individual care management, where clinicians create and edit patient records, view history, and get data summaries so an unfamiliar doctor can quickly learn a patient's key problems and treatments; patient monitoring, where the system automatically issues warnings — for example if a patient hasn't seen a doctor in some time — and specifically tracks sectioned (legally detained) patients to ensure required legal checks happen on time; and administrative reporting, generating monthly reports on patients treated per clinic, patients entering/leaving care, patients sectioned, and drug costs. [S0] Because patients can be irrational, may miss appointments, lose medication, or in a minority of cases be a danger to themselves or others, some patients may need to be sectioned — confined to a secure hospital — and two separate laws apply: data protection law governing confidentiality, and mental health law governing compulsory detention, with staff decisions recorded for judicial review if necessary. [S0] On the non-functional side, the system must be available to all clinics during normal working hours (Monday–Friday, 08:30–17:30) with no more than five seconds of downtime in a day, staff must authenticate via their health authority identity card, and it must follow patient privacy provisions. [S3] Patient information must stay confidential, disclosed only to authorized medical staff and the patient themselves, with hospital managers barred from individual patient information; the system is safety-critical, since some mental illnesses make patients suicidal or dangerous, so it should warn staff wherever possible, and must remain available since downtime could mean the wrong medication gets prescribed. [S0] There is a direct conflict between two requirements here: privacy is easiest with a single copy of the data, but availability during server failure or disconnection requires multiple copies. [S0] The system runs on Linux servers in the health authority's data centre. [S4]

## 1. Overview and Purpose

Mentcare is a medical information system that maintains information about patients suffering from mental health problems and the treatments they have received. Most patients attend specialist clinics regularly rather than requiring hospital admission, and these clinics may be held in hospitals, local medical practices, or community centers. [S0]

Two system purposes:

    1. To generate management information allowing health service managers to assess performance against local and government targets.
    2. To provide medical staff with timely information to support the treatment of patients. [S0]

## 2. Stakeholders

.Patients — the individuals whose treatment is recorded
.Doctors and nurses — clinical staff
.Health visitors — nurses who visit patients at home to check on treatment
.Medical receptionists — make appointments
.Medical records staff — maintain the records system
.Administrative staff — generate reports
.IT staff, medical ethics managers, healthcare managers — supporting roles named in secondary course materials [S0, S1]
## 3. User / Functional Requirements

| ID         | Requirement                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Reference Text                                                                                                                                                                                                                                                                                                      |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **UR-F01** | The system shall generate monthly management reports showing the number of patients treated at each clinic, patients entering and leaving the care system, patients who are sectioned (legally detained), and the drugs prescribed together with their costs.                                                                                                                                                                                                                          | [S0] “The system generates monthly reports on patients treated per clinic, patients entering/leaving care, patients sectioned, and drug costs.”                                                                                                                                                                     |
| **UR-F02** | The system shall allow users to search appointment lists across all clinics.                                                                                                                                                                                                                                                                                                                                                                                                           | [S2] “A user shall be able to search the appointments lists for all clinics.”                                                                                                                                                                                                                                       |
| **UR-F03** | The system shall generate, each day for each clinic, a list of patients who are expected to attend appointments that day.                                                                                                                                                                                                                                                                                                                                                              | [S2] “The system shall generate each day, for each clinic, a list of patients who are expected to attend appointments that day.”                                                                                                                                                                                    |
| **UR-F04** | The system shall restrict patient-record access to authorized medical staff and shall identify and record each staff member's actions so that access and decisions can be reviewed when required by law, including judicial review in sectioning cases.                                                                                                                                                                                                                                | [S0] Patient information must remain confidential and may only be disclosed to authorized medical staff and the patient. Staff decisions relating to compulsory detention must be recorded for possible judicial review.                                                                                            |
| **UR-F05** | The system shall allow clinicians to create and edit patient records, view patient history, and access data summaries that allow an unfamiliar doctor to quickly understand a patient's key problems and prescribed treatments.                                                                                                                                                                                                                                                        | [S0] “Individual care management” allows clinicians to create and edit patient records, view history, and obtain data summaries so that an unfamiliar doctor can quickly learn a patient's key problems and treatments.                                                                                             |
| **UR-F06** | The system shall use a centralized database while also supporting operation on a laptop at sites without secure network connectivity. When connected, the system shall use the central database; when disconnected, it shall allow local copies of patient records to be downloaded and used and synchronized when connectivity returns. The system shall not maintain complete medical records for other medical conditions but may exchange information with other clinical systems. | [S0] The system uses a centralized database and can run on a laptop at sites without secure network connectivity. Local copies of records can be used while disconnected and synchronized when connectivity returns. It is not a complete medical records system but may exchange data with other clinical systems. |
| **UR-F07** | The system shall warn medical staff, wherever possible, about patients who may be suicidal or dangerous to themselves or other people.                                                                                                                                                                                                                                                                                                                                                 | [S0] The system is safety-critical because some mental illnesses may cause patients to become suicidal or dangerous to others, so the system should warn medical staff wherever possible.                                                                                                                           |

### Requirement Clarification

**UR-F02** deliberately uses the word **“search”** because the original user requirement is ambiguous. The intended meaning is that users should be able to search appointment lists **across all clinics**, rather than being limited to a single clinic. This illustrates the importance of refining ambiguous user requirements into precise system requirements. [S2]

---

## 4. Non-Functional Requirements

| ID          | Requirement                                                                                                                                                                                                                          | Reference Text                                                                                                                                                                                                           |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **UR-NF01** | **Product Requirement:** The Mentcare system shall be available to all clinics during normal working hours, Monday to Friday from 08:30 to 17:30. Downtime during normal working hours shall not exceed five seconds in any one day. | [S3] “The Mentcare system shall be available to all clinics during normal working hours (Mon–Fri, 0830–17.30). Downtime within normal working hours shall not exceed five seconds in any one day.”                       |
| **UR-NF02** | **Organizational Requirement:** Users of the Mentcare system shall authenticate themselves using their health authority identity card.                                                                                               | [S3] “Users of the Mentcare system shall authenticate themselves using their health authority identity card.”                                                                                                            |
| **UR-NF03** | **External Requirement:** The system shall implement patient privacy provisions in accordance with HStan-03-2006-priv.                                                                                                               | [S2, S3] “The system shall implement patient privacy provisions as set out in HStan-03-2006-priv.”                                                                                                                       |
| **UR-NF04** | **Infrastructure Requirement:** The Mentcare system shall run on Linux server hardware available in the health authority's data centre.                                                                                              | [S4] “The Mentcare system shall run on hardware (Linux servers) that is available in the authority's data centre.”                                                                                                       |
| **UR-NF05** | Medical staff shall be able to use all system functions after two hours of training. Following this training, the average number of errors made by experienced users shall not exceed two errors per hour of system use.             | [S0] Medical staff should be able to use all system functions after two hours of training, and experienced users should make no more than two errors per hour after training.                                            |
| **UR-NF06** | Patient information shall remain confidential and shall not be disclosed to anyone except authorized medical staff and the patients themselves. Hospital managers shall not have access to individual patient information.           | [S0] Patient information must remain confidential and must never be disclosed to anyone other than authorized medical staff and the patient. Hospital managers should not have access to individual patient information. |

---

## Reference Mapping

| Requirement | Source   |
| ----------- | -------- |
| **UR-F01**  | [S0]     |
| **UR-F02**  | [S2]     |
| **UR-F03**  | [S2]     |
| **UR-F04**  | [S0]     |
| **UR-F05**  | [S0]     |
| **UR-F06**  | [S0]     |
| **UR-F07**  | [S0]     |
| **UR-NF01** | [S3]     |
| **UR-NF02** | [S3]     |
| **UR-NF03** | [S2, S3] |
| **UR-NF04** | [S4]     |
| **UR-NF05** | [S0]     |
| **UR-NF06** | [S0]     |


## References

-[S0] Sommerville, I. (2016) Software Engineering, 10th Edition, Pearson Education Limited, Boston

-[S1] Slideserve, "Comprehensive Overview of Software Requirements Engineering" (Sommerville Ch. 4 content) — https://www.slideserve.com/simeone/practical-software-engineering-session-4-powerpoint-ppt-presentation

-[S2] SlidePlayer, "Chapter 4 – Requirements Engineering," CS 425, Oct 2015 (Sommerville Ch. 4 slides) — https://slideplayer.com/slide/8714092/

-[S3] SlidePlayer, "Chapter 4 – Requirements Engineering," CS709, Sep 2017 (Sommerville Ch. 4 slides) — https://slideplayer.com/slide/13561421/

-[S4] GitHub, opendesigncasestudies/Mentcare-IanSommerville — case study text retrieved from Ian Sommerville's Software Engineering, 10th Edition — https://github.com/opendesigncasestudies/Mentcare-IanSommerville (original: Sommerville, I. (2016) Software Engineering, 10th Edition, Pearson Education Limited, Boston)


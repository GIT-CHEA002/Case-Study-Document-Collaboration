# Use Case Diagram Documentation

This Use Case Diagram outlines the functional boundaries of the system, detailing how various actors interact with core processes while capturing non-functional constraints.

## System Actors

* **Staff Member:** Searches appointments and accesses patient data.
* **Clinician:** Manages consultations, diagnoses, treatments, and prescriptions.
* **Hospital Manager:** Views aggregated management data only.
* **System Administrator:** Generates reports and manages system-related operations.
* **Health Authority Smart Card:** Authenticates staff members.
* **External Clinic System:** Synchronizes offline records with the main system.

---
The Use Case Diagram provides a high-level overview of the Healthcare Patient Management System. It identifies the main actors who interact with the system and the major functions available to each actor.

The diagram shows interactions between Staff Members, Clinicians, Hospital Managers, System Administrators, and the Health Authority Smart Card. It covers functions such as authentication, appointment searching, patient record access, consultation management, prescription management, dosage checking, reporting, and offline synchronization.

This diagram primarily represents SR-F01 through SR-F07 and also illustrates important constraints from SR-NF02 and SR-NF06, particularly smart-card authentication and restricted access to identifiable patient information.

Related Requirements: SR-F01, SR-F02, SR-F03, SR-F04, SR-F05, SR-F06, SR-F07, SR-NF02, SR-NF06.
> **Scope Note:** This diagram focuses primarily on **Functional Requirements** (direct interactions and workflows). **Non-Functional Requirements** (security standards, system performance, and compliance) are integrated as visual constraints and annotations, as NFRs do not represent primary user use cases.
![Alt Text](./usecase.png)
  # SRS Documentation By Sokchea
  # 4. System Requirements Specification (SRS)

    Each SRS item expands a URD item into a precise, unambiguous, verifiable statement — removing any interpretation gap (e.g. URD 3.1-1's "search" is ambiguous about scope; SR-F02 below resolves it explicitly).
  --- 

  ## 4.1 Functional Requirements (FR)

  | ID | Requirement | Traces to URD |
  |---|---|---|
  | **SR-F01** | The system shall generate a Monthly Drug Cost Report, aggregating prescription cost and dose-unit data, produced automatically at 17:30 on the last working day of each month. | 3.1-6 |
  | **SR-F02** | The system shall allow staff to search for appointments by patient name **across all clinics simultaneously**, not restricted to a single pre-selected clinic. | 3.1-1 |
  | **SR-F03** | The system shall generate, each day and for each clinic, a list of patients expected to attend appointments that day. | 3.1-4 |
  | **SR-F04** | The system shall enforce access control on every data request and record an audit log entry for each access to patient data (staff member, timestamp, action). | 3.2-1, 3.2-3 |
  | **SR-F05** | The system shall allow clinicians to record and update patient consultation notes, diagnoses, and treatments — both pharmacological and therapy-based. | 3.1-2, 3.1-3 |
  | **SR-F06** | The system shall record prescribed drug name, dose unit, total doses, and unit cost per prescription, and support a dosage-check against known safe ranges. | 3.1-7 |
  | **SR-F07** | The system shall support local, offline access to a downloaded copy of patient records at sites without secure network connectivity, syncing once connectivity is restored. | 3.1-8 |

  ## 4.2 Non-Functional Requirements (NFR)

  | ID | Requirement | Category |
  |---|---|---|
  | **SR-NF01** | The application cluster shall maintain **99.99% uptime Mon–Fri**, with automatic failover to a standby node within **5 seconds** of primary node failure. | Product (availability) |
  | **SR-NF02** | Each staff member shall authenticate using a Health Authority smart card, which validates the card and extracts the staff member's unique **8-digit employee ID**. | Organizational (security) |
  | **SR-NF03** | All patient data shall be encrypted in transit (**TLS 1.3**) and at rest (**AES-256 column-level encryption**). | Product (security/privacy) |
  | **SR-NF04** | The system shall be available to all clinics **Mon–Fri, 08:30–17:30**. Downtime within working hours shall not exceed **5 seconds in any one day**. | Product (availability) |
  | **SR-NF05** | The system shall implement patient privacy provisions per the applicable patient privacy standard (**HStan-03-2006-priv**). | External (legal/regulatory) |
  | **SR-NF06** | Hospital managers shall not have access to individual, identifiable patient information — only aggregated/management-level data. | Organizational (privacy) |
  | **SR-NF07** | New staff shall learn core functions within **2 hours of training**, with a target error rate of no more than **2 errors/hour thereafter**. | Product (usability) |
  | **SR-NF08** | The system shall run on the health authority's designated data centre infrastructure (**Linux-based servers**). | External (infrastructure) |
  ---
  ## 4.3 Relationship Between Functional and Non-Functional Requirements
  Not every FR has an associated NFR. Where one does apply, the FR must satisfy that constraint at all times — the relationship is not optional once established. For example, SR-F04 (access control/audit logging) is governed by SR-NF02 (smart card authentication) and SR-NF03 (encryption): the action of accessing data is functional, but the rules under which it's permitted are non-functional constraints layered on top.

  A single NFR can also govern multiple FRs through different mechanisms depending on data state — SR-NF03 is satisfied via TLS 1.3 (in transit) and AES-256 (at rest): two mechanisms, one underlying privacy rule.
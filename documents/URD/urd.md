### Author: PutKakada Seng

# Mentcare System — User Requirements Document (URD)

*A Mental Health Clinic Patient Information System*
*Based on the Mentcare case study — Sommerville, Software Engineering, 10th Edition*

---

## 0. Requirements Gathered from Stakeholders (Narrative Form)

> "Our clinicians need to be able to record everything about a patient's mental health treatment in one place — not just the medication they're on, but the therapy and consultation notes too, since most patients get a mix of both. Staff often need to find a patient's appointment quickly, and they shouldn't have to already know which clinic that patient is registered at — they just want to search once and see everything. Every morning, each clinic needs a list of who's expected that day, because patients with mental health conditions don't always attend reliably, and staff need to plan around that. When it comes to medication, we need the system to catch mistakes — wrong doses, or medication that shouldn't be combined — because a mistake here isn't just inconvenient, it can genuinely put a patient at risk. Management also needs a monthly picture of what we're spending on drugs across all clinics, so they can plan budgets, but that's a separate concern from the day-to-day clinical work. Because this is mental health data, it's more sensitive than ordinary medical records — it should only be seen by the clinical staff actually treating that patient, and never by hospital managers, who should only see aggregated numbers, not individual files. Staff should have to prove who they are before touching any of this data, and every time someone looks at a record, that access should be logged, in case it's ever questioned. If a patient shows signs of being a danger to themselves or others, the system should flag that clearly so staff don't miss it. And whatever system we get, it needs to actually be up and running when the clinic is open — if it goes down mid-appointment, that's a real problem, not just an annoyance. Finally, new staff shouldn't need weeks of training just to use it — they should be productive within a couple of hours."

This raw narrative is the starting point of requirements elicitation. It mixes functional needs, non-functional constraints, priorities, and justifications together, exactly as a stakeholder would say them. The requirements in Section 3 below are derived directly from this paragraph, separated into discrete, plain-language statements.

---

## 3. User Requirements Document (URD)

### 3.1 Functional User Requirements

1. A user shall be able to search the appointment lists for all clinics.
2. Clinicians shall be able to create and maintain patient consultation and treatment records.
3. The system shall support recording of both drug-based (pharmacological) and non-drug (therapy-based) treatments for a patient.
4. Staff shall be able to view a list of patients expected to attend each clinic on a given day.
5. The system shall generate letters and reports required for patient care and legal compliance.
6. Health care managers shall be able to obtain a report of drug costs, to support budgeting and management decisions.
7. The system shall record prescribed medication and support checking of drug dosage and appropriate medication.
8. The system shall be usable at clinic sites that do not have reliable network connectivity, with local record access when disconnected.
9. The system shall cope with patient unpredictability, such as irregular attendance at clinic sessions.

### 3.2 Non-Functional User Requirements

1. Patient information must be kept confidential and must not be disclosed to anyone other than authorized medical staff and the patient themselves.
2. The system must be available to clinics during normal working hours, with minimal unplanned downtime.
3. Only authorized staff shall be able to access the system, verified through a secure method of identification.
4. The system shall warn medical staff about potentially suicidal or dangerous patients.
5. The system shall comply with applicable mental health legislation and patient privacy standards.
6. New staff should be able to learn the core functions of the system within a short training period.

---

*Note: This document covers User Requirements (URD) only. The System Requirements Specification (SRS), which expands each item above into precise, verifiable technical requirements, is maintained separately.*

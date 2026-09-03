# How Does Agile Relate to Mentcare?

Mentcare serves many different user groups: doctors, nurses, administrative staff, record managers, and system administrators. Each group has different working methods and needs. Therefore, it is difficult to write a complete set of requirements from the start and keep them unchanged until the system is complete.

For example, the initial requirement might simply say:

> “The system should provide a summary of a patient's record.”

Developers might understand that creating a page displaying diagnosis, medication, and consultation history is sufficient. But when doctors actually use it, they might respond that the most important information should be **current medication, allergies, suicide risk, and violence risk**, while the patient history could be placed below.

Thus, Agile creates the following cycle:

```text
Requirement
    ↓
Prototype / Increment
    ↓
Clinical Use
    ↓
Feedback
    ↓
Refined Requirement
    ↓
Improved Increment
```

The key point is that requirements are not just written on paper but are validated through real-world use.

---

# Where Is Agile Used in Mentcare?

Agile is particularly suitable for areas where the best implementation method cannot be fully determined from the outset.

## 1. Patient Search

The clearest example is **Patient Search**. The initial requirement might simply be:

> “Search for a patient.”

But reality raises many questions:

- Should users search by name or patient code?
- What if there are two patients with the same name?
- Is a date of birth required?
- Should a photo or the current clinic be displayed?
- Which users are allowed to search the entire database?

The development team can build a simple version first, allow doctors and clinic staff to use it, and then adjust it based on feedback.

## 2. Patient Summary

Another example is **Patient Summary**.

Developers can design a summary containing all the necessary information, but doctors do not need “everything”; they need the **most important information within seconds**.

Agile helps determine that priority through real-world testing.

For example, clinicians may decide that the most important information should appear first:

- Current medication
- Allergies
- Suicide risk
- Violence risk
- Recent diagnosis
- Important clinical warnings

Less urgent historical information can be placed further down or accessed when needed.

## 3. Daily Attendance Lists and Missed Appointment Monitoring

The same approach applies to **Daily Attendance Lists** and **Missed Appointment Monitoring**.

Initially, the system might only display the names of patients who missed appointments. But after real use, nurses may request additional information such as:

- Risk level
- Number of missed appointments
- Assigned clinician
- Contact information
- Last consultation date
- Follow-up priority

Such details typically become clear only when users interact with the system in real-world scenarios.

## 4. Management Reporting

**Management Reporting** is also well-suited to Agile.

A manager might initially request a medication cost report. After testing the first version, they may want the report to be categorized by:

- Clinic
- Month
- Dosage
- Drug group
- Treatment unit
- Patient category

Instead of trying to predict every reporting requirement from the beginning, Agile allows the team to build reports step by step and refine them based on management feedback.

---

# Key Idea

Agile is valuable in Mentcare because it supports continuous refinement of requirements through real user feedback.

The relationship can be summarized as:

```text
Clinical Need
    ↓
Initial Requirement
    ↓
Working Increment
    ↓
Doctor / Nurse Feedback
    ↓
Requirement Refinement
    ↓
Improved Mentcare Function
```

In simple terms:

> **Agile helps Mentcare evolve according to real clinical needs instead of assumptions made only by developers.**

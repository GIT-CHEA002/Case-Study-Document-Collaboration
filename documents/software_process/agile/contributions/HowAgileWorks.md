# How Does Agile Work in Mentcare?

Let us take the **Risk Warning** function as an example.

Initially, the clinician says:

> “We need to know whether a patient may be dangerous to themselves or others.”
  
The development team converts this need into a **User Story** and places it in the **Product Backlog**:
  
> “As a clinician, I want to see a patient's risk status so that I can make safer clinical decisions.”

In the first Sprint, the team builds a simple **Risk Indicator**.

The doctor tests it and provides feedback: 

> “The warning is difficult to notice.”

In the next Sprint, the team moves the warning to the **Patient Summary**.

Then the clinician provides additional feedback:

> “High-risk patients should be immediately distinguishable from normal-risk patients.”

The team continues to improve the feature based on real clinical feedback.

The Agile process can be visualized as follows:

```text
Clinical Need
    ↓
User Story
    ↓
Product Backlog
    ↓
Sprint
    ↓
Working Feature
    ↓
Doctor / Nurse Review
    ↓
Feedback
    ↓
Requirement Refinement
    ↓
Next Sprint
```

This is a practical example of **Agile applied to Mentcare**.

---

# Agile Helps Prioritize Functions

Another important advantage of Agile is **prioritization**.

Mentcare contains many functions, but not every function has the same clinical importance or safety impact.

The development team can therefore prioritize features based on value and risk.

## High Priority

- Patient Search
- Patient Summary
- Medication Information
- Allergy Warning
- Risk Status

## Medium Priority
 
- Missed Appointment Monitoring
- Reports

## Lower Priority

- Interface improvements
- Advanced reporting
- Additional convenience features

This approach helps the team focus development resources on features that provide the highest **clinical value** and have the greatest **safety impact**.

---

# Agile Helps Identify Incorrect or Incomplete Requirements

A requirement may sound reasonable when written on paper, but problems may only become visible when users interact with the system.

For example:

> “Display the complete patient history.”

At first, this seems useful.

However, if a patient has been treated for ten years, the doctor may have to read hundreds of records before finding the most important information.

After testing the system, the requirement could be refined to:

> **Display a concise clinical summary first and provide access to the complete history when required.**

Agile helps move requirements from:

> **“What we think users need”**

to:

> **“What users actually need.”**

This is one of the most important contributions of Agile to **Requirements Engineering**.

---

# Agile Cannot Be Applied Uniformly to All Parts of Mentcare

Agile is highly suitable for areas related to:

- Usability
- User Interface
- Clinical Workflow
- Reporting
- Information Presentation
- Search Functions
- User Interaction

However, some Mentcare requirements cannot be changed freely from Sprint to Sprint.

Examples include:

- Patient Privacy
- Access Control
- Legal Compliance
- Patient Safety
- Authentication
- Auditability
- Security Requirements
- Data Integrity

These requirements need stronger control because errors can create serious clinical, legal, or security risks.

For example, the team cannot say:

> “We have not implemented security in this Sprint. We will do it in the next Sprint.”

If **Patient Records** already exist, access control and privacy protection must be considered from the beginning.

---

# A More Practical Approach

A better approach for Mentcare is:

> **Agile Development + Strong Safety/Security Engineering**

This can also be described as a:

> **Hybrid Agile Approach**

In this approach:

## Agile Is Responsible for

- Adaptability
- Iterative development
- Continuous feedback
- Requirement refinement
- Incremental delivery
- Workflow improvement

## Engineering Controls Are Responsible for

- Patient safety
- Security
- Privacy
- Access control
- Legal compliance
- Auditability
- Verification
- Traceability

The relationship can be summarized as:

```text
        AGILE
          ↓
Adaptability + Feedback
          +
   ENGINEERING CONTROLS
          ↓
Safety + Security + Compliance
          =
      MENTCARE
```

---

# Key Conclusion

Agile is valuable in Mentcare because it allows user-facing requirements to evolve through real clinical feedback.

However, Agile cannot replace the strict engineering practices required for safety, privacy, security, and legal compliance.

A useful summary is:

> **Agile provides flexibility, while engineering controls provide safety and security.**

Or more simply:

> **Mentcare should be adaptable, but never uncontrolled.**

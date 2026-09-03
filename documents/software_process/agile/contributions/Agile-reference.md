  # Agile and Mentcare (MHC-PMS)

The relationship between Agile methodologies and mental health patient management systems like MHC-PMS (Mentcare) reflects the intersection – and conflict – between "agile software development" and "safety-critical systems."

Overall, this relationship is expressed through two core aspects: the limitations of pure Agile and the evolution into regulated Agile.

## 1. Limitations of Pure Agile for Mentcare

* **Documentation and Legal Aspects:** The guiding principle of Agile is "Working software is worth more than complete documentation." However, Mentcare stores sensitive mental health data, subject to strict government oversight. The system cannot be licensed without a detailed set of specifications (SRS), risk analysis documents, and audit trail logs.
* **Emergent Architecture:** Agile allows the system architecture to change and improve gradually through Sprints. For Mentcare, this is a critical risk. Security ACL and safety alerts must be designed and defined from the outset. Refactoring a medical data security vulnerability in later iterations is illegal.

## 2. Practical Value of Agile in Mentcare

While pure Agile cannot be used, Agile engineering practices provide immense value in ensuring the "dependability" of the healthcare system:

* **Continuous Testing & TDD:** Test-Driven Development minimizes software errors that could endanger patients' lives.
* **Continuous Integration/Continuous Deployment (CI/CD):** Ensuring that every new piece of code added to the Mentcare system passes automated security and functional tests before deployment.

---

## References

### Quotations from reputable academic sources and international standards

To demonstrate the above connection, here are the perspectives and practical standards being applied worldwide to healthcare software like Mentcare:

* **Textbook "Software Engineering" (10th Edition) - Professor Ian Sommerville:**
  The author of the Mentcare case study himself stated in his book that Agile is not suitable for developing entire critical security systems. He proposed a hybrid approach. In this approach, the risk analysis and security architecture design phases should use a Plan-driven/Waterfall method, while Agile techniques (such as iterative development, continuous integration) are used in the programming phase to minimize errors.

* **International Standard IEC 62304 (Medical Device Software – Software Life Cycle Processes):**
  This is a global standard for the development lifecycle of medical software. While it doesn't prohibit Agile, it strictly stipulates that any agile process must ensure 100% traceability. This means that every line of code written in a Sprint must be traceable back to its resolution of a specific system risk, and documentation must be updated simultaneously.

* **AAMI TIR45 Document (Recognized by the US Food and Drug Administration - FDA):**
  The document "Guidelines for Using Agile Practices in Medical Device Software Development" indicates that development teams can absolutely use Scrum or Kanban. However, it must be wrapped in a tightly controlled process "shell" (often called Water-Scrum-Fall). This framework requires safety reviews (gates) before release.

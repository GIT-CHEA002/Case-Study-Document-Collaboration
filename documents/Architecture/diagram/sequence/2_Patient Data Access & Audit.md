## Sequence Diagram — Patient Data Access and Audit

The Patient Data Access Sequence Diagram shows how the system handles a request to access patient information.

When a staff member requests patient data, the system first sends the request to the Access Control component. If authorization is granted, the system retrieves the requested information from the patient database and records an audit entry containing the staff member's identity, timestamp, and action.

If authorization is denied, the system does not return the patient information and records the denied access attempt.

This diagram demonstrates how access control and auditing are applied to every patient-data request, directly satisfying the requirements of SR-F04.

Related Requirements: SR-F04, SR-NF02, SR-NF03.
![patient data access and audit]('./2_Patient Data Access & Audit.png')
## Sequence Diagram — Smart Card Authentication

The Smart Card Authentication Sequence Diagram illustrates the interaction between a staff member, the smart-card reader, the healthcare system, the Health Authority authentication service, and the staff database.

The staff member inserts a Health Authority smart card, after which the system validates the card and retrieves the staff member's unique 8-digit employee ID. If the card is valid, the system retrieves the user's role and permits access. If authentication fails, access is denied and the event is recorded.

This diagram provides a dynamic representation of SR-NF02 and demonstrates how authentication forms the foundation for the access-control requirement in SR-F04.

Related Requirements: SR-NF02, SR-F04.
![smart card authentication]('./1_Smart Card Authentication.png')
## Sequence Diagram — Offline Synchronization
---
The Offline Synchronization Sequence Diagram illustrates the interaction between a clinic device, local storage, the synchronization service, the central server, and the central patient database.

When network connectivity is unavailable, patient records are accessed from local storage. Changes made by authorized staff are stored locally. When connectivity is restored, the synchronization service sends the changes to the central server, where they are validated and applied to the central patient database.

After successful synchronization, the local records are marked as synchronized and the synchronization event is recorded in the audit log.

This diagram provides a detailed interaction model for SR-F07.

Related Requirements: SR-F07, SR-F04.
![Offline Sync](./4_Offline%20Sync.png)
## State Machine Diagram — Patient Record Synchronization
---
The State Machine Diagram represents the different states of a patient record when the system operates with offline access.

A record initially exists in the central system and can be downloaded to a clinic. When network connectivity is unavailable, the record enters an offline state. If staff modify the record, it becomes a modified record and is then placed into a pending synchronization state.

When network connectivity is restored, synchronization begins. A successful synchronization changes the record to the synchronized state, while a failed synchronization returns it to the pending state so that synchronization can be attempted again.

This diagram provides a clear representation of the state transitions required by SR-F07.

Related Requirements: SR-F07, SR-F04.
![patient record sync](./Patient20%Record20%Synchronization.png)
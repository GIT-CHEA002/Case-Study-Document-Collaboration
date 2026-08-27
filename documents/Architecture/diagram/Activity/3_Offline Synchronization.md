## Activity Diagram — Offline Synchronization
---
The Offline Synchronization Activity Diagram illustrates how authorized staff can access patient records when a clinic does not have secure network connectivity.

When the network is unavailable, the system uses a locally downloaded copy of patient records. Authorized staff can access and update these records locally. Once network connectivity is restored, the system validates and synchronizes the local changes with the central patient database.

If synchronization fails, the changes remain stored locally and can be synchronized again later. This ensures that patient-record operations can continue during temporary network outages.

This diagram directly represents SR-F07 and supports the availability and operational requirements associated with SR-NF04.

Related Requirements: SR-F07, SR-NF04.
![ Offline sychronization ](./3_Offline%20Synchronization.png)
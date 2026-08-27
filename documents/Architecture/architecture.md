# MHC-PMS System Architecture

## 1. Overview

The Mental Health Care Patient Management System (MHC-PMS) uses a distributed client-server architecture that combines centralized data management with standalone local systems.

The main components are:

- Local Systems
- Central Server
- Central Database
- Network / Synchronization Service

This architecture is designed to support mental health care organizations that may operate across multiple clinics and community facilities.

## 2. Architecture Components

### 2.1 Local Systems

Local systems are computers or applications used by staff at individual clinics.

They allow authorized users to:

- Register patients
- Manage appointments
- View locally available patient information
- Record approved clinical information
- Continue essential operations when the network is unavailable

### 2.2 Central Server

The central server acts as the main communication and application layer.

It is responsible for:

- Authentication
- Authorization
- Business rules
- Processing requests
- Synchronization
- Communication with the central database
- Audit logging

### 2.3 Central Database

The central database stores shared system information such as:

- Patient records
- Appointments
- Assessments
- Treatment plans
- Progress information
- Medication records
- User accounts
- Audit records

### 2.4 Network and Synchronization

The network allows local systems to communicate with the central server.

When connectivity is available, local changes can be synchronized with the central system.

When connectivity is unavailable, approved local operations can continue using locally available data.

After the connection is restored, the system synchronizes eligible changes with the central server.

## 3. Data Flow

The normal data flow is:

Local System → Central Server → Central Database

For example, when a clinician searches for a patient:

1. The clinician enters the patient ID.
2. The local system sends the request to the server.
3. The server verifies the user's authorization.
4. The server requests the patient's information from the database.
5. The database returns the information.
6. The server sends the result to the local system.
7. The clinician views the permitted information.

## 4. Network Failure

If the network connection is unavailable, the local system should not necessarily stop all operations.

The system can continue defined essential operations using locally available data.

Changes made while offline can be stored locally and queued for synchronization.

When the network connection is restored:

Local System → Synchronization → Central Server → Central Database

The system should detect synchronization conflicts if multiple locations modify the same information while offline.

## 5. Advantages

- Supports multiple clinics
- Centralizes important information
- Supports local operation during network failures
- Allows synchronization between locations
- Supports centralized reporting
- Improves availability
- Provides a foundation for access control and auditing

## 6. Architectural Risks

### Network Failure

A network outage can prevent access to information that is not available locally.

### Synchronization Conflict

Two clinics may modify the same patient record while offline.

### Security Risk

Patient information is highly sensitive and requires strong authentication, authorization, encryption, and auditing.

### Local Data Exposure

Patient information stored on local systems must be protected against unauthorized access or device loss.
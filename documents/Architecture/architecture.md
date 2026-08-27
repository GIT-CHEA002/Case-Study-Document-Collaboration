# MHC-PMS Architecture and Scope Constraints

## 1. Architecture Overview

The Mental Health Care Patient Management System (MHC-PMS) uses a **centralized database architecture** while also supporting operation on individual laptops. This design allows the system to be used in different healthcare locations, including sites where there is no secure or reliable network connection.

When a network connection is available, the local system communicates with the central database. This allows patient information to be accessed and updated through the centralized system.

When the system is disconnected from the network, it can continue to operate using local copies of patient records that have previously been downloaded. This allows healthcare staff to continue accessing necessary patient information even when network connectivity is unavailable.

The architecture therefore combines centralized data management with local/standalone operation.

## 2. Main Architecture Components

### Local System

The local system runs on a laptop or computer at a healthcare site. It allows authorized healthcare staff to access and work with patient information.

When the network is unavailable, the local system can use locally stored copies of patient records.

### Central Database

The central database provides the main storage for MHC-PMS patient information. When the system is connected to the network, local systems communicate with the central database.

### Network Connection

The network provides communication between local systems and the centralized database.

When the connection is available:

Local System → Central Database

When the connection is unavailable:

Local System → Local Copy of Patient Records

### Synchronization

When connectivity is restored, locally stored information can be exchanged with the central system so that the local and centralized information can be brought up to date.

## 3. Data Flow

The basic operation can be represented as:

    Connected Mode

    Local System
          ↓
       Network
          ↓
    Central Database


    Disconnected Mode

    Local System
          ↓
    Local Patient Records

The architecture allows the system to continue providing access to patient information even when a secure network connection is not available.

## 4. Scope Constraints

MHC-PMS is **not intended to be a complete medical records system**.

The system focuses specifically on the management of information related to mental health care. It does not maintain information about a patient's other medical conditions.

However, MHC-PMS may interact with and exchange data with other clinical information systems when information from those systems is required.

Therefore, the scope of MHC-PMS can be summarized as:

- Focuses on mental health care information.
- Uses a centralized database.
- Supports operation on local laptops.
- Can operate using local copies of patient records when disconnected.
- Can exchange information with other clinical information systems.
- Does not maintain complete records of all medical conditions.

## 5. Why This Architecture Is Important

The combination of centralized and local operation is important because mental healthcare can be provided at different locations, including sites where secure network connectivity may not always be available.

A purely centralized system would depend heavily on continuous network connectivity. If the connection failed, staff could lose access to information stored only on the central system.

By supporting local copies of patient records, MHC-PMS can provide greater availability while still maintaining a centralized source of information when connectivity is available.

## 6. Reference

Sommerville, I. (2016). *Software Engineering* (10th ed.). Pearson.

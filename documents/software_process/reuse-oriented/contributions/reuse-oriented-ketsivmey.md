Author by Kakada Seng — matching Sedtha's format exactly.

### What the model is, per the source

Sommerville defines three basic process models — waterfall, incremental development, and reuse-oriented (also called integration/configuration). The reuse-oriented model works by assembling a system from existing components, COTS (commercial off-the-shelf) systems, or software services, rather than developing every part of the system from scratch. [S5]

This is explicitly different from both waterfall and incremental development: those two describe *how* you build custom software (in sequence, or in interleaved versions), while reuse-oriented development describes *where the software comes from* — integrating and configuring things that already exist, rather than writing them.

### Why the source says this model fits infrastructure

Sommerville's own reasoning for reuse-oriented development centers on avoiding unnecessary, risky, and costly custom engineering when a proven solution already exists. Two points map directly onto Mentcare's infrastructure needs:

* **Reduced development cost and risk:** building your own encryption engine, your own authentication protocol, or your own failover clustering system from first principles would take far longer and carry far more risk of subtle security bugs than integrating existing, already-tested, industry-standard components.
* **Faster time to a working system:** because the components already exist and are proven, the team spends its effort on *configuration and integration* — connecting Mentcare's core application to a smart card reader, a TLS library, a Linux server cluster — rather than *inventing* those pieces.

Both reasons matter more, not less, for safety-critical infrastructure like Mentcare's: a custom-built encryption or failover system would need extensive independent security validation before anyone could trust it, whereas TLS 1.3, AES-256, and standard clustering software already carry that validation from widespread real-world use.

### Applied to Section 5.4 (Infrastructure Requirements)

| ID | Requirement | Why Reuse-Oriented |
| :--- | :--- | :--- |
| **SR-F07** | Offline/local sync of patient records at low-connectivity sites | Built on existing database replication/sync technology (e.g. logical replication, offline-first sync frameworks) rather than a custom-built sync protocol |
| **SR-NF01** | 99.99% uptime with 5-second automatic failover | Standard high-availability clustering pattern (load balancer + standby node + heartbeat check), available as existing infrastructure software |
| **SR-NF02** | Smart card authentication, 8-digit employee ID extraction | Off-the-shelf smart card hardware and authentication protocol, not custom-built |
| **SR-NF03** | TLS 1.3 (in transit) and AES-256 (at rest) encryption | Existing, industry-standard cryptographic libraries — already validated, not developed in-house |
| **SR-NF08** | Linux-based data centre infrastructure | Existing operating system and data-centre hardware/hosting, not built by the Mentcare team |

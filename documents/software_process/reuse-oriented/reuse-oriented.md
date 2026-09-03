### Author by Sao Sothea

## What "reuse-oriented" means ?

A reuse-oriented process is one where the system is developed by assembling and integrating components that already exist — off-the-shelf systems, software services, or program libraries — rather than writing every part from scratch, which is what makes it fundamentally different from both waterfall and agile. Sommerville names this as one of the three basic process models, alongside the waterfall (plan-driven) model and incremental development. [S5]

This model is a systematic reuse approach where systems are integrated from existing components or COTS (commercial off-the-shelf) systems. Unlike plan-driven development, where the team designs and builds every requirement into new code following a fixed specification, reuse-oriented development treats a large part of the requirement as already solved — the engineering task shifts from *building* to *configuring and integrating*.

## Why reuse-oriented fits this kind of requirement ?

Sommerville's own case for reuse-oriented development rests on two practical points that carry extra weight for infrastructure like Mentcare's: [S5]

Reduced development risk, since integrating an already-proven, widely used component avoids the risk of subtle bugs that come with writing brand-new, unvalidated code — and this matters more, not less, for security-critical infrastructure, where an in-house-built encryption or authentication system would need extensive independent validation before anyone could trust it with patient data.

More effective use of development resources, since the team's time goes toward configuration and integration testing rather than reinventing solved engineering problems, freeing effort for the parts of Mentcare that actually are unique to a mental health clinic (like the clinical record-keeping and safety-flag logic covered under plan-driven).

Mentcare's infrastructure requirements — encryption, authentication hardware, server clustering, offline sync — are not unique to Mentcare or to healthcare; they're general-purpose engineering problems that the wider software industry has already solved and hardened through years of real-world use, which is exactly the condition under which the book favors reuse over custom-building.

## Which of our SRS requirements were built this way?

| ID | Requirement | Why Reuse-Oriented |
|---|---|---|
| SR-F07 | Offline/local sync of patient records at low-connectivity sites | Built on existing database replication/sync technology, not a custom-built sync protocol |
| SR-NF01 | 99.99% uptime with 5-second automatic failover | Standard high-availability clustering pattern (load balancer + standby node + heartbeat check) |
| SR-NF02 | Smart card authentication, 8-digit employee ID extraction | Off-the-shelf smart card hardware and authentication protocol |
| SR-NF03 | TLS 1.3 (in transit) and AES-256 (at rest) encryption | Existing, industry-standard cryptographic libraries, already validated through widespread use |
| SR-NF08 | Linux-based data centre infrastructure | Existing operating system and hosting infrastructure, not built by the Mentcare team |

## Reuse-Oriented — How it works :
Integrate an existing smart card authentication module and configure it against staff employee IDs (SR-NF02). Integrate existing TLS 1.3 and AES-256 encryption libraries into the data pipeline (SR-NF03). Configure a standard server cluster with load balancing and heartbeat-based failover (SR-NF01) on the health authority's existing Linux data centre (SR-NF08). Integrate existing database replication/offline-sync technology for clinics without reliable connectivity (SR-F07). Each component is validated through integration testing — confirming the reused component works correctly with Mentcare's core system — rather than unit testing new logic, since the logic itself already exists and is proven.

### Reference

- [S5] SlideShare, "Ch 2 Software Engineering" (Sommerville Ch. 2 slides) — https://www.slideshare.net/slideshow/ch-2-software-engineering/91393431

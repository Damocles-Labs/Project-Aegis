# Data Privacy Ledger: The Sovereignty Standards

This document outlines how Project Aegis handles personal information. Unlike traditional AI platforms, the "Steward" operates on a **Zero-Exfiltration** policy.

<br>

## 1. Data Classification & Memory Tiers
The Steward manages information through a "Decaying Detail, Increasing Insight" model. As data becomes more personal and "intelligent," the physical security surrounding it hardens.

| Tier | Data Nature | Retention Logic | Shorthand Method | Security Level |
| :--- | :--- | :--- | :--- | :--- |
| **Tier 1: Sensory** | Raw logs, casual queries, session scratchpads. | 48-Hour Decay | None (Raw) | **Shield-Encrypted (RAM-Only)** |
| **Tier 2: Narrative** | Professional goals, project history, relationships. | Life-of-Project | **Knowledge Graph** | **Vault-Encrypted (SSD)** |
| **Tier 3: Essence** | Personal values, deep reflections, long-term patterns. | Permanent | **Vector Embeddings** | **Air-Gapped / Multi-Key Auth** |
| **Tier 4: The Archive** | Technical manuals, large PDFs, historical records. | Cold Storage | Indexed (RAG) | **Hardware-Locked (Read-Only)** |

<br>

## 2. Verification: The Transparency Protocols
Trust is a two-way street. Project Aegis provides three "Truth-Checks" that allow the user to verify the integrity of their data at any time.

### **The "Memory Audit" (Tier 2 & 3 Verification)**
The user can command the Steward to: *"Generate a Memory Map."*
* **The Result:** The system produces a visual or text-based report of every "Knowledge Graph" node and "Vector Cluster" currently stored. 
* **The Goal:** This allows the user to see exactly what the Steward "thinks" it knows about them, ensuring no false assumptions or "hallucinated traits" are taking root.

### **The "Leak Test" (Tier 1 Verification)**
Aegis includes a built-in "Packet Sniffer" in the Shield interface.
* **The Action:** The user can initiate a 60-second "Silence Audit." 
* **The Result:** The system shows a real-time log of all outgoing traffic. If the Steward is truly local, the log will show **Zero** packets leaving the system while you are interacting with it. If it’s quiet, it’s private.

### **The "Mirror Test" (Cognitive Verification)**
The user can ask: *"Steward, reflect my current core values and objectives."*
* **The Result:** The Steward synthesizes Tier 3 (Essence) data to describe the user’s trajectory.
* **The Goal:** This verifies that the AI’s "Internal Model" of the user is accurate. If the reflection is distorted, the user knows to perform a **Selective Amnesia** or update their context.

### **The "Physical Key-Check" (Tier 3 & 4 Verification)**
To verify the Air-Gap and Encryption:
* **The Test:** Attempt to access "Essence" or "Archive" data while the physical FIDO2/YubiKey is removed from the Vault.
* **The Expected Result:** The system should return a "Hardware Lockout" error. This proves that the data isn't just "hidden" behind a password, but is physically inaccessible without your key in the slot.

<br>

## 3. The "Right to Forget" (The Purge)
The user has total control over the Steward’s memory. The following commands are hard-coded into the system logic:
* **"Clear Today":** Wipes all Ephemeral and Operational data from the last 24 hours.
* **"Selective Amnesia":** Allows the user to highlight a specific topic or time period for permanent deletion from the Vault.
* **"Nuke Protocol":** A physical multi-key command that wipes the Vault's internal SSDs entirely.

<br>

## 4. Local-Only Processing (The Blood-Oath)
* **No Inference Leakage:** Model weights and KV-caches are never shared.
* **Vector Database Isolation:** The local vector database (where the Steward "remembers" your data) is encrypted with a user-provided physical key (FIDO2). 
* **Zero Telemetry:** The Shield blocks all internal OS attempts to report "Usage Statistics" to hardware manufacturers.

---

> "You own your history. The Steward simply helps you navigate it."

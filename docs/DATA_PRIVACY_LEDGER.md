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

## 2. The "Right to Forget" (The Purge)
The user has total control over the Steward’s memory. The following commands are hard-coded into the system logic:
* **"Clear Today":** Wipes all Ephemeral and Operational data from the last 24 hours.
* **"Selective Amnesia":** Allows the user to highlight a specific topic or time period for permanent deletion from the Vault.
* **"Nuke Protocol":** A physical multi-key command that wipes the Vault's internal SSDs entirely.

<br>

## 3. Local-Only Processing (The Blood-Oath)
* **No Inference Leakage:** Model weights and KV-caches are never shared.
* **Vector Database Isolation:** The local vector database (where the Steward "remembers" your data) is encrypted with a user-provided physical key (FIDO2). 
* **Zero Telemetry:** The Shield blocks all internal OS attempts to report "Usage Statistics" to hardware manufacturers.

---

> "You own your history. The Steward simply helps you navigate it."

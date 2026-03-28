# Project Aegis: Bill of Materials (BOM)
> **Target Baseline:** 2026 Sovereign Research Specifications

### **1. Core Compute (The Vault)**
| Component | Specification | Justification |
| :--- | :--- | :--- |
| **GPU Array** | 2x NVIDIA RTX 5090 (32GB GDDR7 each) | Required for 4-bit/6-bit quantization of 70B+ parameter models. |
| **Memory** | 128GB DDR5-6400+ | Large context window handling and local vector database indexing. |
| **Storage** | 4TB NVMe Gen5 (DirectStorage) | Rapid loading of model weights (GGUF/EXL2) for near-instant inference. |

<br>

### **2. Network & Security (The Shield)**
| Component | Specification | Justification |
| :--- | :--- | :--- |
| **Gateway Host** | Protectli Vault (6-Port / Intel i7) | Hardened physical firewall running a zero-telemetry Linux kernel. |
| **Access Node** | Starlink Mini | Geospatial independence for mobile "Industrial-Edge" operations. |
| **The Bridge** | Physical USB 4.0 Data Diode | Hardware-level air-gap for sensitive data ingestion. |

<br>

### **3. Power & Resilience**
| Component | Specification | Justification |
| :--- | :--- | :--- |
| **Power Station** | EcoFlow Delta 2 Max | Sustained off-grid power for Dual-GPU inference cycles (2400W Peak). |
| **Enclosure** | Pelican 1615 Air Case | Ruggedization for transport in high-activity environments (Subaru Crosstrek). |

---

### **Engineering Notes**
* **VRAM Target:** 64GB total VRAM is the minimum threshold for running top-tier reasoning models without significant loss of "intelligence" via high quantization.
* **Thermal Profile:** Active liquid cooling is recommended for the Vault to prevent thermal throttling during long-context "Deep Research" sessions.

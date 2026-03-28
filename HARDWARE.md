# Aegis Project: Bill of Materials (BOM)
> **Status:** Phase 1 Procurement (Targeting July 2026 Sprint)

| Component | Technical Specification | Role in Architecture |
| :--- | :--- | :--- |
| **Primary Node** | Dual NVIDIA RTX 5090 (32GB GDDR7) | **The Vault:** Local inference for 70B+ models. |
| **Gateway Host** | Protectli Vault (6-Port / Intel i5) | **The Shield:** Physical firewall & packet scrubbing. |
| **The Bridge** | Dedicated USB 4.0 Physical Data Diode | **The Air-Gap:** One-way data flow toggle. |
| **Local Storage** | 4TB NVMe Gen5 (12,000 MB/s) | **The Library:** Rapid weight loading for GGUF/EXL2. |
| **Power/Comms** | EcoFlow Delta 2 Max + Starlink Mini | **Resilience:** Off-grid capability for remote ops. |

---

### **Engineering Notes**
* **Quantization Target:** Optimized for 4-bit and 6-bit GGUF/EXL2 weights to maximize VRAM efficiency.
* **Thermal Management:** Active liquid cooling required for Dual-GPU sustained inference loads.
* **Security:** Gateway runs a hardened Linux kernel with all non-essential ports physically disabled.

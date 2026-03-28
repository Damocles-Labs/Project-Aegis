# Aegis System Architecture: The Shield and The Vault

This document defines the logical and physical boundaries of the Aegis environment, ensuring a "Zero-Trust" posture between the local AI and the external internet.

<br>

## 1. The Physical Boundary (The Air-Gap)
To prevent unauthorized data exfiltration, Aegis maintains a strict separation of concerns:

* **The Shield (Gateway):** A hardened host that manages all external telemetry scrubbing. It acts as the "Bouncer" for the Starlink Mini and the encrypted Tunnel.
* **The Vault (Compute):** A non-networked workstation containing the GPU Array. It does not have a direct path to the internet.
* **The Bridge:** A physical USB 4.0 data diode or manual toggle that allows the user to "push" new models or data into the Vault while maintaining an air-gap during active inference.

<br>

## 2. Remote Orchestration (Mobile Access)
When operating in the field (via the Starlink Mini), the connection follows this hardened path:

1.  **Identity:** User authenticates via Hardware MFA (YubiKey) to the Shield.
2.  **The Tunnel:** A peer-to-peer WireGuard mesh (Tailscale) connects the mobile terminal to the Shield.
3.  **The Proxy:** The Shield strips all outgoing metadata and proxies only the "Model Context Protocol" (MCP) requests to the Vault.
4.  **The Result:** The Vault processes the query and returns the response to the Shield's RAM-only buffer, which is then cleared after the session.

<br>

## 3. Data Sovereignty Protocols
* **Persistence:** No personal data is stored in the "Cloud." All vector databases and chat histories reside on the Vault's encrypted NVMe drives.
* **Telemetry Scrubbing:** The Shield host utilizes `nftables` and DNS-level blocking to ensure that even "leaky" software cannot communicate with corporate servers.
* **Emergency Purge:** A physical "Kill-Switch" on the Vault allows for immediate power-cut and RAM-clearing in the event of a physical security breach.

---

### **Engineering Philosophy**
Architecture is destiny. By separating the **Compute** (Intelligence) from the **Gateway** (Connectivity), Project Aegis ensures that the "Steward" remains loyal only to the individual, regardless of the network environment.

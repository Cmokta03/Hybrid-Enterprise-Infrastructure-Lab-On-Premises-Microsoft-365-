# Hybrid Enterprise Infrastructure Lab (On-Premises + Microsoft 365)

## 🚀 Project Overview
This lab demonstrates the end-to-end deployment of a hybrid enterprise environment, bridging a local Windows Server 2022 infrastructure with Microsoft 365 cloud services. The project focuses on **Hybrid Identity**, **Endpoint Security**, and **Governance**.

### Core Technical Achievements:
* **Hybrid Identity & Sync:** Established a bridge between on-premises AD and the cloud using the Microsoft Entra Provisioning Agent.
* **Security Operations (SecOps):** Enabled advanced security auditing for logon events and hardened server perimeters using Windows Firewall.
* **Endpoint Management:** Managed client workstations through Group Policy Objects (GPOs) to enforce desktop restrictions and security policies.
* **Storage Governance:** Implemented centralized file services with NTFS permissions and FSRM Quotas to manage data limits.
* **Disaster Recovery:** Verified business continuity through full system backups and successful data restoration tests.

---

## 🛠️ Infrastructure Stack
* **On-Premises:** Windows Server 2022 (Domain Controller), Windows 11/10 (Client Workstations), Oracle VirtualBox.
* **Cloud Integration:** Microsoft 365 Enterprise, Microsoft Entra ID.
* **Network Services:** DNS (Forward/Reverse), DHCP, and Static IPv4 addressing.

---

## 📂 Lab Phases

### Phase 1: Core Infrastructure & Connectivity
* **Server Identity:** Modernized server identity (DC01) and established a static network baseline.
* **Domain Initialization:** Promoted the server to a Domain Controller for the `lab.chhiring.online` forest.
* **Connectivity:** Bridged the virtual gap between the DC and client VMs, verifying successful domain authentication.

### Phase 2: Active Directory & Network Management
* **Organizational Hierarchy:** Designed a corporate OU structure with nested sub-OUs for targeted policy application.
* **Core Services:** Automated IP distribution via DHCP and configured DNS forwarders for external name resolution.

### Phase 3: Group Policy & Resource Control
* **Hardening:** Enforced a Default Domain Password Policy and blocked unauthorized system settings via GPOs.
* **Data Control:** Deployed mapped network drives (Z: Drive) and used FSRM to prevent storage exhaustion.

### Phase 4: Monitoring & Disaster Recovery
* **Security Auditing:** Configured Performance Monitor and advanced auditing to maintain a forensic trail of logon events.
* **System Recovery:** Performed full system backups and validated the restoration of deleted files with all permissions intact.

### Phase 5: Remote Access & Hybrid Integration
* **Remote Management:** Enabled secure RDP access for headless data center operations.
* **Cloud Sync:** Successfully mapped local AD objects to the Entra ID tenant, enabling a single set of credentials across the organization.

---

## 📊 Results & Validation
* **Authentication:** Confirmed successful domain joins and user logins via `whoami` checks.
* **Sync Health:** The Microsoft Entra synchronization agent is "Healthy" and exporting local objects to the cloud.
* **Security Baseline:** Verified that security policies (GPOs) correctly restrict standard user access on workstations.
